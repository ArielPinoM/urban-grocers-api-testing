# Test Case Matrix: "Order and Go" Delivery Module (`POST /order-and-go/v1/delivery`)

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
        <td>TC-OG-01</td>
        <td>A 200 OK status code is returned if the request body contains valid values in the required fields when verifying whether the order can be processed (Order and Go Delivery).</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Escribir la URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>- A 200 OK status code is returned.</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-OG-02</td>
        <td>When sending a valid request to the endpoint "/order-and-go/v1/delivery" it returns a response with the required parameters.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>- A response is returned with the following parameters:<br>
        - "name"<br>
        - "clientDeliveryCost"<br>
        - "toBeDeliveredTime"<br>
        - "hostDeliveryCost"<br>
        - "isItPossibleToDeliver"</td>
        <td>- A response is returned with the following parameters:<br>
        - "name"<br>
        - "clientDeliveryCost"<br>
        - "toBeDeliveredTime"<br>
        - "hostDeliveryCost"<br>
        - "isItPossibleToDeliver"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-OG-03</td>
        <td>A 400 Bad Request status code is returned when sending a request with the deliveryTime field as a string to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: &quot;string&quot;,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-25.md#br-25">BR-25</a></td>
    </tr>
    <tr>
        <td>TC-OG-04</td>
        <td>A 400 Bad Request status code is returned when sending a request with the deliveryTime field as a floating-point number to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15.1,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-26.md#br-26">BR-26</a></td>
    </tr>
    <tr>
        <td>TC-OG-05</td>
        <td>A 400 Bad Request status code is returned when sending a request with the deliveryTime field as a boolean to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: true,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-27.md#br-27">BR-27</a></td>
    </tr>
    <tr>
        <td>TC-OG-06</td>
        <td>A 400 Bad Request status code is returned when sending a request with the deliveryTime field as a null to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: null,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-28.md#br-28">BR-28</a></td>
    </tr>
    <tr>
        <td>TC-OG-07</td>
        <td>A 400 Bad Request status code is returned when sending a request with the deliveryTime field as an object to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: {},
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-29.md#br-29">BR-29</a></td>
    </tr>
    <tr>
        <td>TC-OG-08</td>
        <td>A 400 Bad Request status code is returned when sending a request with the deliveryTime field as an array to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: [],
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-30.md#br-30">BR-30</a></td>
    </tr>
    <tr>
        <td>TC-OG-09</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsCount field as a string to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: "string",
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-31.md#br-31">BR-31</a></td>
    </tr>
    <tr>
        <td>TC-OG-10</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsCount field as a floating-point number to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 1.1,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-32.md#br-32">BR-32</a></td>
    </tr>
    <tr>
        <td>TC-OG-11</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsCount field as a boolean to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: true,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-33.md#br-33">BR-33</a></td>
    </tr>
    <tr>
        <td>TC-OG-12</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsCount field as a null to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: null,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-34.md#br-34">BR-34</a></td>
    </tr>
    <tr>
        <td>TC-OG-13</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsCount field as an object to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: {},
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-35.md#br-35">BR-35</a></td>
    </tr>
    <tr>
        <td>TC-OG-14</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsCount field as an array to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: [],
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for integer: ..."</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-36.md#br-36">BR-36</a></td>
    </tr>
    <tr>
        <td>TC-OG-15</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsWeight field as a string to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: &quot;string&quot;
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-37.md#br-37">BR-37</a></td>
    </tr>
    <tr>
        <td>TC-OG-16</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsWeight field as a boolean to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: true
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-38.md#br-38">BR-38</a></td>
    </tr>
    <tr>
        <td>TC-OG-17</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsWeight field as a null to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: null
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-39.md#br-39">BR-39</a></td>
    </tr>
    <tr>
        <td>TC-OG-19</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsWeight field as an object to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: {}
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-40.md#br-40">BR-40</a></td>
    </tr>
    <tr>
        <td>TC-OG-19</td>
        <td>A 400 Bad Request status code is returned when sending a request with the productsWeight field as an array to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: []
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "invalid input syntax for number: ..."</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-41.md#br-41">BR-41</a></td>
    </tr>
    <tr>
        <td>TC-OG-20</td>
        <td>A 400 Bad Request status code is returned when sending a request without the deliveryTime field to the "/order-and-go/v1/delivery" endpoint.</td>
        <td>1. The warehouse system must be active.</td>
        <td><pre><code>{
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5 
}</code></pre></td>
        <td>1. Select the POST method.<br>
        2. Enter the server URL + /order-and-go/v1/delivery.<br>
        3. Add the test data to the request body.<br>
        4. Send the request.</td>
        <td>A 400 Bad Request status code is returned.<br>
        - "message": "deliveryTime is required".</td>
        <td>- A 200 OK status code is returned.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-42.md#br-42">BR-42</a></td>
    </tr>
    <tr>
    <td>TC-OG-21</td>
    <td>A 400 Bad Request status code is returned when sending a request omitting the productsCount field to the "/order-and-go/v1/delivery" endpoint.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 400 Bad Request status code is returned.<br>- "message": "productsCount is required".</td>
    <td>- A 200 OK status code is returned.</td>
    <td>🔴 FAILED</td>
    <td><a href="../../reports/bug-reports/br-43.md#BR-43">BR-43</a></td>
  </tr>
  <tr>
    <td>TC-OG-22</td>
    <td>A 400 Bad Request status code is returned when sending a request omitting the productsWeight field to the "/order-and-go/v1/delivery" endpoint.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 4
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 400 Bad Request status code is returned.<br>- "message": "productsWeight is required".</td>
    <td>- A 200 OK status code is returned.</td>
    <td>🔴 FAILED</td>
    <td><a href="../../reports/bug-reports/br-44.md#BR-44">BR-44</a></td>
  </tr>
  <tr>
    <td>TC-OG-23</td>
    <td>A 400 Bad Request status code is returned when omitting the request body to the "/order-and-go/v1/delivery" endpoint.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>The request body is omitted.</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Send the request.</td>
    <td>- A 400 Bad Request status code is returned.<br>- "message": "Request body is required".</td>
    <td>- A 200 OK status code is returned.</td>
    <td>🔴 FAILED</td>
    <td><a href="../../reports/bug-reports/br-45.md#BR-45">BR-45</a></td>
  </tr>
  <tr>
    <td>TC-OG-24</td>
    <td>A 400 Bad Request status code is returned when sending an unexpected field in the request body to the "/order-and-go/v1/delivery" endpoint.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 4,
    "productsWeight": 1.5,
    "extraParameter": "string"
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 400 Bad Request status code is returned.<br>- "message": "extraParameter is not allowed".</td>
    <td>- A 200 OK status code is returned.</td>
    <td>🔴 FAILED</td>
    <td><a href="../../reports/bug-reports/br-46.md#BR-46">BR-46</a></td>
  </tr>
  <tr>
    <td>TC-OG-25</td>
    <td>The "isItPossibleToDeliver" field in the response is "true" if "deliveryTime" = 8 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 8,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": true.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-26</td>
    <td>The "isItPossibleToDeliver" field in the response is "true" if "deliveryTime" = 9 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 9,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": true.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-27</td>
    <td>The "isItPossibleToDeliver" field in the response is "true" if "deliveryTime" = 15 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": true.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-28</td>
    <td>The "isItPossibleToDeliver" field in the response is "true" if "deliveryTime" = 21 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 21,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": true.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-29</td>
    <td>The "isItPossibleToDeliver" field in the response is "true" if "deliveryTime" = 22 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 22,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": true.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-30</td>
    <td>The "isItPossibleToDeliver" field in the response is "false" if "deliveryTime" = 3 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 3,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": false.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🔴 FAILED</td>
    <td><a href="../../reports/bug-reports/br-47.md#BR-47">BR-47</a></td>
  </tr>
  <tr>
    <td>TC-OG-31</td>
    <td>The "isItPossibleToDeliver" field in the response is "false" if "deliveryTime" = 6 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 6,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": false.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🔴 FAILED</td>
    <td><a href="../../reports/bug-reports/br-48.md#BR-48">BR-48</a></td>
  </tr>
  <tr>
    <td>TC-OG-32</td>
    <td>The "isItPossibleToDeliver" field in the response is "false" if "deliveryTime" = 7 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 7,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": false.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🔴 FAILED</td>
    <td><a href="../../reports/bug-reports/br-49.md#BR-49">BR-49</a></td>
  </tr>
  <tr>
    <td>TC-OG-33</td>
    <td>The "isItPossibleToDeliver" field in the response is "false" if "deliveryTime" = 23 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 23,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": false.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🔴 FAILED</td>
    <td><a href="../../reports/bug-reports/br-50.md#BR-50">BR-50</a></td>
  </tr>
  <tr>
    <td>TC-OG-34</td>
    <td>The "isItPossibleToDeliver" field in the response is "false" if "deliveryTime" = 0 and all other required fields contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 0,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "isItPossibleToDeliver": false.</td>
    <td>- A 200 OK status code is returned.
- "isItPossibleToDeliver": true.</td>
    <td>🔴 FAILED</td>
    <td><a href="../../reports/bug-reports/br-51.md#BR-51">BR-51</a></td>
  </tr>
  <tr>
    <td>TC-OG-35</td>
    <td>The "name" parameter in the response is equal to "Order and Go" when making a request with all required fields valid to the "/order-and-go/v1/delivery" endpoint.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "name": "Order and Go".</td>
    <td>- A 200 OK status code is returned.
- "name": "Order and Go".</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-36</td>
    <td>The "hostDeliveryCost" parameter equals 3 if "productsCount" equals 0 and "productsWeight" equals 0. [Gray area]</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 0,
    "productsWeight": 0
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 3.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 3.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-37</td>
    <td>The "hostDeliveryCost" parameter equals 3 if "productsCount" equals 1 and "productsWeight" equals 0.1.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 1,
    "productsWeight": 0.1
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 3.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 3.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-38</td>
    <td>The "hostDeliveryCost" parameter equals 3 if "productsCount" equals 4 and "productsWeight" equals 1.5.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 4,
    "productsWeight": 1.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 3.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 3.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-39</td>
    <td>The "hostDeliveryCost" parameter equals 3 if "productsCount" equals 7 and "productsWeight" equals 2.9.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 7,
    "productsWeight": 2.9
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 3.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 3.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-40</td>
    <td>The "hostDeliveryCost" parameter equals 3 if "productsCount" equals 8 and "productsWeight" equals 3.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 8,
    "productsWeight": 3
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 3.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 3.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-41</td>
    <td>The "hostDeliveryCost" parameter equals 5 if "productsCount" equals 9 and "productsWeight" equals 3.1.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 9,
    "productsWeight": 3.1
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 5.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 5.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-42</td>
    <td>The "hostDeliveryCost" parameter equals 5 if "productsCount" equals 10 and "productsWeight" equals 3.2.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 10,
    "productsWeight": 3.2
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 5.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 5.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-43</td>
    <td>The "hostDeliveryCost" parameter equals 5 if "productsCount" equals 12 and "productsWeight" equals 4.5.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 12,
    "productsWeight": 4.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 5.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 5.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-44</td>
    <td>The "hostDeliveryCost" parameter equals 5 if "productsCount" equals 14 and "productsWeight" equals 5.9.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 14,
    "productsWeight": 5.9
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 5.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 5.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-45</td>
    <td>The "hostDeliveryCost" parameter equals 5 if "productsCount" equals 15 and "productsWeight" equals 6.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 15,
    "productsWeight": 6
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 5.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 5.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-46</td>
    <td>The "hostDeliveryCost" parameter equals 5 if "productsCount" equals 4 and "productsWeight" equals 4.5.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 4,
    "productsWeight": 4.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 5.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 5.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-47</td>
    <td>The "hostDeliveryCost" parameter equals 5 if "productsCount" equals 12 and "productsWeight" equals 1.5.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 4,
    "productsWeight": 4.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "hostDeliveryCost": 5.</td>
    <td>- A 200 OK status code is returned.
- "hostDeliveryCost": 5.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
  <tr>
    <td>TC-OG-48</td>
    <td>The "toBeDeliveredTime" parameter equals {"min": 20, "max": 25}, if the required fields in the request body contain valid data.</td>
    <td>1. The warehouse system must be active.</td>
    <td><pre><code>{
    "deliveryTime": 15,
    "productsCount": 4,
    "productsWeight": 4.5
}</code></pre></td>
    <td>1. Select the POST method.<br>2. Enter the URL + /order-and-go/v1/delivery.<br>3. Add the test data to the request body.<br>4. Send the request.</td>
    <td>- A 200 OK status code is returned.<br>- "toBeDeliveredTime": {<br>   "min": 20,<br>   "max": 25<br>}.</td>
    <td>- A 200 OK status code is returned.
- "toBeDeliveredTime": {
   "min": 20,
   "max": 25
}.</td>
    <td>🟢 PASSED</td>
    <td></td>
  </tr>
</tr>
</tbody>
</table>



