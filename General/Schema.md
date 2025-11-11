
<table style="width: 100%">
        <tr>
            <th>Parameter</th>
            <th>Description</th>
            <th>Value</th>
        </tr>
        <tr>
            <td>page</td>
            <td>The collection page number</td>
            <td>integer(>0)</td>
        </tr>
        <tr>
            <td> path</td>
            <td>The path where the collection is stored</td>
            <td>string</td>
        </tr>
        <tr>
            <td> type </td>
            <td>The asset ype used to filter the collection.Multiple values can be inserted seperated by a comma <br>
              (Example: image,document)</td>
            <td>string or null</td>
        </tr>
       <tr>
            <td>query</td>
            <td>The PQL query(Pimcore Query Language Syntax) used to filter the returned collection </td>
            <td>query</td>
        </tr>
        <tr>
            <td>creationDate</td>
            <td>The timestamp when the asset was first created</td>
            <td>string or null</td>
        </tr>
        <tr>
            <td>modificationDate</td>
            <td>The timestamp of the most recent modification to the asset</td>
            <td>string or null</td>
        </tr>
         <tr>
            <td>content</td>
            <td>Raw content or data of the asset.</td>
            <td>string or null</td>
        </tr>
        <tr>
            <td>fileSize</td>
            <td>The size of the file in bytes</td>
            <td>integer</td>
        </tr>
         <tr>
            <td>properties  <span style="color: red;">&#9733;</span></td>
            <td>A list of custom properties associated with the asset. Each property contains metadata such as name, type, and value.</td>
            <td>integer</td>
        </tr>
        <tr>
            <td>metadata</td>
            <td>A list of metadata records related to the asset. Each record contains information such as asset ID, name, language, type of data, and the value of the metadata.</td>
            <td>string</td>
        </tr>
        <tr>
            <td>fullPath</td>
            <td>The absolute path to the file which includes the full directory and filename</td>
            <td>string</td>
        </tr>
        <tr>
            <td>formatedFileSize</td>
            <td>TA human-readable version of the file size, formatted for easier interpretation.</td>
            <td>string</td>
        </tr>
    </table>

#
#
#
#
#
#

<table style="width: 100%">
    <tr>
        <th>Parameter</th>
        <th>Description</th>
        <th>Value</th>
    </tr>
    <tr>
        <td> id</td>
        <td>The identifier of the retrieved object</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>key</td>
        <td>A key or code associated with the object</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>path</td>
        <td>The full hierarchical path to the object within the system</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>classId</td>
        <td>Identifier of the object's class or category</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>className </td>
        <td>Human-readable name of the class the object belongs to.</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>type<span style="color: red;">&#9733;</span> </td>
        <td>The object type, which could define its behavior or structure</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>parents </td>
        <td>Contains metadata about the parent object.If the object is at the root level, this may be null or default values.</td>
        <td>
            <table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>parent.id</td>
                    <td>interger,null or string</td>
                    <td>Unique identifier of the parent object.</td>
                </tr>
                <tr>
                    <td>parent.type<span style="color: red;">&#9733;</span></td>
                    <td>string or null</td>
                    <td>Type of the parent object</td>
                </tr>
                <tr>
                    <td>parent.path</td>
                    <td>string or null</td>
                    <td>Full path of the parent object </td>
                </tr>
               <tr>
                    <td>parent.classId</td>
                    <td>string or null</td>
                    <td>Class ID of the parent object. </td>
                </tr>
               <tr>
                    <td>parent.className</td>
                    <td>string or null</td>
                    <td>Class name of the parent object. </td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>creationDate</td>
        <td>Timestamp indicating when the object was created</td>
        <td>string, null or dateTime</td>
    </tr>
     <tr>
        <td>modificationDate</td>
        <td>Timestamp indicating the last time the object was last modified</td>
        <td>string, null or dateTime</td>
    </tr>
     <tr>
        <td>properties</td>
        <td>A list of custom properties associated with the object. Each property contains metadata such as name, type, and data</td>
        <td>
            <table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>name<span style="color: red;">&#9733;</span></td>
                    <td>string or null</td>
                    <td>name of the object.</td>
                </tr>
                <tr>
                    <td>type<span style="color: red;">&#9733;</span></td>
                    <td>string</td>
                    <td>Type of the object</td>
                </tr>
                <tr>
                    <td>data</td>
                    <td>string, null or boolean</td>
                    <td>The data can be one of: <br>
                         #0 = "string or null"<br>
                         #1 = "boolean"
                          </td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>attributes</td>
        <td>A list of attributes of the object. Each attribute contains metadata such as name, type, value and properties</td>
        <td>
            <table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>name<span style="color: red;">&#9733;</span></td>
                    <td>string or null</td>
                    <td>name of the object.</td>
                </tr>
                <tr>
                    <td>type<span style="color: red;">&#9733;</span></td>
                    <td>string or null</td>
                    <td>Type of the object</td>
                </tr>
                <tr>
                    <td>value</td>
                    <td>string or null</td>
                    <td>The data of the object </td>
                </tr>
            </table>
        </td>
    </tr>
   
</table>
