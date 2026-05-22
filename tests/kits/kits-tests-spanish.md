# Test Case Matrix - Kit Management API

## Project Information
**Sprint**: 4th Sprint  
**Module**: Kit Management (KM)  
**Endpoint**: `/api/v1/kits/:id/products`  
**Date Generated**: 2024  

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
        <td>Verificar que el usuario pueda añadir productos existentes a un kit.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td>Path params: id = 2<br><pre><code>{
  &quot;productsList&quot;: [
    {
      &quot;id&quot;: 1,
      &quot;quantity&quot;: 1
    }
  ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id:2 en las Path Variables y un ID de producto existente en el cuerpo de la solicitud.<br>
    3. Se añanden productos existentes al kit.<br>
    4. Se obtiene un código de estado: 200 OK en la respuesta.</td>
        <td>- Se añaden productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>- Se añaden productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-02</td>
        <td>Verificar que el kit pueda tener 1 producto único.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
    {
      &quot;id&quot;: 1,
      &quot;quantity&quot;: 1
    }
  ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y un ID de producto existente en el cuerpo de la solicitud.<br>
    3. Se añade el producto existente al kit.<br>
    4. Se obtiene un código de estado: 200 OK en la respuesta.</td>
        <td>- Se añaden productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>- Se añaden productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-03</td>
        <td>Verificar que el kit pueda tener 29 productos únicos.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
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
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y id's de productos existente en el cuerpo de la solicitud.<br>
    3. Se añaden los productos existentes al kit.<br>
    4. El usuario obtiene un código de estado: 200 OK en la respuesta.</td>
        <td>- Se añaden productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>- Se añaden productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-04</td>
        <td>Verificar que el kit pueda tener 30 productos únicos.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
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
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y id's de productos existente en el cuerpo de la solicitud.<br>
    3. Se añaden los productos existentes al kit.<br>
    4. Se obtiene un código de estado: 200 OK en la respuesta.</td>
        <td>- Se añaden productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>- Se añaden productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-05</td>
        <td>Verificar que el kit no pueda tener 31 productos únicos.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
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
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y id's de productos existente en el cuerpo de la solicitud.<br>
    3. No se añaden los productos existentes al kit.<br>
    4. Se obtiene un código de estado: 400 Bad Request en la respuesta con un mensaje de error "message": "No más de 30 artículos por conjunto" en la respuesta.</td>
        <td>- No se añaden los productos al kit.<br>
    - El estado de la solicitud es 400 Bad Request.<br>
    - "message": "No más de 30 artículos por conjunto"</td>
        <td>- No se añaden los productos al kit.<br>
    - El estado de la solicitud es 400 Bad Request.<br>
    - "message": "No más de 30 artículos por conjunto"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-06</td>
        <td>Verificar que el kit no pueda tener 32 productos únicos.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
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
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y id's de productos existente en el cuerpo de la solicitud.<br>
    3. No se añaden los productos existentes al kit.<br>
    4. Se obtiene un código de estado: 400 Bad Request en la respuesta con un mensaje de error "message": "No más de 30 artículos por conjunto" en la respuesta.</td>
        <td>- No se añaden los productos al kit.<br>
    - El estado de la solicitud es 400 Bad Request.<br>
    - "message": "No más de 30 artículos por conjunto"</td>
        <td>- No se añaden los productos al kit.<br>
    - El estado de la solicitud es 400 Bad Request.<br>
    - "message": "No más de 30 artículos por conjunto"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-07</td>
        <td>Verificar que el kit no pueda tener 33 productos únicos.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
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
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y id's de productos existente en el cuerpo de la solicitud.<br>
    3. No se añaden los productos existentes al kit.<br>
    4. Se obtiene un código de estado: 400 Bad Request en la respuesta con un mensaje de error "message": "No más de 30 artículos por conjunto" en la respuesta.</td>
        <td>- No se añaden los productos al kit.<br>
    - El estado de la solicitud es 400 Bad Request.<br>
    - "message": "No más de 30 artículos por conjunto"</td>
        <td>- No se añaden los productos al kit.<br>
    - El estado de la solicitud es 400 Bad Request.<br>
    - "message": "No más de 30 artículos por conjunto"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-08</td>
        <td>El conteo de productos de un kit puede ser mayor a 30 (productsCount > 30).</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
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
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y id's de productos existente en el cuerpo de la solicitud. La cantidad de productos totales son de 39.<br>
    3. Se añaden los productos existentes al kit "TestKit".<br>
    4. Se obtiene un código de estado: 200 OK en la respuesta.</td>
        <td>- Se añaden los productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>- Se añaden los productos existentes al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-09</td>
        <td>No se pueden agregar productos no existentes a un kit existente.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
    &quot;productsList&quot;: [
        {
            &quot;id&quot;: 93,
            &quot;quantity&quot;: 1
        }
    ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y un id del producto no existente en el cuerpo de la solicitud.<br>
    3. No se añade el producto no existente al kit "TestKit".<br>
    4. Se obtiene un código de estado: 404 Not Found en la respuesta.</td>
        <td>- No se añade el producto al kit.<br>
    - Se obtiene un código de estado: 404 Not Found en la respuesta.<br>
    - "message": "Not found".</td>
        <td>- Se añade el producto al kit.<br>
    - El estado de la solicitud es 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="../../reports/bug-reports/br-01.md#br-01">BR-01</a></td>
    </tr>
    <tr>
        <td>TC-KM-10</td>
        <td>No se pueden agregar productos existentes a un kit no existente.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td>Path params: id = 10<br><pre><code>{
    &quot;productsList&quot;: [
        {
            &quot;id&quot;: 1,
            &quot;quantity&quot;: 1
        }
    ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id: 10 en las Path Variables y un id de producto existente en el cuerpo de la solicitud.<br>
    3. No se añade el producto al kit no existente.<br>
    4. Se obtiene un código de estado: 404 Not Found en la respuesta.</td>
        <td>- No se añade el producto al kit no existente.<br>
    - Se obtiene un código de estado: 404 Not Found en la respuesta.<br>
    - "message": "Not found".</td>
        <td>- No se añade el producto al kit no existente.<br>
    - Se obtiene un código de estado: 404 Not Found en la respuesta.<br>
    - "message": "Not found".</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-11</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "productsList" es null.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: null
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y un productsList nulo en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-2?atlOrigin=eyJpIjoiZTMxN2U4NDk1ODQ4NDYzMDk5MjEzZGEwMGM4ZGE3YjYiLCJwIjoiaiJ9" target="_blank">BR-2</a></td>
    </tr>
    <tr>
        <td>TC-KM-12</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "productsList" es un número entero.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: 1
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y un productsList = 1 en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.<br>
    - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-3?atlOrigin=eyJpIjoiZmFhNmY1ODQzMWNjNGUwOGEyNDk1ZDQxZGQ4YTljYjUiLCJwIjoiaiJ9" target="_blank">BR-3</a></td>
    </tr>
    <tr>
        <td>TC-KM-13</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "productsList" es un número flotante.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: 1.1
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y un productsList = 1.1 en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.<br>
    - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-4?atlOrigin=eyJpIjoiODJjNjYyYzhlZWExNDM0Mjg2OGQwMzMwYTYyMjUwMDUiLCJwIjoiaiJ9" target="_blank">BR-4</a></td>
    </tr>
    <tr>
        <td>TC-KM-14</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "productsList" es un string.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: &quot;string&quot;
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y un productsList = "string" en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.<br>
    - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-5?atlOrigin=eyJpIjoiOTY5NDExMTc2YzA0NDE5N2E4Y2UyNzVhN2QxMWFlNTYiLCJwIjoiaiJ9" target="_blank">BR-5</a></td>
    </tr>
    <tr>
        <td>TC-KM-15</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "productsList" es un booleano.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: true
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y un productsList = true en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.<br>
    - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-6?atlOrigin=eyJpIjoiMjFiMzIzOWY1NDNjNGQyMGEwMzEwNDhkMWE4MmU3MDAiLCJwIjoiaiJ9" target="_blank">BR-6</a></td>
    </tr>
    <tr>
        <td>TC-KM-16</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "productsList" es un objeto.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: {}
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y un productsList = {} en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.<br>
    - "message": "productsList.forEach is not a function".</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-7?atlOrigin=eyJpIjoiM2JhYmYxY2IxYzgwNGZiZmJmOGJkZmE0NDcxZDIxZmIiLCJwIjoiaiJ9" target="_blank">BR-7</a></td>
    </tr>
    <tr>
        <td>TC-KM-17</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es null y "quantity" es válido.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: null,
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id = null y "quantity" válido en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 200 OK en la respuesta.<br>
    - Se añade el producto al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-8?atlOrigin=eyJpIjoiMDNhMDczZGU2YTE5NDQ2MjgxODQ4ODk4ODYyYTFlNWUiLCJwIjoiaiJ9" target="_blank">BR-8</a></td>
    </tr>
    <tr>
        <td>TC-KM-18</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es un número flotante y "quantity" es válido.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1.1,
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id = 1.1 y "quantity" válido en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-9?atlOrigin=eyJpIjoiODVmMGY5Njk4YjE2NGZkOGIwYjNkZDNmNDQzZDNkZWUiLCJwIjoiaiJ9" target="_blank">BR-9</a></td>
    </tr>
    <tr>
        <td>TC-KM-19</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es un string y "quantity" es válido.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: &quot;string&quot;,
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id = "string" y "quantity" válido en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-11?atlOrigin=eyJpIjoiNTA3NTg1ZTk2MWI5NDA0NDhmZGY5N2JiNWU1M2E3MzYiLCJwIjoiaiJ9" target="_blank">BR-11</a></td>
    </tr>
    <tr>
        <td>TC-KM-20</td>
        <td>Se obtiene un código de estado 500 Internal Server Error si en el cuerpo de la solicitud, el valor de "productsList" es un array vacío.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: []
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables y un "productsList" = [] en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-10?atlOrigin=eyJpIjoiYWEyMDRmZTg2OGQ0NGYyMjg4OWMwNTg4ODRjMmU3NmEiLCJwIjoiaiJ9" target="_blank">BR-10</a></td>
    </tr>
    <tr>
        <td>TC-KM-21</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es un booleano y "quantity" es válido.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: true,
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id = true y "quantity" válido en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-12?atlOrigin=eyJpIjoiNThjMDMwNTI4ZTU3NDBhN2FjNGYwOGM3NjJlNWFhYTAiLCJwIjoiaiJ9" target="_blank">BR-12</a></td>
    </tr>
    <tr>
        <td>TC-KM-22</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es un objeto y "quantity" es válido.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: {},
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id = {} y "quantity" válido en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-13?atlOrigin=eyJpIjoiMzM0MGM5N2RiYjVhNDFhZGJjY2FiNDUyM2E0MjVhNjgiLCJwIjoiaiJ9" target="_blank">BR-13</a></td>
    </tr>
    <tr>
        <td>TC-KM-23</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es un array y "quantity" es válido.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: [],
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id = [] y "quantity" válido en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-14?atlOrigin=eyJpIjoiN2Q0ZGI3NGQ0OGQ1NDZiNjlkYWVmMTcwNzhmOGFjYjMiLCJwIjoiaiJ9" target="_blank">BR-14</a></td>
    </tr>
    <tr>
        <td>TC-KM-24</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es válido y "quantity" es null.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: null
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id válido y "quantity" = null en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for ..."</td>
        <td>- Se obtiene un código de estado: 200 OK en la respuesta.<br>
    - Se añade el producto al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-15?atlOrigin=eyJpIjoiMjVlODYyODI0NGRhNDk2NDlkZWM2NGVjNzg0YmMxZDQiLCJwIjoiaiJ9" target="_blank">BR-15</a></td>
    </tr>
    <tr>
        <td>TC-KM-25</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es válido y "quantity" es un número flotante.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: 1.1
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id válido y "quantity" = 1.1 en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for type integer: ..."<br>
    - No se añade el producto al kit.</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.<br>
    - "message": "invalid input syntax for type integer: \"1.1\""<br>
    - No se añade el producto al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-16?atlOrigin=eyJpIjoiNDZhYjJiMjA3YTdiNDg1Njk4NzMzZmY5Mzg4OGQyMzMiLCJwIjoiaiJ9" target="_blank">BR-16</a></td>
    </tr>
    <tr>
        <td>TC-KM-26</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es válido y "quantity" es un string.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: &quot;string&quot;
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id válido y "quantity" = "string" en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for type integer: ..."<br>
    - No se añade el producto al kit.</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.<br>
    - "message": "invalid input syntax for type integer: \"0string\""<br>
    - No se añade el producto al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-17?atlOrigin=eyJpIjoiYzViMDdkYWVjM2FlNDQzYjhlYzMyOGQxODE3Nzc4ZmYiLCJwIjoiaiJ9" target="_blank">BR-17</a></td>
    </tr>
    <tr>
        <td>TC-KM-27</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es válido y "quantity" es un booleano.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: true
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id válido y "quantity" = true en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for type integer: ..."<br>
    - No se añade el producto al kit.</td>
        <td>- Se obtiene el código de estado: 200 OK en la respuesta.<br>
    - Se añade el producto al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-18?atlOrigin=eyJpIjoiNGRhNWJlNDZlOTE0NDBkN2JiMjU2ZDExZjVmMzg0YWEiLCJwIjoiaiJ9" target="_blank">BR-18</a></td>
    </tr>
    <tr>
        <td>TC-KM-28</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es válido y "quantity" es un objeto.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: {}
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id válido y "quantity" = {} en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for type integer: ..."<br>
    - No se añade el producto al kit.</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.<br>
    - "message": "invalid input syntax for type integer: \"0[object Object]\""<br>
    - No se añade el producto al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-19?atlOrigin=eyJpIjoiNWNkZTA2M2MyODc0NDliNGFmMjA4NWU4YmEzMGM1M2QiLCJwIjoiaiJ9" target="_blank">BR-19</a></td>
    </tr>
    <tr>
        <td>TC-KM-29</td>
        <td>Se obtiene un código de estado 400 Bad Request si en el cuerpo de la solicitud, el valor de "id" es válido y "quantity" es un array.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
  &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: []
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, un id válido y "quantity" = [] en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "invalid input syntax for type integer: ..."<br>
    - No se añade el producto al kit.</td>
        <td>- Se obtiene el código de estado: 200 OK en la respuesta.<br>
    - Se añade el producto al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-20?atlOrigin=eyJpIjoiZDAwMTljMjY1OWQ3NDAyMDk2NTdiMjRmMjM2MGYxYWUiLCJwIjoiaiJ9" target="_blank">BR-20</a></td>
    </tr>
    <tr>
        <td>TC-KM-30</td>
        <td>Se obtiene un código de estado 400 Bad Request si no se completa el cuerpo de la solicitud al añadir productos al kit.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code></code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, se deja vacío el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "Request body is required"</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-21?atlOrigin=eyJpIjoiOGY5ZTExYTM4NDNjNDI1Y2I5MTUzNjAzZGUzZmQ4MzUiLCJwIjoiaiJ9" target="_blank">BR-21</a></td>
    </tr>
    <tr>
        <td>TC-KM-31</td>
        <td>Se obtiene un código de estado 400 Bad Request si no está presente el "id" del producto en el cuerpo de la solicitud al añadir productos al kit.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
   &quot;productsList&quot;: [
      {
         &quot;quantity&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, no escribir el "id" y agregar "quantity" válido en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "id is required"</td>
        <td>- Se obtiene un código de estado: 200 OK en la respuesta.<br>
    - Se añade el producto al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-22?atlOrigin=eyJpIjoiMzc2ZjM2YWUxODE1NDIwMThkOWU0ZDFhNzExYjA4NTQiLCJwIjoiaiJ9" target="_blank">BR-22</a></td>
    </tr>
    <tr>
        <td>TC-KM-32</td>
        <td>Se obtiene un código de estado 400 Bad Request si no está presente "quantity" del producto en el cuerpo de la solicitud al añadir productos al kit.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
   &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, no escribir "quantity" y agregar un "id" válido en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "quantity is required"</td>
        <td>- Se obtiene un código de estado: 500 Internal Server Error en la respuesta.<br>
    - "message": "invalid input syntax for type integer: \"NaN\""</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-23?atlOrigin=eyJpIjoiZmI0MjQwMjkxYWM0NDdlNjg3MmQzNmQwZDU2YWZlMjgiLCJwIjoiaiJ9" target="_blank">BR-23</a></td>
    </tr>
    <tr>
        <td>TC-KM-33</td>
        <td>Se obtiene un código de estado 400 Bad Request si se envía una clave diferente a las requeridas en el cuerpo de la solicitud al añadir productos al kit.</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
   &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: 1,
         &quot;extraParameter&quot;: true
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, se escribe un producto válido más el parámetro extra "extraParameter": true en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "extraParameter is not allowed"</td>
        <td>- Se obtiene el código de estado: 200 OK en la respuesta.<br>
    - Se añade el producto al kit.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-24?atlOrigin=eyJpIjoiODNmZDlmYWI1NDc3NGE2M2ExOTcwNzcxMDY0MzYzZDYiLCJwIjoiaiJ9" target="_blank">BR-24</a></td>
    </tr>
    <tr>
        <td>TC-KM-34</td>
        <td>Se obtiene un código de estado 400 Bad Request si el formato del cuerpo de la solicitud es incorrecto en el endpoint "api/v1/kits/:id/products".</td>
        <td>1. El sistema de almacén debe estar activo.<br>
    2. Crear un kit con el nombre "TestKit".<br>
    3. Buscar el kit con el nombre "TestKit".<br>
    4. Copiar el "id" del kit.</td>
        <td>Path params: id = id del kit "TestKit".<br><pre><code>{
   &quot;productsList&quot;: [
      {
         &quot;id&quot;: 1,
         &quot;quantity&quot;: dos
      }
   ]
}</code></pre></td>
        <td>1. Seleccionar el método POST y hacer una solicitud a: URL + api/v1/kits/:id/products<br>
    2. Enviar una petición usando el id del "TestKit" en las Path Variables, se escribe "id":1 y "quantity": dos en el cuerpo de la solicitud.<br>
    3. Se obtiene un código de estado: 400 Bad Request en la respuesta.</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "Unexpected token ... is not valid JSON"</td>
        <td>- Se obtiene un código de estado: 400 Bad Request en la respuesta.<br>
    - "message": "Unexpected token ... is not valid JSON"</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-35</td>
        <td>Se obtiene 200 OK si el cuerpo de la solicitud incluye valores válidos en los campos obligatorios al verificar si el pedido se puede hacer (Entrega: Order and Go).</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-36</td>
        <td>Al enviar una solicitud válida al endpoint "/order-and-go/v1/delivery" se obtiene una respuesta con los parámetros obligatorios.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene una respuesta con los siguientes parámetros:<br>
    - "name"<br>
    - "clientDeliveryCost"<br>
    - "toBeDeliveredTime"<br>
    - "hostDeliveryCost"<br>
    - "isItPossibleToDeliver"</td>
        <td>- Se obtiene una respuesta con los siguientes parámetros:<br>
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
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo string al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: &quot;string&quot;,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-25?atlOrigin=eyJpIjoiMmFjNjY1YjM0MjI4NDRjNGIxZjYyMGQyYzczNDhjMDUiLCJwIjoiaiJ9" target="_blank">BR-25</a></td>
    </tr>
    <tr>
        <td>TC-KM-38</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo flotante al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15.1,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-26?atlOrigin=eyJpIjoiMjE4NDFlM2ZlZjI0NGM4ZGJkOWFlMGJiNDRiMDUzNmEiLCJwIjoiaiJ9" target="_blank">BR-26</a></td>
    </tr>
    <tr>
        <td>TC-KM-39</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo booleano al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: true,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-27?atlOrigin=eyJpIjoiOWQ1MmVkMTAxYjdjNDNkOGJhMTNmN2MyNzI3NWYxODAiLCJwIjoiaiJ9" target="_blank">BR-27</a></td>
    </tr>
    <tr>
        <td>TC-KM-40</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime = null al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: null,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-28?atlOrigin=eyJpIjoiMjVhZDkwODc4NDU2NGQ0OWE4YTA3ZTE2NjQyMmI0N2MiLCJwIjoiaiJ9" target="_blank">BR-28</a></td>
    </tr>
    <tr>
        <td>TC-KM-41</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo objeto al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: {},
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-29?atlOrigin=eyJpIjoiZDU3M2I5MDE4OThkNDgzOTgwMTE1ZjdjMjc5OWIzYjUiLCJwIjoiaiJ9" target="_blank">BR-29</a></td>
    </tr>
    <tr>
        <td>TC-KM-42</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo deliveryTime tipo array al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: [],
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-30?atlOrigin=eyJpIjoiYjM3MzRjOWI1MDYwNGE3OGFhNDkyYmE1OGQwYjc4NDQiLCJwIjoiaiJ9" target="_blank">BR-30</a></td>
    </tr>
    <tr>
        <td>TC-KM-43</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo string al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: &quot;string&quot;,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-31?atlOrigin=eyJpIjoiNzRmNjkyMDcyODkwNDNkM2IxNmRiZTEyZjk5ZWIzNWQiLCJwIjoiaiJ9" target="_blank">BR-31</a></td>
    </tr>
    <tr>
        <td>TC-KM-44</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo flotante al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 1.1,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-32?atlOrigin=eyJpIjoiNTFmMjU5YzM2NDU3NDM3NDg0ZGQ0NTczNWMwNWRiZGQiLCJwIjoiaiJ9" target="_blank">BR-32</a></td>
    </tr>
    <tr>
        <td>TC-KM-45</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo booleano al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: true,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-33?atlOrigin=eyJpIjoiZTdkOGNmZTFlMzQ5NGY2NGI4MDE0M2E0MmM5MjI5NWMiLCJwIjoiaiJ9" target="_blank">BR-33</a></td>
    </tr>
    <tr>
        <td>TC-KM-46</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsCount = null al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: null,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-34?atlOrigin=eyJpIjoiZDgyODlkYWE0MWFkNGQyZGFmMzczZDU1OTEwMzMzOTgiLCJwIjoiaiJ9" target="_blank">BR-34</a></td>
    </tr>
    <tr>
        <td>TC-KM-47</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo objeto al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: {},
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-35?atlOrigin=eyJpIjoiYjY4YzVkOWIwZWE0NDA2ZWFlZmQwOTQ1MDYyNzcwN2UiLCJwIjoiaiJ9" target="_blank">BR-35</a></td>
    </tr>
    <tr>
        <td>TC-KM-48</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsCount tipo array al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: [],
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for integer: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-36?atlOrigin=eyJpIjoiZDUxMThkOWQ4YTE1NGQ2ZjliZWUwMGRmOGFjZjljODciLCJwIjoiaiJ9" target="_blank">BR-36</a></td>
    </tr>
    <tr>
        <td>TC-KM-49</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsWeight tipo string al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: &quot;string&quot;
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for number: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-37?atlOrigin=eyJpIjoiZTkxNTNlYzA2MzAyNDY4MTg1YTM0YjBhZDkxMmY4ZGIiLCJwIjoiaiJ9" target="_blank">BR-37</a></td>
    </tr>
    <tr>
        <td>TC-KM-50</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsWeight tipo booleano al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: true
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for number: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-38?atlOrigin=eyJpIjoiZWUyY2JhZWRiM2FkNGM5NzlkOWJjMDkwNDhmNTI3NzAiLCJwIjoiaiJ9" target="_blank">BR-38</a></td>
    </tr>
    <tr>
        <td>TC-KM-51</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsWeight = null al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: null
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for number: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-39?atlOrigin=eyJpIjoiYjkwM2I2MDJiYzE3NDBlZDgzYzJiOTRkMGY4MmQwYjAiLCJwIjoiaiJ9" target="_blank">BR-39</a></td>
    </tr>
    <tr>
        <td>TC-KM-52</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsWeight tipo objeto al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: {}
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for number: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-40?atlOrigin=eyJpIjoiMTAxM2Q4YzdhNDU0NDZhODg2ODlkYjQ4YTI4Nzk4ZjgiLCJwIjoiaiJ9" target="_blank">BR-40</a></td>
    </tr>
    <tr>
        <td>TC-KM-53</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud con el valor del campo productsWeight tipo array al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: []
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "invalid input syntax for number: ..."</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-41?atlOrigin=eyJpIjoiNGQzNTIwOTQ2Njg5NDU1M2IwYTU3ODVhOWUxMTc2MjEiLCJwIjoiaiJ9" target="_blank">BR-41</a></td>
    </tr>
    <tr>
        <td>TC-KM-54</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud omitiendo el campo deliveryTime al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5 
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "deliveryTime is required".</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-42?atlOrigin=eyJpIjoiMGUyYzlmNmRlNmU1NDgzMjkxYzg4NWViYjYyZjdmMjYiLCJwIjoiaiJ9" target="_blank">BR-42</a></td>
    </tr>
    <tr>
        <td>TC-KM-55</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud omitiendo el campo productsCount al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsWeight&quot;: 1.5 
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "productsCount is required".</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-43?atlOrigin=eyJpIjoiM2JkNTI4NzY0MGZjNDc1NWJiMDg0MzIxYjEwY2Q3ZmUiLCJwIjoiaiJ9" target="_blank">BR-43</a></td>
    </tr>
    <tr>
        <td>TC-KM-56</td>
        <td>Se obtiene 400 Bad Request al enviar la solicitud omitiendo el campo productsWeight al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4 
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "productsWeight is required".</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-44?atlOrigin=eyJpIjoiMmJlNDA5MjAxNTQ0NDc3Zjk0YjIxMzAxNzNhYjEwMDkiLCJwIjoiaiJ9" target="_blank">BR-44</a></td>
    </tr>
    <tr>
        <td>TC-KM-57</td>
        <td>Se obtiene 400 Bad Request al omitir el cuerpo de la solicitud al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>Se omite el cuerpo de la solicitud.</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "Request body is required".</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-45?atlOrigin=eyJpIjoiZTczY2VhMTM4OTI2NDU2ZWE2YjA1ZWJlNDBlM2FhM2QiLCJwIjoiaiJ9" target="_blank">BR-45</a></td>
    </tr>
    <tr>
        <td>TC-KM-58</td>
        <td>Se obtiene 400 Bad Request al enviar un campo no esperado en el cuerpo de la solicitud al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5,
    &quot;extraParameter&quot;: &quot;string&quot;
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 400 Bad Request.<br>
    - "message": "extraParameter is not allowed".</td>
        <td>- Se obtiene el código de estado: 200 OK.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-46?atlOrigin=eyJpIjoiNTI2YmM5MGYxZjQ5NGUxNGE2NDBkNzlmNTQ2YzAyNTEiLCJwIjoiaiJ9" target="_blank">BR-46</a></td>
    </tr>
    <tr>
        <td>TC-KM-59</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "true" si "deliveryTime" = 8 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 8,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-60</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "true" si "deliveryTime" = 9 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 9,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-61</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "true" si "deliveryTime" = 15 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-62</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "true" si "deliveryTime" = 21 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 21,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-63</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "true" si "deliveryTime" = 22 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 22,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-64</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "false" si "deliveryTime" = 3 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 3,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": false.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-47?atlOrigin=eyJpIjoiM2U0NDdjNzAyYjJiNGU1OWIyOTlmNDVlMDIyMjNlMmIiLCJwIjoiaiJ9" target="_blank">BR-47</a></td>
    </tr>
    <tr>
        <td>TC-KM-65</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "false" si "deliveryTime" = 6 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 6,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": false.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-48?atlOrigin=eyJpIjoiYTA5OGYyYmM1ZTdjNGZiZDg5N2E1ZjVlZDg2ZGE1NTIiLCJwIjoiaiJ9" target="_blank">BR-48</a></td>
    </tr>
    <tr>
        <td>TC-KM-66</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "false" si "deliveryTime" = 7 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 7,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": false.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-49?atlOrigin=eyJpIjoiYjc2NGVkMGNiZTU5NDA0Njg5MGI2YzFhNmRjYWYwMzkiLCJwIjoiaiJ9" target="_blank">BR-49</a></td>
    </tr>
    <tr>
        <td>TC-KM-67</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "false" si "deliveryTime" = 23 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 23,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": false.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-50?atlOrigin=eyJpIjoiZmY0OTQ5NzhkMDU5NDVjM2FlYWYzMDUwZGRjYWY3NmUiLCJwIjoiaiJ9" target="_blank">BR-50</a></td>
    </tr>
    <tr>
        <td>TC-KM-68</td>
        <td>El campo "isItPossibleToDeliver" en la respuesta es "false" si "deliveryTime" = 0 y el resto de los campos obligatorios contienen datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 0,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": false.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "isItPossibleToDeliver": true.</td>
        <td>🔴 FAILED</td>
        <td><a href="https://arielpinom96.atlassian.net/browse/BR-51?atlOrigin=eyJpIjoiZmMwMjE0NTEzYjAxNDg3ZGE1NmZjZDY2ZTVjMjgyODkiLCJwIjoiaiJ9" target="_blank">BR-51</a></td>
    </tr>
    <tr>
        <td>TC-KM-69</td>
        <td>El parámetro "name" en la respuesta es igual a "Order and Go" al realizar una solicitud con todos los campos obligatorios válidos al endpoint "/order-and-go/v1/delivery".</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "name": "Order and Go".</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "name": "Order and Go".</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-70</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 0 y "productsWeight" es igual a 0. [Zona gris]</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 0,
    &quot;productsWeight&quot;: 0
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-71</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 1 y "productsWeight" es igual a 0.1.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 1,
    &quot;productsWeight&quot;: 0.1
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-72</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 4 y "productsWeight" es igual a 1.5.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 1.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-73</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 7 y "productsWeight" es igual a 2.9.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 7,
    &quot;productsWeight&quot;: 2.9
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-74</td>
        <td>El parámetro "hostDeliveryCost" es igual a 3 si "productsCount" es igual a 8 y "productsWeight" es igual a 3.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 8,
    &quot;productsWeight&quot;: 3
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 3.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-75</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 9 y "productsWeight" es igual a 3.1.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 9,
    &quot;productsWeight&quot;: 3.1
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-76</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 9 y "productsWeight" es igual a 3.1.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 10,
    &quot;productsWeight&quot;: 3.2
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-77</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 9 y "productsWeight" es igual a 3.1.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 12,
    &quot;productsWeight&quot;: 4.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-78</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 14 y "productsWeight" es igual a 5.9.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 14,
    &quot;productsWeight&quot;: 5.9
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-79</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 15 y "productsWeight" es igual a 6.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 15,
    &quot;productsWeight&quot;: 6
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-80</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 4 y "productsWeight" es igual a 4.5.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 4.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-81</td>
        <td>El parámetro "hostDeliveryCost" es igual a 5 si "productsCount" es igual a 12 y "productsWeight" es igual a 1.5.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 4.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "hostDeliveryCost": 5.</td>
        <td>🟢 PASSED</td>
        <td></td>
    </tr>
    <tr>
        <td>TC-KM-82</td>
        <td>El parámetro "toBeDeliveredTime" es igual a {"min": 20, "max": 25}, si los campos obligatorios en el cuerpo de la solicitud tienes datos válidos.</td>
        <td>1. El sistema de almacén debe estar activo.</td>
        <td><pre><code>{
    &quot;deliveryTime&quot;: 15,
    &quot;productsCount&quot;: 4,
    &quot;productsWeight&quot;: 4.5
}</code></pre></td>
        <td>1. Seleccionar el método POST.<br>
    2. Escribir la URL + /order-and-go/v1/delivery.<br>
    3. Añadir en el cuerpo de la solicitud los datos de la prueba.<br>
    4. Enviar la solicitud.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
    - "toBeDeliveredTime": {<br>
    "min": 20,<br>
    "max": 25<br>
    }.</td>
        <td>- Se obtiene el código de estado: 200 OK.<br>
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
- **🟢 PASSED**: Tests that met all acceptance criteria
- **🔴 FAILED**: Tests that encountered defects or unexpected behavior

### Notes
- All test cases are related to API endpoint testing for the Kit Management system
- JSON request bodies are properly escaped for HTML rendering
- Path parameters and request bodies are separated by `<br>` tags for clarity
- Bug links are hyperlinked to the corresponding Jira tickets

---

*Generated for GitHub markdown table format with HTML structure*