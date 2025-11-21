
`Version 2024.4.4.1`

Field Collection Configuration
-----
## General
Field collections are defined using the same structural approach as standard objects. 
Each collection type is created with its own set of fields, data types, and validation rules, 
just like an object class. An object can contain multiple field collection items, 
including multiple instances of the same collection type, allowing for flexible and repeatable data structures.

## Input Parameters
Parameters given in input while defining a field collection attribute. <br>

Required parameter <span style="color: red;">&#9733;</span>
<table style="width: 100%">
        <tr>
            <th>Parameter</th>
            <th>Parameter Type</th>
            <th>Description</th>
            <th>Value</th>
        </tr>
        <tr>
            <td rowspan="4">Properties</td>
            <td>Field collection name<span style="color: red;">&#9733;</span></td>
            <td>The name of the field collection</td>
            <td>string</td>
        </tr>
        <tr>
            <td>Overwrite mode</td>
            <td>configuration setting mode used during data import or object update<br>
                ex.merge,preserve(default)</td>
            <td>string</td>
        </tr>
        <tr>
            <td>Identifiers</td>
            <td>Unique strings to distinguish individual field collection items within an object</td>
            <td>string</td>
        </tr>
       <tr>
            <td>Language</td>
            <td>Associates a  field collection entry with a particular language context<br>
              (ex.'en'.'it')</td>
            <td>string</td>
        </tr>
       
   </table>

----------
#
## Output Parameters
Parameters received in output while retrieving a field collection attribute. <br>

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
            <td>Field collection name<span style="color: red;">&#9733;</span></td>
            <td>The name of the field collection</td>
            <td>string</td>
        </tr>
        <tr>
            <td>type</td>
            <td>The type of the container field attribute in the object class</td>
            <td>string</td>
        </tr>
        <tr>
            <td>Items</td>
            <td>Individual instances of a defined field collection type that are added to an object</td>
            <td>field collection</td>
        </tr>
   </table>

---------------
#
[Attribute Type Configuration](../DataObject.md#attribute-type-configuration-br)