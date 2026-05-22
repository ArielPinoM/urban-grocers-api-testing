# Test Case Matrix: Kit Management (`POST /api/v1/kits/:id/products`)

**Language**: English (EN)

---

## Test Cases

<table>
<thead>
    <tr>
        <th>Test Case ID</th>
        <th>Test Case Name</th>
        <th>Preconditions</th>
        <th>Test Data</th>
        <th>Steps</th>
        <th>Expected Result</th>
        <th>Actual Result</th>
        <th>Status</th>
        <th>Defect Link</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>TC-KM-01</td>
        <td>Verify that the user can añadir existing products a un kit.</td>
        <td>1. The warehouse system must be active.</td>
        <td>Path params: id = 2<br><pre><code>{
  &quot;productsList&quot;: [
    {
      &quot;id&quot;: 1,
      &quot;quantity&quot;: 1
    }
  ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using id:2 in Path Variables and existing product ID in the request body.<br>
        </td>
        <td>- Existing products are added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>- Existing products were added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-02</td>
        <td>Verify that the kit can have 1 unique product.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
    {
      &quot;id&quot;: 1,
      &quot;quantity&quot;: 1
    }
  ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and a existing product ID in the request body.<br>
        3. Add the product to the kit.<br>
        4. A status code of 200 OK is returned in the response.</td>
        <td>- The existing product is added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>- The existing products is added to the kit.<br>
        - The request status is 200 OK.</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-03</td>
        <td>Verify that the kit can have 29 unique products.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
    { &quot;id&quot;: 1, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 2, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 3, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 4, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 5, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 6, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 7, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 8, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 9, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 10, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 11, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 12, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 13, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 14, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 15, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 16, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 17, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 18, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 19, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 20, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 21, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 22, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 23, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 24, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 25, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 26, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 27, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 28, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 29, &quot;quantity&quot;: 1 }
  ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and the id's in the request body.<br>
        <td>- The existing products are added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>- The existing products are added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-04</td>
        <td>Verify that the kit can have 30 unique products.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
    { &quot;id&quot;: 1, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 2, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 3, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 4, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 5, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 6, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 7, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 8, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 9, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 10, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 11, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 12, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 13, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 14, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 15, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 16, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 17, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 18, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 19, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 20, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 21, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 22, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 23, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 24, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 25, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 26, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 27, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 28, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 29, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 30, &quot;quantity&quot;: 1 }
  ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and the id's in the request body.<br>
        <td>- The existing products are added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>- The existing products are added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-05</td>
        <td>Verify that the kit cannot have 31 unique products.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
    { &quot;id&quot;: 1, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 2, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 3, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 4, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 5, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 6, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 7, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 8, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 9, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 10, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 11, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 12, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 13, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 14, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 15, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 16, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 17, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 18, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 19, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 20, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 21, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 22, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 23, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 24, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 25, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 26, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 27, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 28, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 29, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 30, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 31, &quot;quantity&quot;: 1 }
  ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and the existing products id in the request body.<br>
        3. The products are not added to the kit.<br>
        4. A status code is returned: 400 Bad Request in the response with an error "message": "No más de 30 artículos por conjunto" in the response.</td>
        <td>- The products are not added to the kit.<br>
        - The request status is 400 Bad Request.<br>
        - "message": "No más de 30 artículos por conjunto"</td>
        <td>- The products are not added to the kit.<br>
        - The request status is 400 Bad Request.<br>
        - "message": "No más de 30 artículos por conjunto"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-06</td>
        <td>Verify that the kit cannot have 32 unique products.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
    { &quot;id&quot;: 1, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 2, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 3, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 4, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 5, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 6, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 7, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 8, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 9, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 10, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 11, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 12, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 13, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 14, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 15, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 16, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 17, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 18, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 19, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 20, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 21, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 22, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 23, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 24, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 25, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 26, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 27, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 28, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 29, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 30, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 31, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 32, &quot;quantity&quot;: 1 },
  ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and the existing products id in the request body.<br>
        3. The existing products are not added to the kit.<br>
        4. A status code is returned: 400 Bad Request in the responde with an error "message": "No más de 30 artículos por conjunto" in the response.</td>
        <td>- The products are not added to the kit.<br>
        - The request status is 400 Bad Request.<br>
        - "message": "No más de 30 artículos por conjunto"</td>
        <td>- The products are not added to the kit.<br>
        - The request status is 400 Bad Request.<br>
        - "message": "No más de 30 artículos por conjunto"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-07</td>
        <td>Verify that the kit cannot have 33 unique products.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
    { &quot;id&quot;: 1, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 2, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 3, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 4, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 5, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 6, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 7, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 8, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 9, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 10, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 11, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 12, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 13, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 14, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 15, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 16, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 17, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 18, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 19, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 20, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 21, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 22, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 23, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 24, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 25, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 26, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 27, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 28, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 29, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 30, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 31, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 32, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 33, &quot;quantity&quot;: 1 },
  ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and the existing products id in the request body.<br>
        3. The existing products are not added to the kit.<br>
        4. A status code is returned: 400 Bad Request in the responde with an error "message": "No más de 30 artículos por conjunto" in the response.</td>
        <td>- The products are not added to the kit.<br>
        - The request status is 400 Bad Request.<br>
        - "message": "No más de 30 artículos por conjunto"</td>
        <td>- The products are not added to the kit.<br>
        - The request status is 400 Bad Request.<br>
        - "message": "No más de 30 artículos por conjunto"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-08</td>
        <td>The product count of a kit can be greater than 30 (productsCount > 30).</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
    { &quot;id&quot;: 1, &quot;quantity&quot;: 10 },
    { &quot;id&quot;: 2, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 3, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 4, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 5, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 6, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 7, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 8, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 9, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 10, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 11, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 12, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 13, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 14, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 15, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 16, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 17, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 18, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 19, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 20, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 21, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 22, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 23, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 24, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 25, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 26, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 27, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 28, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 29, &quot;quantity&quot;: 1 },
    { &quot;id&quot;: 30, &quot;quantity&quot;: 1 }
  ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and the existing products id in the request body. The total product quantity is 39.<br>
        3. The existing products are added to the kit "TestKit".<br>
        4. A status code of 200 OK is returned in the response.</td>
        <td>- The existing products are added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>- The existing products are added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-09</td>
        <td>Cannot add non-existing products to an existing kit.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
    &quot;productsList&quot;: [
        {
            &quot;id&quot;: 93,
            &quot;quantity&quot;: 1
        }
    ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables a non-existent product ID in the request body.<br>
        3. The product is not added to the kit "TestKit".<br>
        4. A status code is returned: 404 Not Found in the response.</td>
        <td>- The product is not added to the kit.<br>
        - A status code is returned: 404 Not Found in the response.<br>
        - "message": "Not found".</td>
        <td>- The product is added to the kit.<br>
        - The request status is 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-01.md#br-01">BR-01</a></td>
    </tr>
    <tr>
        <td>TC-KM-10</td>
        <td>Cannot add existing products to a non-existent kit.</td>
        <td>1. The warehouse system must be active.</td>
        <td>Path params: id = 10<br><pre><code>{
    &quot;productsList&quot;: [
        {
            &quot;id&quot;: 1,
            &quot;quantity&quot;: 1
        }
    ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request with id: 10 in Path Variables and an existing product ID in the request body.<br>
        3. The product is not added to the non-existing kit.<br>
        4. A status code is returned: 404 Not Found in the response.</td>
        <td>- The product is not added to the non-existing kit.<br>
        - A status code is returned: 404 Not Found in the response.<br>
        - "message": "Not found".</td>
        <td>- The product is not added to the non-existing kit.<br>
        - A status code is returned: 404 Not Found in the response.<br>
        - "message": "Not found".</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-11</td>
        <td>400 Bad Request is returned if "productsList" is null.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: null
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and productsList = null in the request body.<br>
        </td>
        <td>- 400 Bad Request is returned in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- 500 Internal Server Error is returned in the response.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-02.md#br-02">BR-02</a></td>
    </tr>
    <tr>
        <td>TC-KM-12</td>
        <td>400 Bad Request is returned in the request body, when "productsList" is an integer number.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: 1
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and productsList = 1 in the request body.</td>
        <td>- 400 Bad Request is returned in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- 500 Internal Server Error is returned in the response.<br>
        - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-03.md#br-03">BR-3</a></td>
    </tr>
    <tr>
        <td>TC-KM-13</td>
        <td>A 400 Bad Request status code is returned if the "productsList" value in the request body is a floating-point number.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: 1.1
}</code></pre></td>
        <td>1. Select the POST method and send a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" ID in the Path Variables and productsList = 1.1 in the request body.</td>
        <td>- A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A 500 Internal Server Error status code is returned in the response.<br>
        - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-04.md#br-04">BR-4</a></td>
    </tr>
    <tr>
        <td>TC-KM-14</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "productsList" es un string.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: &quot;string&quot;
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables a productsList = "string" in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.<br>
        - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-5?atlOrigin=eyJpIjoiOTY5NDExMTc2YzA0NDE5N2E4Y2UyNzVhN2QxMWFlNTYiLCJwIjoiaiJ9" target="_blank">BR-5</a></td>
    </tr>
    <tr>
        <td>TC-KM-15</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "productsList" es un booleano.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: true
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables a productsList = true in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.<br>
        - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-6?atlOrigin=eyJpIjoiMjFiMzIzOWY1NDNjNGQyMGEwMzEwNDhkMWE4MmU3MDAiLCJwIjoiaiJ9" target="_blank">BR-6</a></td>
    </tr>
    <tr>
        <td>TC-KM-16</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "productsList" es un objeto.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: {}
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables a productsList = {} in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.<br>
        - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-7?atlOrigin=eyJpIjoiM2JhYmYxY2IxYzgwNGZiZmJmOGJkZmE0NDcxZDIxZmIiLCJwIjoiaiJ9" target="_blank">BR-7</a></td>
    </tr>
    <tr>
        <td>TC-KM-17</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es null "quantity" es válido.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: null,
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, an id = null valid "quantity" in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code of 200 OK is returned in the response.<br>
        - The product is added to the kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-8?atlOrigin=eyJpIjoiMDNhMDczZGU2YTE5NDQ2MjgxODQ4ODk4ODYyYTFlNWUiLCJwIjoiaiJ9" target="_blank">BR-8</a></td>
    </tr>
    <tr>
        <td>TC-KM-18</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es un número flotante "quantity" es válido.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1.1,
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, an id = 1.1 valid "quantity" in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-9?atlOrigin=eyJpIjoiODVmMGY5Njk4YjE2NGZkOGIwYjNkZDNmNDQzZDNkZWUiLCJwIjoiaiJ9" target="_blank">BR-9</a></td>
    </tr>
    <tr>
        <td>TC-KM-19</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es un string "quantity" es válido.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: &quot;string&quot;,
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, an id = "string" valid "quantity" in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-11?atlOrigin=eyJpIjoiNTA3NTg1ZTk2MWI5NDA0NDhmZGY5N2JiNWU1M2E3MzYiLCJwIjoiaiJ9" target="_blank">BR-11</a></td>
    </tr>
    <tr>
        <td>TC-KM-20</td>
        <td>A status code is returned 500 Internal Server Error si in the request body, el valor de "productsList" es un array vacío.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: []
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables un "productsList" = [] in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-10?atlOrigin=eyJpIjoiYWEyMDRmZTg2OGQ0NGYyMjg4OWMwNTg4ODRjMmU3NmEiLCJwIjoiaiJ9" target="_blank">BR-10</a></td>
    </tr>
    <tr>
        <td>TC-KM-21</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es un booleano "quantity" es válido.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: true,
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, an id = true valid "quantity" in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-12?atlOrigin=eyJpIjoiNThjMDMwNTI4ZTU3NDBhN2FjNGYwOGM3NjJlNWFhYTAiLCJwIjoiaiJ9" target="_blank">BR-12</a></td>
    </tr>
    <tr>
        <td>TC-KM-22</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es un objeto "quantity" es válido.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: {},
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, an id = {} valid "quantity" in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-13?atlOrigin=eyJpIjoiMzM0MGM5N2RiYjVhNDFhZGJjY2FiNDUyM2E0MjVhNjgiLCJwIjoiaiJ9" target="_blank">BR-13</a></td>
    </tr>
    <tr>
        <td>TC-KM-23</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es un array "quantity" es válido.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: [],
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, an id = [] valid "quantity" in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-14?atlOrigin=eyJpIjoiN2Q0ZGI3NGQ0OGQ1NDZiNjlkYWVmMTcwNzhmOGFjYjMiLCJwIjoiaiJ9" target="_blank">BR-14</a></td>
    </tr>
    <tr>
        <td>TC-KM-24</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es válido "quantity" es null.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: null
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, a valid id "quantity" = null in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A status code of 200 OK is returned in the response.<br>
        - The product is added to the kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-15?atlOrigin=eyJpIjoiMjVlODYyODI0NGRhNDk2NDlkZWM2NGVjNzg0YmMxZDQiLCJwIjoiaiJ9" target="_blank">BR-15</a></td>
    </tr>
    <tr>
        <td>TC-KM-25</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es válido "quantity" es un número flotante.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: 1.1
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, a valid id "quantity" = 1.1 in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for type integer: ..."<br>
        - The product is not added al kit.</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.<br>
        - "message": "invalid input syntax for type integer: \"1.1\""<br>
        - The product is not added al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-16?atlOrigin=eyJpIjoiNDZhYjJiMjA3YTdiNDg1Njk4NzMzZmY5Mzg4OGQyMzMiLCJwIjoiaiJ9" target="_blank">BR-16</a></td>
    </tr>
    <tr>
        <td>TC-KM-26</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es válido "quantity" es un string.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: &quot;string&quot;
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, a valid id "quantity" = "string" in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for type integer: ..."<br>
        - The product is not added al kit.</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.<br>
        - "message": "invalid input syntax for type integer: \"0string\""<br>
        - The product is not added al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-17?atlOrigin=eyJpIjoiYzViMDdkYWVjM2FlNDQzYjhlYzMyOGQxODE3Nzc4ZmYiLCJwIjoiaiJ9" target="_blank">BR-17</a></td>
    </tr>
    <tr>
        <td>TC-KM-27</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es válido "quantity" es un booleano.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: true
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, a valid id "quantity" = true in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for type integer: ..."<br>
        - The product is not added al kit.</td>
        <td>- A el código de estado: 200 OK in the response.<br>
        - The product is added to the kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-18?atlOrigin=eyJpIjoiNGRhNWJlNDZlOTE0NDBkN2JiMjU2ZDExZjVmMzg0YWEiLCJwIjoiaiJ9" target="_blank">BR-18</a></td>
    </tr>
    <tr>
        <td>TC-KM-28</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es válido "quantity" es un objeto.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: {}
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, a valid id "quantity" = {} in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for type integer: ..."<br>
        - The product is not added al kit.</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.<br>
        - "message": "invalid input syntax for type integer: \"0[object Object]\""<br>
        - The product is not added al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-19?atlOrigin=eyJpIjoiNWNkZTA2M2MyODc0NDliNGFmMjA4NWU4YmEzMGM1M2QiLCJwIjoiaiJ9" target="_blank">BR-19</a></td>
    </tr>
    <tr>
        <td>TC-KM-29</td>
        <td>A status code is returned 400 Bad Request si in the request body, el valor de "id" es válido "quantity" es un array.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: []
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, a valid id "quantity" = [] in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "invalid input syntax for type integer: ..."<br>
        - The product is not added al kit.</td>
        <td>- A el código de estado: 200 OK in the response.<br>
        - The product is added to the kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-20?atlOrigin=eyJpIjoiZDAwMTljMjY1OWQ3NDAyMDk2NTdiMjRmMjM2MGYxYWUiLCJwIjoiaiJ9" target="_blank">BR-20</a></td>
    </tr>
    <tr>
        <td>TC-KM-30</td>
        <td>A status code is returned 400 Bad Request si no se completa el cuerpo de la solicitud al añadir productos al kit.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code></code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, leave empty el cuerpo de la solicitud.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "Request body is required"</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-21?atlOrigin=eyJpIjoiOGY5ZTExYTM4NDNjNDI1Y2I5MTUzNjAzZGUzZmQ4MzUiLCJwIjoiaiJ9" target="_blank">BR-21</a></td>
    </tr>
    <tr>
        <td>TC-KM-31</td>
        <td>A status code is returned 400 Bad Request si no está presente el "id" del producto in the request body al añadir productos al kit.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
   &quot;productsList&quot;: [
      {
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, do not write el "id" agregar valid "quantity" in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "id is required"</td>
        <td>- A status code of 200 OK is returned in the response.<br>
        - The product is added to the kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-22?atlOrigin=eyJpIjoiMzc2ZjM2YWUxODE1NDIwMThkOWU0ZDFhNzExYjA4NTQiLCJwIjoiaiJ9" target="_blank">BR-22</a></td>
    </tr>
    <tr>
        <td>TC-KM-32</td>
        <td>A status code is returned 400 Bad Request si no está presente "quantity" del producto in the request body al añadir productos al kit.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
   &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, do not write "quantity" agregar un "id" válido in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "quantity is required"</td>
        <td>- A status code is returned: 500 Internal Server Error in the response.<br>
        - "message": "invalid input syntax for type integer: \"NaN\""</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-23?atlOrigin=eyJpIjoiZmI0MjQwMjkxYWM0NDdlNjg3MmQzNmQwZDU2YWZlMjgiLCJwIjoiaiJ9" target="_blank">BR-23</a></td>
    </tr>
    <tr>
        <td>TC-KM-33</td>
        <td>A status code is returned 400 Bad Request si se envía una clave diferente a las requeridas in the request body al añadir productos al kit.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
   &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: 1,
         &quot;extraParameter&quot;: true
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, write un producto válido más el parámetro extra "extraParameter": true in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "extraParameter is not allowed"</td>
        <td>- A el código de estado: 200 OK in the response.<br>
        - The product is added to the kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-24?atlOrigin=eyJpIjoiODNmZDlmYWI1NDc3NGE2M2ExOTcwNzcxMDY0MzYzZDYiLCJwIjoiaiJ9" target="_blank">BR-24</a></td>
    </tr>
    <tr>
        <td>TC-KM-34</td>
        <td>A status code is returned 400 Bad Request si el formato del cuerpo de la solicitud es incorrecto en el endpoint "api/v1/kits/:id/products".</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
   &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: dos
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, write "id":1 "quantity": dos in the request body.<br>
        3. A status code is returned: 400 Bad Request in the response.</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "Unexpected token ... is not valid JSON"</td>
        <td>- A status code is returned: 400 Bad Request in the response.<br>
        - "message": "Unexpected token ... is not valid JSON"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-35</td>
        <td>A 200 OK si el cuerpo de la solicitud incluye valores válidos en los campos obligatorios al verificar si el pedido se puede hacer (Entrega: Order and Go).</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-36</td>
        <td>When sending a valid request to the endpoint "/order-and-go/v1/delivery" se obtiene a response with the required parameters.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A una respuesta con los siguientes parámetros:<br>
        - "name"<br>
        - "clientDeliveryCost"<br>
        - "toBeDeliveredTime"<br>
        - "hostDeliveryCost"<br>
        - "isItPossibleToDeliver"</td>
        <td>- A una respuesta con los siguientes parámetros:<br>
        - "name"<br>
        - "clientDeliveryCost"<br>
        - "toBeDeliveredTime"<br>
        - "hostDeliveryCost"<br>
        - "isItPossibleToDeliver"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-37</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo string al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: &quot;string&quot;,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-25?atlOrigin=eyJpIjoiMmFjNjY1YjM0MjI4NDRjNGIxZjYyMGQyYzczNDhjMDUiLCJwIjoiaiJ9" target="_blank">BR-25</a></td>
    </tr>
    <tr>
        <td>TC-KM-38</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo flotante al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15.1,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-26?atlOrigin=eyJpIjoiMjE4NDFlM2ZlZjI0NGM4ZGJkOWFlMGJiNDRiMDUzNmEiLCJwIjoiaiJ9" target="_blank">BR-26</a></td>
    </tr>
    <tr>
        <td>TC-KM-39</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo booleano al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: true,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-27?atlOrigin=eyJpIjoiOWQ1MmVkMTAxYjdjNDNkOGJhMTNmN2MyNzI3NWYxODAiLCJwIjoiaiJ9" target="_blank">BR-27</a></td>
    </tr>
    <tr>
        <td>TC-KM-40</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime = null al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: null,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-28?atlOrigin=eyJpIjoiMjVhZDkwODc4NDU2NGQ0OWE4YTA3ZTE2NjQyMmI0N2MiLCJwIjoiaiJ9" target="_blank">BR-28</a></td>
    </tr>
    <tr>
        <td>TC-KM-41</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo objeto al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: {},
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-29?atlOrigin=eyJpIjoiZDU3M2I5MDE4OThkNDgzOTgwMTE1ZjdjMjc5OWIzYjUiLCJwIjoiaiJ9" target="_blank">BR-29</a></td>
    </tr>
    <tr>
        <td>TC-KM-42</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo array al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: [],
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-30?atlOrigin=eyJpIjoiYjM3MzRjOWI1MDYwNGE3OGFhNDkyYmE1OGQwYjc4NDQiLCJwIjoiaiJ9" target="_blank">BR-30</a></td>
    </tr>
    <tr>
        <td>TC-KM-43</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo string al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: &quot;string&quot;,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-31?atlOrigin=eyJpIjoiNzRmNjkyMDcyODkwNDNkM2IxNmRiZTEyZjk5ZWIzNWQiLCJwIjoiaiJ9" target="_blank">BR-31</a></td>
    </tr>
    <tr>
        <td>TC-KM-44</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo flotante al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 1.1,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-32?atlOrigin=eyJpIjoiNTFmMjU5YzM2NDU3NDM3NDg0ZGQ0NTczNWMwNWRiZGQiLCJwIjoiaiJ9" target="_blank">BR-32</a></td>
    </tr>
    <tr>
        <td>TC-KM-45</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo booleano al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: true,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-33?atlOrigin=eyJpIjoiZTdkOGNmZTFlMzQ5NGY2NGI4MDE0M2E0MmM5MjI5NWMiLCJwIjoiaiJ9" target="_blank">BR-33</a></td>
    </tr>
    <tr>
        <td>TC-KM-46</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsCount = null al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: null,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-34?atlOrigin=eyJpIjoiZDgyODlkYWE0MWFkNGQyZGFmMzczZDU1OTEwMzMzOTgiLCJwIjoiaiJ9" target="_blank">BR-34</a></td>
    </tr>
    <tr>
        <td>TC-KM-47</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo objeto al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: {},
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-35?atlOrigin=eyJpIjoiYjY4YzVkOWIwZWE0NDA2ZWFlZmQwOTQ1MDYyNzcwN2UiLCJwIjoiaiJ9" target="_blank">BR-35</a></td>
    </tr>
    <tr>
        <td>TC-KM-48</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo array al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: [],
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-36?atlOrigin=eyJpIjoiZDUxMThkOWQ4YTE1NGQ2ZjliZWUwMGRmOGFjZjljODciLCJwIjoiaiJ9" target="_blank">BR-36</a></td>
    </tr>
    <tr>
        <td>TC-KM-49</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsWeight tipo string al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: &quot;string&quot;
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-37?atlOrigin=eyJpIjoiZTkxNTNlYzA2MzAyNDY4MTg1YTM0YjBhZDkxMmY4ZGIiLCJwIjoiaiJ9" target="_blank">BR-37</a></td>
    </tr>
    <tr>
        <td>TC-KM-50</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsWeight tipo booleano al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: true
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-38?atlOrigin=eyJpIjoiZWUyY2JhZWRiM2FkNGM5NzlkOWJjMDkwNDhmNTI3NzAiLCJwIjoiaiJ9" target="_blank">BR-38</a></td>
    </tr>
    <tr>
        <td>TC-KM-51</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsWeight = null al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: null
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-39?atlOrigin=eyJpIjoiYjkwM2I2MDJiYzE3NDBlZDgzYzJiOTRkMGY4MmQwYjAiLCJwIjoiaiJ9" target="_blank">BR-39</a></td>
    </tr>
    <tr>
        <td>TC-KM-52</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsWeight tipo objeto al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: {}
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-40?atlOrigin=eyJpIjoiMTAxM2Q4YzdhNDU0NDZhODg2ODlkYjQ4YTI4Nzk4ZjgiLCJwIjoiaiJ9" target="_blank">BR-40</a></td>
    </tr>
    <tr>
        <td>TC-KM-53</td>
        <td>A 400 Bad Request al enviar la solicitud con el valor del campo productsWeight tipo array al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: []
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-41?atlOrigin=eyJpIjoiNGQzNTIwOTQ2Njg5NDU1M2IwYTU3ODVhOWUxMTc2MjEiLCJwIjoiaiJ9" target="_blank">BR-41</a></td>
    </tr>
    <tr>
        <td>TC-KM-54</td>
        <td>A 400 Bad Request al enviar la solicitud omitiendo el campo deliveryTime al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5 
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "deliveryTime is required".</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-42?atlOrigin=eyJpIjoiMGUyYzlmNmRlNmU1NDgzMjkxYzg4NWViYjYyZjdmMjYiLCJwIjoiaiJ9" target="_blank">BR-42</a></td>
    </tr>
    <tr>
        <td>TC-KM-55</td>
        <td>A 400 Bad Request al enviar la solicitud omitiendo el campo productsCount al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsWeight&quot;: 1.5 
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "productsCount is required".</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-43?atlOrigin=eyJpIjoiM2JkNTI4NzY0MGZjNDc1NWJiMDg0MzIxYjEwY2Q3ZmUiLCJwIjoiaiJ9" target="_blank">BR-43</a></td>
    </tr>
    <tr>
        <td>TC-KM-56</td>
        <td>A 400 Bad Request al enviar la solicitud omitiendo el campo productsWeight al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4 
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "productsWeight is required".</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-44?atlOrigin=eyJpIjoiMmJlNDA5MjAxNTQ0NDc3Zjk0YjIxMzAxNzNhYjEwMDkiLCJwIjoiaiJ9" target="_blank">BR-44</a></td>
    </tr>
    <tr>
        <td>TC-KM-57</td>
        <td>A 400 Bad Request al omitir el cuerpo de la solicitud al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>Se omite el cuerpo de la solicitud.</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "Request body is required".</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-45?atlOrigin=eyJpIjoiZTczY2VhMTM4OTI2NDU2ZWE2YjA1ZWJlNDBlM2FhM2QiLCJwIjoiaiJ9" target="_blank">BR-45</a></td>
    </tr>
    <tr>
        <td>TC-KM-58</td>
        <td>A 400 Bad Request al enviar un campo no esperado in the request body al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5,
    &quot;extraParameter&quot;: &quot;string&quot;
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 400 Bad Request.<br>
        - "message": "extraParameter is not allowed".</td>
        <td>- A el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-46?atlOrigin=eyJpIjoiNTI2YmM5MGYxZjQ5NGUxNGE2NDBkNzlmNTQ2YzAyNTEiLCJwIjoiaiJ9" target="_blank">BR-46</a></td>
    </tr>
    <tr>
        <td>TC-KM-59</td>
        <td>The "isItPossibleToDeliver" field in the response is "true" si "deliveryTime" = 8 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 8,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-60</td>
        <td>The "isItPossibleToDeliver" field in the response is "true" si "deliveryTime" = 9 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 9,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-61</td>
        <td>The "isItPossibleToDeliver" field in the response is "true" si "deliveryTime" = 15 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-62</td>
        <td>The "isItPossibleToDeliver" field in the response is "true" si "deliveryTime" = 21 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 21,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-63</td>
        <td>The "isItPossibleToDeliver" field in the response is "true" si "deliveryTime" = 22 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 22,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-64</td>
        <td>The "isItPossibleToDeliver" field in the response is "false" si "deliveryTime" = 3 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 3,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": false.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-47?atlOrigin=eyJpIjoiM2U0NDdjNzAyYjJiNGU1OWIyOTlmNDVlMDIyMjNlMmIiLCJwIjoiaiJ9" target="_blank">BR-47</a></td>
    </tr>
    <tr>
        <td>TC-KM-65</td>
        <td>The "isItPossibleToDeliver" field in the response is "false" si "deliveryTime" = 6 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 6,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": false.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-48?atlOrigin=eyJpIjoiYTA5OGYyYmM1ZTdjNGZiZDg5N2E1ZjVlZDg2ZGE1NTIiLCJwIjoiaiJ9" target="_blank">BR-48</a></td>
    </tr>
    <tr>
        <td>TC-KM-66</td>
        <td>The "isItPossibleToDeliver" field in the response is "false" si "deliveryTime" = 7 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 7,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": false.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-49?atlOrigin=eyJpIjoiYjc2NGVkMGNiZTU5NDA0Njg5MGI2YzFhNmRjYWYwMzkiLCJwIjoiaiJ9" target="_blank">BR-49</a></td>
    </tr>
    <tr>
        <td>TC-KM-67</td>
        <td>The "isItPossibleToDeliver" field in the response is "false" si "deliveryTime" = 23 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 23,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": false.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-50?atlOrigin=eyJpIjoiZmY0OTQ5NzhkMDU5NDVjM2FlYWYzMDUwZGRjYWY3NmUiLCJwIjoiaiJ9" target="_blank">BR-50</a></td>
    </tr>
    <tr>
        <td>TC-KM-68</td>
        <td>The "isItPossibleToDeliver" field in the response is "false" si "deliveryTime" = 0 el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 0,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": false.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-51?atlOrigin=eyJpIjoiZmMwMjE0NTEzYjAxNDg3ZGE1NmZjZDY2ZTVjMjgyODkiLCJwIjoiaiJ9" target="_blank">BR-51</a></td>
    </tr>
    <tr>
        <td>TC-KM-69</td>
        <td>El parámetro "name" field in the response is igual a "Order and Go" when making a request with all valid required fields to the endpoint "/order-and-go/v1/delivery".</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "name": "Order and Go".</td>
        <td>- A el código de estado: 200 OK.<br>
        - "name": "Order and Go".</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-70</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 0 "productsWeight" es igual a 0. [Gray zone]</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 0,
    &quot;productsWeight&quot;: 0
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-71</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 1 "productsWeight" es igual a 0.1.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 1,
    &quot;productsWeight&quot;: 0.1
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-72</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 4 "productsWeight" es igual a 1.5.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-73</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 7 "productsWeight" es igual a 2.9.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 7,
    &quot;productsWeight&quot;: 2.9
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-74</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 8 "productsWeight" es igual a 3.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 8,
    &quot;productsWeight&quot;: 3
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-75</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 9 "productsWeight" es igual a 3.1.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 9,
    &quot;productsWeight&quot;: 3.1
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-76</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 9 "productsWeight" es igual a 3.1.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 10,
    &quot;productsWeight&quot;: 3.2
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-77</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 9 "productsWeight" es igual a 3.1.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 12,
    &quot;productsWeight&quot;: 4.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-78</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 14 "productsWeight" es igual a 5.9.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 14,
    &quot;productsWeight&quot;: 5.9
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-79</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 15 "productsWeight" es igual a 6.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 15,
    &quot;productsWeight&quot;: 6
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-80</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 4 "productsWeight" es igual a 4.5.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 4.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-81</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 12 "productsWeight" es igual a 1.5.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 4.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-82</td>
        <td>El parámetro "toBeDeliveredTime" es igual a {"min": 20, "max": 25}, si los campos obligatorios in the request body tienes datos válidos.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 4.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Añadir in the request body los datos de la prueba.<br>
        4. Enviar la solicitud.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "toBeDeliveredTime": {<br>
        "min": 20,<br>
        "max": 25<br>
        }.</td>
        <td>- A el código de estado: 200 OK.<br>
        - "toBeDeliveredTime": {<br>
        "min": 20,<br>
        "max": 25<br>
        }.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
</tbody>
</table>

---

## Test Summary

### Status Distribution
- **🟢 PASSED**: Test cases that met all acceptance criteria
- **🔴 FAILED**: Test cases that encountered defects or unexpected behavior

### Test Coverage
- **Total Test Cases**: 82
- **Passed**: 41
- **Failed**: 41
- **Defects Identified**: 41 bugs logged in Jira

### API Endpoints Tested
1. **POST /api/v1/kits/:id/products** - Add products to a kit
2. **POST /order-and-go/v1/delivery** - Check delivery feasibility

### Notes
- All test cases use standard QA terminology and API testing conventions
- JSON request bodies are properly escaped for HTML rendering in GitHub
- Path parameters and request bodies are separated by `<br>` tags for clarity
- Bug links are hyperlinked to the corresponding Jira tickets
- Test data includes boundary value analysis and negative test scenarios

### Key Test Areas
1. **Positive Testing**: Adding existing products to existing kits
2. **Boundary Testing**: Kit product limits (min/max 30 unique products)
3. **Negative Testing**: Invalid product IDs, non-existent kits
4. **Input Validation**: Request body format, field types, required fields
5. **Business Logic**: Delivery time calculation, cost calculation, feasibility checks

---

*Generated for GitHub markdown table format with HTML structure*
*Bilingual Test Matrix - Spanish version also available*

