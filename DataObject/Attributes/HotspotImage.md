
`Version 2024.4.9.0`

Hotspot Image Configuration
-----

## Input Parameters
 Parameters given in input while defining a hotspot image attribute of an object. <br>

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
            <td> image<span style="color: red;">&#9733;</span></td>
            <td>The ID of the image asset to be used. </td>
            <td>integer (Asset ID)'</td>
        </tr>
         <tr>
            <td> crop</td>
            <td>Coordinates for a specific crop area. </td>
            <td>object (containing top, left, width, height)</td>
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
Parameters received in output while retrieving a hotspot image attribute of an object. <br>

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
            <td>type <span style="color: red;">&#9733;</span></td>
            <td>Type of the attribute</td>
            <td>string</td>
        </tr>
         <tr>
            <td> image<span style="color: red;">&#9733;</span></td>
            <td>The ID of the referenced asset. </td>
            <td>integer (Asset ID)'</td>
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

---------------
#
[Attribute Type Configuration](../DataObject.md#attribute-type-configuration-br)