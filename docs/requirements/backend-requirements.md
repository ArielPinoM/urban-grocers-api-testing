# Urban.Grocers Backend Requirements

## Create your own kit
The user can create a custom kit: assign a name, select items, edit or remove products, and modify or delete the kit entirely. Validation messages are displayed for invalid or missing data.

### Kit Creation Constraints
| Name | Constraints | Required |
| :--- | :--- | :---: |
| Kit name | Only Latin alphabet letters, spaces, and hyphens allowed. Length must be between 2 and 15 characters. | ✓ |
| Number of items in the kit | Maximum 30 items. | ✓ |

## Delivery services
### Manual (through the service endpoint)
The user can directly query availability and pricing for each delivery service via its corresponding URL.
The system calculates shipping cost based on two primary variables:
- The number of items.
- The total order weight.
Unlike the automatic calculation method, the order subtotal does not affect shipping cost for this manual endpoint.
Each service enforces its own **constraints** and **rates** depending on schedule, allowed maximum item count, and the data format required.
Refer to the corresponding table for service-specific limits and pricing.
This information should prevent issues when running Android Studio emulation.

### Delivery services constraints
| Name | Schedule | Items per order | Order weight | Delivery time | Delivery cost ($) | Data format |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Speedy | 08-22 | 0-10 | 0-3 kg | 30-35 min | 4 | JSON |
| Speedy | 08-22 | 11-15 | 3.1-7 kg | 30-35 min | 7 | JSON |
| Fast Delivery | 07-21 | 0-7 | 0-2.5 kg | 25-30 min | 3 | XML |
| Fast Delivery | 07-21 | 8-14 | 2.6-6 kg | 25-30 min | 6 | XML |
| Food Service | 06-20 | 0-12 | 0-3.5 kg | 25-30 min | 5 | SOAP |
| Food Service | 06-20 | 13-20 | 3.6-9 kg | 25-30 min | 7 | SOAP |
| Order and Go | 08-22 | 0-8 | 0-3 kg | 20-25 min | 3 | JSON |
| Order and Go | 08-22 | 9-15 | 3.1-6 kg | 20-25 min | 5 | JSON |

### Delivery Service Calculation Details
The user can query which delivery services are available and what the cost would be by accessing each service's specific URL.
When this request is made, the system returns a response with several parameters, including:
```json
{
    "name": "Speedy",
    "isItPossibleToDeliver": true,
    "hostDeliveryCost": 4,
    "toBeDeliveredTime": "30-35 min",
    "clientDeliveryCost": 0
}
```

#### How Is the Cost Calculated?
The calculation is based exclusively on two factors:
- **productsCount**: number of items in the order.
- **productsWeight**: total weight of the items in kilograms.

Each delivery service defines valid ranges for these two variables. Depending on which range the order falls into, the system assigns a specific value for both the internal cost (`hostDeliveryCost`) and the customer cost (`clientDeliveryCost`).

##### Example for the `Speedy` service:
- If the order has up to 10 items and up to 3 kg of weight, the `hostDeliveryCost` is 4 USD.
- If those values are exceeded, the `hostDeliveryCost` increases to 7 USD.

For the customer, the calculation is similar but with wider limits:
- If the order does not exceed 15 items and 7 kg, the `clientDeliveryCost` is 0 USD.
- If either of those limits is exceeded, the `clientDeliveryCost` is 9 USD.

**Important**: with this calculation method, the order total does not affect the delivery cost. In other words, it does not matter if the order is under $7 USD. That rule only applies to the automatic method (POST `/api/v1/orders`).

## Kits URLs
| HTTP method and endpoint | Description |
| :--- | :--- |
| POST `/api/v1/kits` | Create a new kit |
| GET `/api/v1/kits` | Retrieve the list of kits |
| DELETE `/api/v1/kits` | Delete a kit |
| PUT `/api/v1/kits` | Rename a kit or modify the grocery items in a kit |
| GET `/api/v1/kits/search` | Retrieve the list of grocery items in a kit |

## Delivery services URLs
| HTTP method and endpoint | Description |
| :--- | :--- |
| GET `/api/v1/couriers` | Retrieve the list of delivery services |
| POST `/api/v1/couriers/check` | Check if a delivery service is available for the order |
| POST `/api/v1/orders` | Determine which delivery service will handle the order |
| POST `/speedy/v1/calculate` | Check delivery availability and cost for the `Speedy` service |
| POST `/order-and-go/v1/delivery` | Check delivery availability and cost for the `Order and Go` service |
| POST `/fast-delivery/v3.1.1/calculate-delivery.xml` | Check delivery availability and cost for the `Fast Delivery` service |
| POST `/food-service/wsdl` | Check delivery availability and cost for the `Food Service` service |