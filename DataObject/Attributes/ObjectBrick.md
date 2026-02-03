
`Version 2024.4.9.0`

Object Brick Configuration
-----
## General
Object bricks are defined using the same structural approach as standard objects. 
Each brick is created with its own set of fields, data types, and validation rules, 
just like an object class.An object can contain multiple object bricks, 
but only one instance of each brick type may be assigned.

## Input Parameters
Parameters given in input while defining an object brick attribute. <br>

Required parameter <span style="color: red;">&#9733;</span>
<table style="width: 100%">
        <tr>
            <th>Parameter</th>
            <th>Parameter Type</th>
            <th>Description</th>
            <th>Value</th>
        </tr>
        <tr>
            <td rowspan="2">Properties</td>
            <td>Container name<span style="color: red;">&#9733;</span></td>
            <td>The name of the container field attribute in the object class</td>
            <td>string</td>
        </tr>
        <tr>
            <td>Object brick name<span style="color: red;">&#9733;</span></td>
            <td>Unique name of the object brick</td>
            <td>string</td>
        </tr>
   </table>

----------
#
## Output Parameters
Parameters received in output while retrieving an object brick attribute. <br>

Required parameter <span style="color: red;">&#9733;</span>
<table style="width: 100%">
        <tr>
            <th>Parameter</th>
            <th>Parameter Type</th>
            <th>Description</th>
            <th>Value</th>
        </tr>
        <tr>
            <td rowspan="3">Properties</td>
            <td>Container name<span style="color: red;">&#9733;</span></td>
            <td>The name of the container field attribute in the object class</td>
            <td>string</td>
        </tr>
        <tr>
            <td>Container type<span style="color: red;">&#9733;</span></td>
            <td>The type of the container field attribute in the object class</td>
            <td>string</td>
        </tr>
        <tr>
            <td>Object brick name<span style="color: red;">&#9733;</span></td>
            <td>Unique name of the object brick</td>
            <td>string</td>
        </tr>
   </table>

---------------
#
[Attribute Type Configuration](../DataObject.md#attribute-type-configuration-br)