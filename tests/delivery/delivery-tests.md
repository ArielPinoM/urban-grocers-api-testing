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
        <td>TC-OG-45</td>
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
        <td>TC-OG-46</td>
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
        <td>TC-OG-47</td>
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
        <td>TC-OG-48</td>
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
        <td>TC-OG-49</td>
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
        <td>TC-OG-50</td>
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
        <td>TC-OG-51</td>
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
        <td>TC-OG-52</td>
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
        <td>TC-OG-53</td>
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
        <td>TC-OG-54</td>
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
        <td>TC-OG-55</td>
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
        <td>TC-OG-56</td>
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
        <td>TC-OG-57</td>
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
        <td>TC-OG-58</td>
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
        <td>TC-OG-59</td>
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
        <td>TC-OG-60</td>
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
        <td>TC-OG-61</td>
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
        <td>TC-OG-62</td>
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
        <td>TC-OG-63</td>
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
        <td>TC-OG-64</td>
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
        <td>TC-OG-65</td>
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
        <td>TC-OG-66</td>
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
        <td>TC-OG-67</td>
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
        <td>TC-OG-68</td>
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
        <td>TC-OG-69</td>
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
        <td>TC-OG-70</td>
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
        <td>TC-OG-71</td>
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
        <td>TC-OG-72</td>
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
        <td>TC-OG-73</td>
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
        <td>TC-OG-74</td>
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
        <td>TC-OG-75</td>
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
        <td>TC-OG-76</td>
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
        <td>TC-OG-77</td>
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
        <td>TC-OG-78</td>
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
        <td>TC-OG-79</td>
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
        <td>TC-OG-80</td>
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
        <td>TC-OG-81</td>
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
        <td>TC-OG-82</td>
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



