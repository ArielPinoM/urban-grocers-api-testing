# API Documentation - Urban Grocers

## Couriers > Delivery: "Order and Go"

### POST

`/order-and-go/v1/delivery`

#### Header Examples

```json
{
  "Content-Type": "application/json"
}
```

### Parameters

| Field            | Type   | Description                     |
| :--------------- | :----- | :------------------------------ |
| `productsCount`  | number | Number of products in the order |
| `productsWeight` | number | Weight of the products          |
| `deliveryTime`   | number | Estimated delivery time         |

#### Request Example

```json
{
  "deliveryTime": 9,
  "productsCount": 10,
  "productsWeight": 11
}
```

#### Response Example

```json
HTTP/1.1 200 OK
{
    "name": "Order and Go",
    "clientDeliveryCost": 10,
    "toBeDeliveredTime": {"min": 10, "max": 20},
    "hostDeliveryCost": 23,
    "isItPossibleToDeliver": true
}
```

## Main.Kits > Add products to a kit

### POST

`/api/v1/kits/:id/products`

#### Header Examples

```json
{
  "Content-Type": "application/json"
}
```

### Parameters

| Field          | Type   | Description                                                                                                                      |
| :------------- | :----- | :------------------------------------------------------------------------------------------------------------------------------- |
| `id`           | number | The kit ID from the kit_model table. Passed in the URL.                                                                          |
| `productsList` | array  | A list of products to be added to the kit. The list contains product IDs and their quantities. Must be sent in the request body. |

#### Request Body Example: Adding Products to a Kit

```json
{
  "productsList": [
    {
      "id": 1,
      "quantity": 2
    },
    {
      "id": 6,
      "quantity": 2
    }
  ]
}
```

#### Response: Successfully Added Products to Kit

```json
HTTP/1.1 200 OK
{
    "id": 2,
    "name": "My Weekend Bundle",
    "productsList": [
        {
            "id": 1,
            "name": "Red Caviar",
            "price": 45,
            "weight": 5,
            "units": "kg",
            "quantity": 2
        },
        {
            "id": 5,
            "name": "Baguette",
            "price": 14,
            "weight": 1,
            "units": "kg",
            "quantity": 2
        }
    ],
    "productsCount": 4
}
```

#### Error: No Matching Kits Found

```json
HTTP/1.1 404 Not found.
{
    "code": 404,
    "message": "Not found"
}
```

#### Error: Invalid JSON Format

```json
HTTP/1.1 400 Bad Request.
{
    "code": 400,
    "message": "Unexpected token 'd', ...\"uantity\": dos\n      \"... is not valid JSON"
}
```

#### Error: Invalid Parameter Value

```json
HTTP/1.1 400 Bad Request.
{
    "code": 400,
    "message": "invalid input syntax for integer: \"131dos11111111111113\""
}
```

## Main.Kits > Create a kit

Endpoint to create a kit for a specific card or user.

- The `Authorization` header or the `cardId` parameter is required to create the kit.
- If a request contains an `Authorization` header with a user's auth token, the kit is created for that user.
- If the `cardId` parameter is provided, the kit is created under the specified card.
- If neither parameter is provided, an error is returned.
- When both parameters are provided, `Authorization` takes priority.

### POST

`/api/v1/kits`

### Headers

| Field                    | Type   | Description                                                                                                    |
| :----------------------- | :----- | :------------------------------------------------------------------------------------------------------------- |
| Authorization `optional` | string | Authorization header in the format `Bearer {authToken}`. When present, kits created by that user are returned. |
| Content-Type `optional`  | string | Default value: `application/json`                                                                              |

#### Header Examples

```json
{
  "Content-Type": "application/json"
}
```

#### Example: Request with user authorization

```json
{
  "Content-Type": "application/json",
  "Authorization": "Bearer jknnFApafP4awfAIFfafam2fma"
}
```

### Parameters

| Field             | Type   | Description                                                                                |
| :---------------- | :----- | :----------------------------------------------------------------------------------------- |
| cardId `optional` | number | The card ID from the card_model table. When provided, the kit is created within this card. |
| name              | string | The kit name to store in the kit_model table.                                              |

### Response: Kit created successfully

```json
HTTP/1.1 201 Created
{
    "name": "My kit",
    "card": {
        "id": 1,
        "name": "For the occasion"
    },
    "productsList": null,
    "id": 7,
    "productsCount": 0
}
```

### Error: Missing required parameters

```json
HTTP/1.1 400 Bad Request.
{
    "code": 400,
    "message": "Not all required parameters were provided"
}
```

### Error: Name validation failed

```json
HTTP/1.1 400 Bad Request.
{
    "code": 400,
    "message": "The name must contain only Latin letters, spaces, and hyphens. It must be 2 to 15 characters long"
}
```

## Main.Kits > Retrieve a kit by name

### GET

`/api/v1/kits/search`

### Parameters

| Field | Type   | Description                              |
| :---- | :----- | :--------------------------------------- |
| name  | string | The kit `name` from the kit_model table. |

### Example: Retrieve a kit named "Sabores de Paris"

`/api/v1/kits/search?name=Sabores%20de%20París`

### Response: Kit retrieved successfully

```json
HTTP/1.1 200 OK
{
    "id": 3,
    "name": "Sabores de París",
    "productsList": [
        {
            "id": 54,
            "name": "Dairy Rich Chocolate Bar - Fruit & Nut",
            "price": 139,
            "weight": 100,
            "units": "g",
            "quantity": 6
        },
           {
               "id": 58,
               "name": "Milk Cookies",
               "price": 239,
               "weight": 100,
               "units": "g",
               "quantity": 8
           },
           {
               "id": 67,
               "name": "Baguette French Recipe",
               "price": 89,
               "weight": 200,
               "units": "g",
               "quantity": 4
           },
           {
               "id": 68,
               "name": "Queso Croissant",
               "price": 79,
               "weight": 75,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 69,
               "name": "French Almond Croissant",
               "price": 129,
               "weight": 120,
               "units": "g",
               "quantity": 7
           },
           {
               "id": 70,
               "name": "Chocolate Croissant",
               "price": 104,
               "weight": 96,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 71,
               "name": "Smoked Salmon Croissant",
               "price": 119,
               "weight": 90,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 72,
               "name": "Belgian Chocolate Cake Mix",
               "price": 359,
               "weight": 125,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 73,
               "name": "Queso para untar: Queso crema",
               "price": 79,
               "weight": 130,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 74,
               "name": "Queso Slices",
               "price": 239,
               "weight": 400,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 75,
               "name": "Queso Spread - Roasted Garlic",
               "price": 129,
               "weight": 200,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 76,
               "name": "Spicy Queso Straw",
               "price": 229,
               "weight": 250,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 77,
               "name": "Rebanadas de queso procesado",
               "price": 220,
               "weight": 250,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 78,
               "name": "Cubos de queso procesado",
               "price": 399,
               "weight": 200,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 79,
               "name": "Soybean Tempeh Cubes",
               "price": 209,
               "weight": 300,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 82,
               "name": "Center Filled Dark Chocolate Cookies",
               "price": 129,
               "weight": 100,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 83,
               "name": "Enrobed Cinnamon Milk Chocolate Dipped Cookies",
               "price": 225,
               "weight": 100,
               "units": "g",
               "quantity": 1
           },
           {
               "id": 84,
               "name": "Oreo & Crème Frozen Dessert",
               "price": 339,
               "weight": 300,
               "units": "ml",
               "quantity": 1
           },
           {
               "id": 85,
               "name": "Chocorich Eclairs Chocolate - Assorted",
               "price": 429,
               "weight": 200,
               "units": "g",
               "quantity": 1
           }
       ],
       "productsCount": 19
   }
```

### Error: No matching kits found

```json
HTTP/1.1 404 Not found.
{
    "code": 404,
    "message": "Not found"
}
```

## Utils > Courier/Warehouse Server Logs

This tool retrieves the latest mixed log lines from all secondary servers (couriers and warehouses). The `count` parameter defines how many lines are read from the end and returned in the response.

### GET

`/api/logs/secondary`

### Parameter

| Field            | Type   | Description                                          |
| :--------------- | :----- | :--------------------------------------------------- |
| count `optional` | number | Number of lines from the end.<br>Default value: `50` |

### Get the last 50 records

`/api/logs/secondary`

### Get the last 100 records

`/api/logs/secondary?count=100`

### Response: Latest log records

```json
2020-08-26T16:07:33.017Z [INFO] [Warehouse][food-city]: Server is listening at port 4022
2020-08-26T16:08:01.324Z [DEBUG] [Warehouse][everything-you-need]: [Request] - ::ffff:127.0.0.1 POST:/everything-you-need/v1/calculate - HTTP/1.1 - application/json - {"deliveryTime":10,"products":[{"id":1,"quantity":1},{"id":4,"quantity":1},{"id":44,"quantity":1}]}
2020-08-26T16:08:01.324Z [DEBUG] [Warehouse][fresh-food]: [Request] - ::ffff:127.0.0.1 POST:/fresh-food/v2.0.1/ct - HTTP/1.1 - application/json - {"deliveryTime":10,"products":[{"id":1,"quantity":1},{"id":4,"quantity":1},{"id":44,"quantity":1}]}
2020-08-26T16:08:01.324Z [DEBUG] [Warehouse][big-world]: [SOAP Client] received <?xml version="1.0" encoding="utf-8"?><soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  xmlns:tns="WebServices.WarehouseWsdl"><soap:Body><tns:checkSupply><tns:deliveryTime>10</tns:deliveryTime><tns:products><tns:products><id>1</id><quantity>1</quantity></tns:products><tns:products><id>4</id><quantity>1</quantity></tns:products><tns:products><id>44</id><quantity>1</quantity></tns:products></tns:products></tns:checkSupply></soap:Body></soap:Envelope>
2020-08-26T16:08:01.361Z [DEBUG] [Warehouse][food-city]: [Request] - ::ffff:127.0.0.1 POST:/food-city/calculate.xml - HTTP/1.1 - application/xml - <InputModel><deliveryTime>10</deliveryTime><product id="1" quantity="1"/><product id="4" quantity="1"/><product id="44" quantity="1"/></InputModel>
2020-08-26T16:39:17.168Z [DEBUG] [Warehouse][big-world]: [SOAP Client] received <?xml version="1.0" encoding="utf-8"?><soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  xmlns:tns="WebServices.WarehouseWsdl"><soap:Body><tns:checkSupply><tns:deliveryTime>10</tns:deliveryTime><tns:products><tns:products><id>1</id><quantity>1</quantity></tns:products><tns:products><id>4</id><quantity>1</quantity></tns:products><tns:products><id>44</id><quantity>1</quantity></tns:products></tns:products></tns:checkSupply></soap:Body></soap:Envelope>
2020-08-26T16:39:17.168Z [DEBUG] [Warehouse][fresh-food]: [Request] - ::ffff:127.0.0.1 POST:/fresh-food/v2.0.1/ct - HTTP/1.1 - application/json - {"deliveryTime":10,"products":[{"id":1,"quantity":1},{"id":4,"quantity":1},{"id":44,"quantity":1}]}
2020-08-26T16:39:17.170Z [DEBUG] [Warehouse][everything-you-need]: [Request] - ::ffff:127.0.0.1 POST:/everything-you-need/v1/calculate - HTTP/1.1 - application/json - {"deliveryTime":10,"products":[{"id":1,"quantity":1},{"id":4,"quantity":1},{"id":44,"quantity":1}]}
2020-08-26T16:39:17.173Z [DEBUG] [Warehouse][food-city]: [Request] - ::ffff:127.0.0.1 POST:/food-city/calculate.xml - HTTP/1.1 - application/xml - <InputModel><deliveryTime>10</deliveryTime><product id="1" quantity="1"/><product id="4" quantity="1"/><product id="44" quantity="1"/></InputModel>
2020-08-26T16:39:21.398Z [DEBUG] [Courier][food-service]: [SOAP Client] received <?xml version="1.0" encoding="utf-8"?><soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  xmlns:tns="WebServices.CourierWsdl"><soap:Body><Request xmlns="WebServices.CourierWsdl"><productsCount>3</productsCount><productsWeight>1.433</productsWeight><deliveryTime>7</deliveryTime></Request></soap:Body></soap:Envelope>
2020-08-26T16:39:21.453Z [DEBUG] [Courier][fast-delivery]: [Request] - ::ffff:127.0.0.1 POST:/fast-delivery/v3.1.1/calculate-delivery.xml - HTTP/1.1 - application/xml - {"InputModel":{"deliveryTime":["7"],"productsWeight":["1.433"],"productsCount":["3"]}}
2020-08-26T16:39:21.481Z [DEBUG] [Courier][order-and-go]: [Request] - ::ffff:127.0.0.1 POST:/order-and-go/v1/delivery - HTTP/1.1 - application/json - {"productsCount":3,"productsWeight":1.433,"deliveryTime":7}
2020-08-26T16:39:21.489Z [DEBUG] [Courier][speedy]: [Request] - ::ffff:127.0.0.1 POST:/speedy/v1/calculate - HTTP/1.1 - application/json - {"productsCount":3,"productsWeight":1.433,"deliveryTime":7}
```

## Utils > Main Server Logs

This tool retrieves the latest lines from the main server log. The `count` parameter defines how many lines are read from the end and returned in the response.

### GET

`/api/logs/main`

### Parameter

| Field            | Type   | Description                                           |
| :--------------- | :----- | :---------------------------------------------------- |
| count `optional` | number | Number of lines from the end.<br>Default value: `50`. |

### Get the last 50 records

`/api/logs/main`

### Get the last 100 records

`/api/logs/main/count=100`

### Response: Latest log records

```json
2020-08-26T16:38:31.489Z [INFO] [Main]: Server is listening at port 4000
2020-08-26T16:38:31.500Z [INFO] [Main]: [SOAP Client] Soap is listening at /api/wsdl
2020-08-26T16:38:31.532Z [DEBUG] [Main]: [SOAP Client] TRAIN client is initialized
2020-08-26T16:38:31.564Z [DEBUG] [Main]: [SOAP Client] WORLD client is initialized
2020-08-26T16:38:31.609Z [INFO] [Main]: [PostgreSQL] PostgreSQL is initialized
2020-08-26T16:38:35.057Z [DEBUG] [Main]: [Request] - ::1 GET:/api/logs/main - HTTP/1.1 -  -
2020-08-26T16:39:17.106Z [DEBUG] [Main]: [Request] - ::1 POST:/api/v1/warehouses/amount?dataType=xml - HTTP/1.1 - application/xml - <root><id>1</id><id>4</id><id>44</id></root>
2020-08-26T16:39:21.358Z [DEBUG] [Main]: [Request] - ::1 POST:/api/v1/couriers/check - HTTP/1.1 - application/json - {"ids":[1,4,44],"deliveryTime":7}
2020-08-26T16:39:36.767Z [DEBUG] [Main]: [Request] - ::1 GET:/api/v1/orders - HTTP/1.1 - application/json - {"productsList":"1,4"}
2020-08-26T16:39:47.908Z [DEBUG] [Main]: [Request] - ::1 GET:/api/logs/main - HTTP/1.1 -  -
2020-08-26T16:07:32.123Z [ERROR] [Main]: Unexpected error:
2020-08-26T16:07:32.127Z [ERROR] [Main]: 	 {"message":"request to http://localhost:4022/food-city/calculate.xml failed, reason: connect ECONNREFUSED 127.0.0.1:4022","type":"system","errno":"ECONNREFUSED","code":"ECONNREFUSED","stack":"FetchError: request to http://localhost:4022/food-city/calculate.xml failed, reason: connect ECONNREFUSED 127.0.0.1:4022\n    at ClientRequest.<anonymous> (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/node-fetch/lib/index.js:1455:11)\n    at ClientRequest.emit (events.js:198:13)\n    at ClientRequest.EventEmitter.emit (domain.js:448:20)\n    at Socket.socketErrorListener (_http_client.js:401:9)\n    at Socket.emit (events.js:198:13)\n    at Socket.EventEmitter.emit (domain.js:448:20)\n    at emitErrorNT (internal/streams/destroy.js:91:8)\n    at emitErrorAndCloseNT (internal/streams/destroy.js:59:3)\n    at process._tickCallback (internal/process/next_tick.js:63:19)"}
2020-08-26T16:07:32.131Z [ERROR] [Main]: Unexpected error:
2020-08-26T16:07:32.162Z [ERROR] [Main]: 	 {"stack":"RangeError [ERR_HTTP_INVALID_STATUS_CODE]: Invalid status code: ECONNREFUSED\n    at ServerResponse.writeHead (_http_server.js:211:11)\n    at ServerResponse._implicitHeader (_http_server.js:202:8)\n    at write_ (_http_outgoing.js:585:9)\n    at ServerResponse.end (_http_outgoing.js:702:5)\n    at ServerResponse.send (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/express/lib/response.js:221:10)\n    at ServerResponse.json (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/express/lib/response.js:267:15)\n    at app.use (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/src/app.ts:77:14)\n    at Layer.handle_error (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/express/lib/router/layer.js:71:5)\n    at trim_prefix (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/express/lib/router/index.js:315:13)\n    at /Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/express/lib/router/index.js:284:7\n    at Function.process_params (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/express/lib/router/index.js:335:12)\n    at next (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/express/lib/router/index.js:275:10)\n    at ServiceContext.next (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/express/lib/router/route.js:127:14)\n    at ServiceInvoker.<anonymous> (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/typescript-rest/src/server/service-invoker.ts:37:21)\n    at Generator.throw (<anonymous>)\n    at rejected (/Users/vladimirlevin/Desktop/Own/ez-lavka/packages/main/node_modules/typescript-rest/dist/server/service-invoker.js:6:65)\n    at process._tickCallback (internal/process/next_tick.js:68:7)","message":"Invalid status code: ECONNREFUSED"}
2020-08-26T16:08:01.311Z [DEBUG] [Main]: [Request] - ::1 POST:/api/v1/warehouses/amount - HTTP/1.1 - application/json - {"ids":[1,4,44]}
```

## Utils > Retrieve database table information

### GET

`/api/db/resources/{table_name}.csv`

### Parameter

| Field      | Type   | Description                                                  |
| :--------- | :----- | :----------------------------------------------------------- |
| table_name | string | The database table name. Passed in the URL. |

### Get the product_model table

`/api/db/resources/product_model.csv`

### Get the kit_model table

`/api/db/resources/kit_model.csv`

### Response: File with product_model table contents

```csv
id,name,price,weight,units,categoryId,
1,Orange Juice - Cold-Pressed, No Added Sugar, Preservative Free,149,473,ml,1
2,Refresco Mountain Dew,89,1,l,1
3,Refresco Pepsi,109,1,l,1
4,Refresco Sprite,79,900,ml,1
5,Jugo Fruit Power: Lichi,349,900,ml,1
```