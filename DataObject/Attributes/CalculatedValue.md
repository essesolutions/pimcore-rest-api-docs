
`Version 2024.4.9.0`

Calculated Value Configuration
-----

## Input Parameters
 Parameters given in input while defining a calculated value attribute of an object.

Required parameter <span style="color: red;">&#9733;</span>
<table style="width: 100%">
        <tr>
            <th>Parameter</th>
            <th>Description</th>
            <th>Value</th>
        </tr>
        <tr>
            <td>name <span style="color: red;">&#9733;</span></td>
            <td>Name of the attribute</td>
            <td>string</td>
        </tr>
        <tr>
            <td> Calculator class<span style="color: red;">&#9733;</span></td>
            <td>The PHP class responsible for calculating the value</td>
            <td>string</td>
        </tr>
        <tr>
        <tr>
            <td> Calculator expression</td>
            <td>An optional expression used if the calculator class supports expression-based logic</td>
            <td>string</td>
        </tr>
        <tr>
            <td> Properties </td>
            <td>A list of custom properties associated with the attribute. Each property contains metadata such as name,type and value. </td>
            <td>
               <table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>name</td>
                    <td>string</td>
                    <td>The name of the property(ex. 'language').</td>
                </tr>
                <tr>
                    <td>type</td>
                    <td>string</td>
                    <td>The type of the property</td>
                </tr>
                <tr>
                    <td>value</td>
                    <td>string</td>
                    <td>The value of the property</td>
                </tr>
            </table>
            </td>
        </tr>
   </table>

----------
#

## Output Parameters
Parameters given in output while retrieving a calculated value attribute of an object.

Required parameter <span style="color: red;">&#9733;</span>
<table style="width: 100%">
        <tr>
            <th>Parameter</th>
            <th>Description</th>
            <th>Value</th>
        </tr>
        <tr>
            <td>name<span style="color: red;">&#9733;</span></td>
            <td>Name of the attribute</td>
            <td>string</td>
        </tr>
         <tr>
            <td>type<span style="color: red;">&#9733;</span></td>
            <td>Type of the attribute</td>
            <td>string</td>
        </tr>
        <tr>
            <td>value</td>
            <td>The resulting data returned by the PHP calculator class.</td>
            <td>mixed (can be string, number, or array)</td>
        </tr>
        <tr>
            <td> Properties </td>
            <td>A list of custom properties associated with the attribute. Each property contains metadata such as name,type and value. </td>
            <td>
               <table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>name</td>
                    <td>string</td>
                    <td>The name of the property(ex. 'language').</td>
                </tr>
                <tr>
                    <td>type</td>
                    <td>string</td>
                    <td>The type of the property</td>
                </tr>
                <tr>
                    <td>value</td>
                    <td>string</td>
                    <td>The value of the property</td>
                </tr>
            </table>
            </td>
        </tr>
   </table>

----------
#
[Attribute Type Configuration](../DataObject.md#attribute-type-configuration-br)