# Integration Validation and API Testing: Urban Grocers

![Status](https://img.shields.io/badge/Status-Completed-teal)
![Tool](https://img.shields.io/badge/Tool-Postman-orange)
[![Reported Bugs](https://img.shields.io/badge/Reported%20Bugs-See%20%2Freports-red)](./reports)

This repository contains the quality strategy, test scenario design, and full integration test execution for the backend API of the Urban Grocers platform. The project validates system behavior against the latest updates related to product kit management and automatic delivery service calculation.

---

## 🗺️ Business Problem Context

Urban Grocers implemented critical updates to its business logic:

1. **Kit Management Module:** Strict inventory control limiting kits to a maximum of 30 unique products to optimize packaging logistics.
2. **"Order and Go" Delivery Module:** Analytical engine responsible for calculating delivery feasibility and shipping cost based on weight restrictions, item quantity, and delivery time windows.

A failure in the API for these modules could result in unprocessable orders, financial losses caused by incorrect delivery charges, or database inconsistencies.

---

## 🛠️ Technologies and Tools Used

* **API Testing and Execution:** Postman Client (v12.8.4)
* **Defect Management:** Jira Software
* **Test Design Methodology:** Equivalence Partitioning (EP) and Boundary Value Analysis (BVA)
* **Technical Specification:** apiDoc and Backend Requirements Engineering

---

## 📈 Test Strategy

Se aplicó un enfoque de caja negra centrado en la validación de contratos de API e integración de componentes del lado del servidor. Las pruebas se ejecutaron directamente contra los endpoints desplegados en el entorno de pruebas (QA) provisto por el backend.

### Areas Under Test:

1. **Kit Management (`POST /api/v1/kits/:id/products`):** Validation of the physical limit for unique products, payload data types (`productsList`), array structure validation, and HTTP status code handling (`200`, `400`, `404`).

2. **"Order and Go" Service (`POST /order-and-go/v1/delivery`):** Matrix validation of three simultaneous input variables (`productsCount`, `productsWeight`, `deliveryTime`), strict data type analysis, and logical consistency validation against the operational status (`isItPossibleToDeliver`).

---

## 📝 Designed Test Scenarios (Summary)

### 1. Requirement: Kit Management

* **Happy Paths:**
  * Successful addition of valid products to an existing kit (`status: 200 OK`).
  * Persistence validation when adding duplicate items (`quantity` increases while the unique product ID count remains unchanged).

* **Edge Cases and Negative Scenarios:**
  * Exact upper boundary validation (30 unique products -> Successful response).
  * Upper boundary exceeded (31 unique products -> `400 Bad Request`, message: `"No more than 30 items per kit"`).
  * Non-existent product in the database (`400 Bad Request`).
  * Unregistered Kit ID in the request URL (`404 Not Found`).
  * Malformed payload (`productsList` sent as an Object or String instead of an Array -> `400 Bad Request`).

### 2. Requirement: "Order and Go" Service

* **Required Parameter Validation:**
  * Submission of valid numeric parameters according to the calculation matrix (`200 OK`).
  * Omission of individual required fields -> `400 Bad Request`.
  * Invalid data types (Strings in numeric fields) -> `400 Bad Request`.

* **Strict Business Rules:**
  * Boundary value evaluation for delivery schedule restrictions (`deliveryTime` outside operational hours).
  * Scenarios where delivery calculation is not feasible (Exceeded weight or volume limits) -> Successful response with `status: 200 OK` containing the logical flag `"isItPossibleToDeliver": false`.

---

## 📊 Evidence Reports and Defect Integration

All execution evidence (screenshots including status codes, payloads, and validations) is linked in a structured manner. Detailed bug reports are documented in the [reports/bug_reports/](./reports/bug-reports/) section, following the formal structure used in **Jira Software**, enabling full traceability.

## Author
**Ariel Pino Meza** · QA Engineer · [LinkedIn](https://www.linkedin.com/in/ariel-pino-qa-engineer/) · [GitHub](https://github.com/ArielPinoM)