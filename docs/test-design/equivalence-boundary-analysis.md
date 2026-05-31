# Equivalence Classes and Boundary Value Analysis

<table>
    <thead>
        <tr>
            <th>Test Group</th>
            <th>Class Name</th>
            <th>Bounds</th>
            <th>Test Data Inside Class (Field Content)</th>
            <th>Boundary Test Data (Field Content)</th>
        </tr>
    </thead>
    <tbody>
        <!-- Product identifiers in a kit -->
        <tr>
            <td rowspan = 3>Product identifiers in a kit</td>
            <td>30 unique products</td>
            <td>30</td>
            <td>1 — id: 1</td>
            <td>L: 30 — id: 1-30<br>L - 1: 29 — id: 1-29</td>
        </tr>
        <tr>
            <td>31 unique products and above</td>
            <td>31</td>
            <td>33 — id: 1-33</td>
            <td>L: 31 — id: 1-31<br>L + 1: 32 — id: 1-32</td>
        </tr>
        <tr>
            <td>No products [id: null]</td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <!-- Order and Go: deliveryTime -->
        <tr>
            <td rowspan = 2>Order and Go — `deliveryTime`</td>
            <td>Operating hours 08:00–22:00</td>
            <td>8, 22</td>
            <td>15</td>
            <td>Lower: 8<br>Upper: 22<br>Lower+1: 9<br>Upper-1: 21</td>
        </tr>
        <tr>
            <td>Operating hours 23:00–07:00</td>
            <td>23, 7</td>
            <td>3</td>
            <td>Lower: 23<br>Upper: 7 (next day)<br>Lower+1: 0<br>Upper-1: 6</td>
        </tr>
        <!-- Order and Go: productsCount -->
        <tr>
            <td rowspan = 3>Order and Go — `productsCount`</td>
            <td>0 to 8 items per order</td>
            <td>0, 8</td>
            <td>4</td>
            <td>Lower: 0<br>Upper: 8<br>Lower+1: 1<br>Upper-1: 7</td>
        </tr>
        <tr>
            <td>9 to 15 items per order</td>
            <td>9, 15</td>
            <td>12</td>
            <td>Lower: 9<br>Upper: 15<br>Lower+1: 10<br>Upper-1: 14</td>
        </tr>
        <tr>
            <td>16 items per order and above</td>
            <td>16</td>
            <td>18</td>
            <td>Lower: 16<br>Lower+1: 17</td>
        </tr>
        <!-- Order and Go: productsWeight -->
        <tr>
            <td rowspan = 3>Order and Go — `productsWeight`</td>
            <td>Order weight: 0.0 kg to 3.0 kg</td>
            <td>0.0, 3.0</td>
            <td>1.5</td>
            <td>Lower: 0.0<br>Upper: 3.0<br>Lower+0.1: 0.1<br>Upper-0.1: 2.9</td>
        </tr>
        <tr>
            <td>Order weight: 3.1 kg to 6.0 kg</td>
            <td>3.1, 6.0</td>
            <td>4.5</td>
            <td>Lower: 3.1<br>Upper: 6.0<br>Lower+0.1: 3.2<br>Upper-0.1: 5.9</td>
        </tr>
        <tr>
            <td>Order weight: 6.1 kg and above</td>
            <td>6.1</td>
            <td>7</td>
            <td>Lower: 6.1<br>Lower+0.1: 6.2</td>
        </tr>
    </tbody>
</table>
