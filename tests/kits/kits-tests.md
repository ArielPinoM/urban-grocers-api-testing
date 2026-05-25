# Test Case Matrix: Kit Management (`POST /api/v1/kits/:id/products`)

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
        <td>🟢 PASSED</td>
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
        <td><a href="../../reports/bug-reports/br-04.md#br-04">BR-04</a></td>
    </tr>
    <tr>
        <td>TC-KM-14</td>
        <td>A 400 Bad Request status code is returned if the "productsList" value in the request body is a string.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: &quot;string&quot;
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and productsList = "string" in the request body.</td>
        <td>- A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."</td>
        <td>- A 500 Internal Server Error status code is returned in the response.<br>
        - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-05.md#br-05">BR-05</a></td>
    </tr>
    <tr>
        <td>TC-KM-15</td>
        <td>A 400 Bad Request status code is returned if the "productsList" value in the request body is a boolean.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: true
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and productsList = true in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 500 Internal Server Error status code is returned in the response.
        <br>
        - "message": "productsList.forEach is not a function".
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-06.md#br-06">BR-06</a></td>
    </tr>
    <tr>
        <td>TC-KM-16</td>
        <td>A 400 Bad Request status code is returned if the "productsList" value in the request body is an object.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: {}
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and productsList = {} in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 500 Internal Server Error status code is returned in the response.
        <br>
        - "message": "productsList.forEach is not a function".
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-07.md#br-07">BR-07</a></td>
    </tr>
    <tr>
        <td>TC-KM-17</td>
        <td>A 400 Bad Request status code is returned if the "id" value is null and "quantity" is valid in the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = null and quantity = 1 in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 200 OK status code is returned in the response.
        <br>
        - The product is added to the kit.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-08.md#br-08">BR-08</a></td>
    </tr>
    <tr>
        <td>TC-KM-18</td>
        <td>A 400 Bad Request status code is returned if the "id" value is a string and "quantity" is valid in the request body.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
    {
        &quot;id&quot;: "string",
        &quot;quantity&quot;: 1
    }
  ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, id = "string" and quantity contains a valid value in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 500 Internal Server Error code is returned in the response.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-11.md#br-11">BR-11</a></td>
    </tr>
    <tr>
        <td>TC-KM-19</td>
        <td>A 400 Bad Request status code is returned if the "id" value is a floating-point number and "quantity" is valid in the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = 1.1 and quantity contains a valid value in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 500 Internal Server Error code is returned in the response.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-09.md#br-09">BR-09</a></td>
    </tr>
    <tr>
        <td>TC-KM-20</td>
        <td>A 400 Bad Request status code is returned if the "productsList" value is an empty array in the request body.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: []
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables and "productsList": [] in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 500 Internal Server Error code is returned in the response.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-10.md#br-10">BR-10</a></td>
    </tr>
    <tr>
        <td>TC-KM-21</td>
        <td>A 400 Bad Request status code is returned if the "id" value is a boolean and "quantity" is valid in the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = true and quantity contains a valid value in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 500 Internal Server Error code is returned in the response.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-12.md#br-12">BR-12</a></td>
    </tr>
    <tr>
        <td>TC-KM-22</td>
        <td>A 400 Bad Request status code is returned if the "id" value is a an object and "quantity" is valid in the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = {} and quantity contains a valid value in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 500 Internal Server Error code is returned in the response.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-13.md#br-13">BR-13</a></td>
    </tr>
    <tr>
        <td>TC-KM-23</td>
        <td>A 400 Bad Request status code is returned if the "id" value is a an empty array and "quantity" is valid in the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = [] and quantity contains a valid value in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 500 Internal Server Error code is returned in the response.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-14.md#br-14">BR-14</a></td>
    </tr>
    <tr>
        <td>TC-KM-24</td>
        <td>A 400 Bad Request status code is returned if the "id" value is valid and "quantity" is null the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = 1 and quantity = null in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for ..."
        </td>
        <td>
        - A 200 OK code is returned in the response.
        - The product is added to the kit.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-15.md#br-15">BR-15</a></td>
    </tr>
    <tr>
        <td>TC-KM-25</td>
        <td>A 400 Bad Request status code is returned if the "id" value is valid and "quantity" is a floating-point number in the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = 1 and quantity = 1.1 in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for type integer ..."<br>
        - The product is not added to the kit.
        </td>
        <td>
        - A 500 Internal Server Error code is returned in the response.<br>
        - "message": "invalid input syntax for type integer: \"1.1\""<br>
        - The product is not added to the kit.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-16.md#br-16">BR-16</a></td>
    </tr>
    <tr>
        <td>TC-KM-26</td>
        <td>A 400 Bad Request status code is returned if the "id" value is valid and "quantity" is a string in the request body.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: "string"
      }
   ]
}</code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, id = 1 and quantity = "string" in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for type integer ..."<br>
        - The product is not added to the kit.
        </td>
        <td>
        - A 500 Internal Server Error code is returned in the response.<br>
        - "message": "invalid input syntax for type integer: \"0string\""<br>
        - The product is not added to the kit.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-17.md#br-17">BR-17</a></td>
    </tr>
    <tr>
        <td>TC-KM-27</td>
        <td>A 400 Bad Request status code is returned if the "id" value is valid and "quantity" is a boolean in the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = 1 and quantity = true in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for type integer ..."<br>
        - The product is not added to the kit.
        </td>
        <td>
        - A 200 OK code is returned in the response.<br>
        - The product is added to the kit.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-18.md#br-18">BR-18</a></td>
    </tr>
    <tr>
        <td>TC-KM-28</td>
        <td>A 400 Bad Request status code is returned if the "id" value is valid and "quantity" is an object in the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = 1 and quantity = {} in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for type integer ..."<br>
        - The product is not added to the kit.
        </td>
        <td>
        - A 500 Internal Server Error code is returned in the response.<br>
        - "message": "invalid input syntax for type integer: \"0[object Object]\"".<br>
        - The product is not added to the kit.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-19.md#br-19">BR-19</a></td>
    </tr>
    <tr>
        <td>TC-KM-29</td>
        <td>A 400 Bad Request status code is returned if the "id" value is valid and "quantity" is an array in the request body.</td>
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
        2. Send a request using the "TestKit" id in Path Variables, id = 1 and quantity = [] in the request body.</td>
        <td>
        - A 400 Bad Request status code is returned in the response.<br>
        - "message": "invalid input syntax for type integer ..."<br>
        - The product is not added to the kit.
        </td>
        <td>
        - A 200 OK code is returned in the response.<br>
        - The product is added to the kit.
        </td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-20.md#br-20">BR-20</a></td>
    </tr>
    <tr>
        <td>TC-KM-30</td>
        <td>A 400 Bad Request status code is returned if the request body is empty while adding products to a kit.</td>
        <td>1. The warehouse system must be active.<br>
        2. Create a kit named "TestKit".<br>
        3. Search for the kit named "TestKit".<br>
        4. Copy the kit "id".</td>
        <td>Path params: id = "TestKit" id.<br><pre><code></code></pre></td>
        <td>1. Select the POST method and make a request to: URL + /api/v1/kits/:id/products<br>
        2. Send a request using the "TestKit" id in Path Variables, leave the request body empty.<br></td>
        <td>- A 400 Bad Request status code is returned in the response.<br>
        - "message": "Request body is required"</td>
        <td>- A 500 Internal Server Error status code is returned in the response.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-21.md#br-21">BR-21</a></td>
    </tr>
    <tr>
        <td>TC-KM-31</td>
        <td>A 400 Bad Request status code is returned if the product "id" is missing from the request body while adding products to a kit.</td>
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
        2. Send a request using the "TestKit" ID in the Path Variables, omit the "id" field, and include a valid "quantity" value in the request body.</td>
        <td>- A 400 Bad Request status code is returned in the response.<br>
        - "message": "id is required"</td>
        <td>- A 200 OK status code is returned in the response.<br>
        - The product is added to the kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-22.md#br-22">BR-22</a></td>
    </tr>
    <tr>
        <td>TC-KM-32</td>
        <td>A 400 Bad Request status code is returned if the product "quantity" is missing from the request body while adding products to a kit.</td>
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
        2. Send a request using the "TestKit" ID in the Path Variables, omit the "quantity" field, and include a valid "id" value in the request body.<br></td>
        <td>- A 400 Bad Request status code is returned in the response.<br>
        - "message": "quantity is required"</td>
        <td>- A 500 Internal Server Error status code is returned in the response.<br>
        - "message": "invalid input syntax for type integer: \"NaN\""</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-23.md#br-23">BR-23</a></td>
    </tr>
    <tr>
        <td>TC-KM-33</td>
        <td>A 400 Bad Request status code is returned if an unsupported key is sent in the request body while adding products to a kit.</td>
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
        2. Send a request using the "TestKit" ID in the Path Variables, including a valid product and the additional parameter "extraParameter": true in the request body.</td>
        <td>- A 400 Bad Request status code is returned in the response.<br>
        - "message": "extraParameter is not allowed"</td>
        <td>- A 200 OK status code is returned in the response.<br>
        - The product is added to the kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-24.md#br-24">BR-24</a></td>
    </tr>
    <tr>
        <td>TC-KM-34</td>
        <td>A 400 Bad Request status code is returned if the request body format is invalid in the api/v1/kits/:id/products endpoint.</td>
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
        2. Send a request using the "TestKit" ID in the Path Variables, including "id": 1 and "quantity": dos in the request body.</td>
        <td>- A 400 Bad Request status code is returned in the response.<br>
        - "message": "Unexpected token ... is not valid JSON"</td>
        <td>- A 400 Bad Request status code is returned in the response.<br>
        - "message": "Unexpected token ... is not valid JSON"</td>
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

