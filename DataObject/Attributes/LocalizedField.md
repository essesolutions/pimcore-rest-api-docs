
`Version 2024.4.4.1`

Localized Field Configuration
-----

## Input Parameters
Parameters given in input while defining a localized field attribute. <br>

Required parameter <span style="color: red;">&#9733;</span>
<table style="width: 100%">
        <tr>
            <th>Parameter</th>
            <th>Parameter Type</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>Properties</td>
            <td>Children field definition<span style="color: red;">&#9733;</span><br>
             Each defined child has a title and a decription</td>
            <td><table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>title</td>
                    <td>string</td>
                    <td>The title or name of the child in a specific language</td>
                </tr>
                <tr>
                    <td>description</td>
                    <td>string</td>
                    <td>the description of the child in a specific language</td>
                </tr>
            </table>
        </tr>
        
   </table>

----------
#
## Output Parameters
Parameters received in output while retrieving a localized field attribute. <br>

Required parameter <span style="color: red;">&#9733;</span>
<table style="width: 100%">
        <tr>
            <th>Parameter</th>
            <th>Parameter Type</th>
            <th>Description</th>
        </tr>
        <tr>
            <td rowspan="2">Properties </td>
            <td>Children field definition<span style="color: red;">&#9733;</span><br>
             Each defined child has a title and a decription</td>
            <td><table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>title</td>
                    <td>string</td>
                    <td>The title or name of the child in a specific language</td>
                </tr>
                <tr>
                    <td>description</td>
                    <td>string</td>
                    <td>the description of the child in a specific language</td>
                </tr>
            </table>
        </tr>
       <tr>
       <td>Language</td>
       <td>The language version of data inside the localized field<br>
        (ex. en,it,de)</td>
       </tr>

   </table>

---------------
#
[Attribute Type Configuration](../DataObject.md#attribute-type-configuration-br)