 [Authentication](../General/Authentication.md) 
 
`Version 2024.4.9.0`

Asset Operations
-------
# GET 
## /oktoplus/rest/v1/assets

### Retrieving the collection asset resources

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint retrieves a list of all assets in the system.The returned collection could be filtered using parameters like the page,the  number of items per page,path,type and query. The response will contain the asset data in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>{
  "elements": [
    {
      "internalId": 1,
      "filename": "string",
      "path": "string",
      "mimeType": "string",
      "type": "string",
      "frontEndUrl": "string",
      "creationDate": "2025-10-27T11:26:08.301Z",
      "modificationDate": "2025-10-27T11:26:08.301Z",
      "fileSize": 0,
      "fullpath": "string",
      "formattedFileSize": "string"
    }
  ],
  "page": 0,
  "elementsPerPage": 0,
  "totalElements": 0,
  "lastPage": 0
}</code></pre>
  </div>

</div>

#
## Request Parameters(Non-mandatory)

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
            <td>items per page</td>
            <td>The number of items per page</td>
            <td>integer <br>(1000 items by default)</td>
        </tr>
        <tr>
            <td> path</td>
            <td>The path where the collection is stored</td>
            <td>string</td>
        </tr>
        <tr>
            <td> type </td>
            <td>The asset type used to filter the collection.Multiple values can be inserted seperated by a comma <br>
              (Example: image,document)</td>
            <td>string</td>
        </tr>
       <tr>
            <td>query</td>
            <td>The PQL query(Pimcore Query Language Syntax) used to filter the returned collection </td>
            <td>string</td>
        </tr>
   </table>

## Response Parameters
Required parameter <span style="color: red;">&#9733;</span> 

<table style="width: 100%; border: none; border-collapse: collapse;">
        <tr>
            <th>Parameter</th>
            <th>Description</th>
            <th>Value</th>
        </tr>
        <tr>
            <td>internalId</td>
            <td>The identifier of the retrieved asset</td>
            <td>integer or null(>0)</td>
        </tr>
        <tr>
            <td> filename <span style="color: red;">&#9733; </span></td>
            <td>The name of the file from which the asset was read.</td>
            <td>string or null, max 255 characters</td>
        </tr>
        <tr>
            <td> path <span style="color: red;">&#9733; </span></td>
            <td>The relative file path where the asset is stored</td>
            <td class="string or null, max 765 characters">string</td>
        </tr>
        <tr>
            <td>mimeType</td>
            <td>Indicated the file format or content type </td>
            <td>string or null, max 190 characters</td>
        </tr>
        <tr>
            <td> type <span style="color: red;">&#9733; </span></td>
            <td>The type or category of the asset</td>
            <td>string or null</td>
        </tr>
        <tr>
            <td> creationDate </td>
            <td>The timestamp when the asset was first created</td>
            <td>string or null</td>
        </tr>
        <tr>
            <td>modificationDate</td>
            <td>The timestamp of the most recent modification to the asset</td>
            <td>string or null</td>
        </tr>
        <tr>
            <td>fileSize</td>
            <td>The size of the file in bytes</td>
            <td>integer</td>
        </tr>
        <tr>
            <td>fullPath</td>
            <td>The absolute path to the file which includes the full directory and filename</td>
            <td>string</td>
        </tr>
        <tr>
            <td>formatedFileSize</td>
            <td>A human-readable version of the file size, formatted for easier interpretation.</td>
            <td>string</td>
        </tr>
        <tr>
            <td>page</td>
            <td>The page number from which the asset collection has been retrieved</td>
            <td>integer</td>
        </tr>
       <tr>
            <td>elementsPerPage</td>
            <td>The number of assets per page</td>
            <td>integer</td>
        </tr>
        <tr>
            <td>totalElements</td>
            <td>The total amount of asset retrieved from that particular page</td>
            <td>integer</td>
        </tr>
       <tr>
            <td>lastPage</td>
            <td>The number of the last page</td>
            <td>integer</td>
        </tr>
    </table>

#
## /oktoplus/rest/v1/assets/path/{path}
### Retrieves an asset resource

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint retrieves a particular asset in the system. It requires the asset path. The response will contain the asset data in JSON format.</p>
  </div>
  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>{
  "internalId": 1,
  "filename": "string",
  "path": "string",
  "fullpath": "string",
  "mimeType": "string",
  "type": "string",
  "frontEndUrl": "string",
  "creationDate": "2026-02-02T08:55:30.405Z",
  "modificationDate": "2026-02-02T08:55:30.405Z",
  "fileSize": 0,
  "formattedFileSize": "string"
}
</code></pre>

<h4>404 :Not found</h4>
<pre><code>{
  "@context": "string",
  "@id": "string",
  "@type": "string",
  "id": "string",
  "title": "string",
  "detail": "string",
  "status": 404,
  "instance": "string",
  "type": "string",
  "meta": {},
  "source": {
    "pointer": "string",
    "parameter": "string",
    "header": "string"
  },
  "description": "string",
  "trace": [
    "string"
  ]
}
</code></pre>
  </div>

</div>

## Response Parameters
 The parameters returned by this call are equal to those of /oktoplus/rest/v1/assets
#
## /oktoplus/rest/v1/assets/{id}
### Retrieves an asset resource

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint retrieves a particular asset in the system. It requires an identifier passed in the path. The response will contain the asset data in JSON format.</p>
  </div>
  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>{
  "internalId": 1,
  "filename": "string",
  "path": "string",
  "mimeType": "string",
  "type": "string",
  "frontEndUrl": "string",
  "creationDate": "2025-09-05T08:26:00.350Z",
  "modificationDate": "2025-09-05T08:26:00.350Z",
  "content": "string",
  "fileSize": 0,
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "metadata": [
    {
      "assetId": 0,
      "name": "string",
      "language": "string",
      "type": "input",
      "value": "string"
    }
  ],
  "fullpath": "string",
  "formattedFileSize": "string"
}
</code></pre>

<h4>404 :Not found</h4>
<pre><code>{
  "@context": "string",
  "@id": "string",
  "@type": "string",
  "id": "string",
  "title": "string",
  "detail": "string",
  "status": 404,
  "instance": "string",
  "type": "string",
  "meta": {},
  "source": {
    "pointer": "string",
    "parameter": "string",
    "header": "string"
  },
  "description": "string",
  "trace": [
    "string"
  ]
}
</code></pre>
  </div>

</div>

## Response Parameters
Required parameter <span style="color: red;">&#9733;</span>

<table style="width: 100%">
    <tr>
        <th>Parameter</th> 
        <th>Description</th>
        <th>Value</th>
    </tr>
    <tr>
        <td>internalId</td>
        <td>The identifier of the retrieved asset</td>
        <td>integer or null (>0)</td>
    </tr>
    <tr>
        <td>filename <span style="color: red;">&#9733;</span></td>
        <td>The name of the file from which the asset was read.</td>
        <td>string or null, max 255 characters</td>
    </tr>
    <tr>
        <td>path <span style="color: red;">&#9733;</span></td>
        <td>The relative file path where the asset is stored</td>
        <td>string or null, max 765 characters</td>
    </tr>
    <tr>
        <td>mimeType</td>
        <td>Indicates the file format or content type</td>
        <td>string or null, max 190 characters</td>
    </tr>
    <tr>
        <td>type <span style="color: red;">&#9733;</span></td>
        <td>The type or category of the asset</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>frontEndUrl</td>
        <td>A URL that points to the asset's frontend representation</td>
        <td>string or null</td>
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
        <td>content<span style="color: red;">&#9733;</span></td>
        <td>Raw content or data of the asset.</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>fileSize</td>
        <td>The size of the file in bytes</td>
        <td>integer</td>
    </tr>
    <tr>
        <td>properties</td>
        <td>A list of custom properties associated with the asset. Each property contains metadata such as name, type, and value.</td>
        <td>
            <table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>name</td>
                    <td>string</td>
                    <td>The name of the property.</td>
                </tr>
                <tr>
                    <td>type</td>
                    <td>string</td>
                    <td>The type of the property</td>
                </tr>
                <tr>
                    <td>data</td>
                    <td>string</td>
                    <td>The value or data associated with the property </td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>metadata</td>
        <td>A list of metadata records related to the asset. Each record contains information such as asset ID, name, language, type of data, and the value of the metadata.</td>
        <td>
            <table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>assetId</td>
                    <td>integer</td>
                    <td>The identifier of the related asset</td>
                </tr>
                <tr>
                    <td>name<span style="color: red;">&#9733;</span></td>
                    <td>string</td>
                    <td>The name or label of the metadata</td>
                </tr>
                <tr>
                    <td>language</td>
                    <td>string</td>
                    <td>The language in which the metadata is provided </td>
                </tr>
                <tr>
                    <td>type<span style="color: red;">&#9733;</span></td>
                    <td>string("input" by default)</td>
                    <td>The type of metadata</td>
                </tr>
                <tr>
                    <td>value</td>
                    <td>any</td>
                    <td>The actual value of the metadata</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>fullPath</td>
        <td>The absolute path to the file which includes the full directory and filename</td>
        <td>string</td>
    </tr>
    <tr>
        <td>formattedFileSize</td>
        <td>A human-readable version of the file size, formatted for easier interpretation.</td>
        <td>string or null</td>
    </tr>
</table>

#

# POST
## /oktoplus/rest/v1/assets

### Creating an asset resource

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
  "filename": "string",
  "path": "string",
  "mimeType": "string",
  "type": "string",
  "content": "string",
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "metadata": [
    {
      "name": "string",
      "language": "string",
      "type": "input",
      "value": "string"
    }
  ],
  "options": {}
}</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint creates a new asset resource. It requires that the parameters of the new object should be specified in the request body and in their correct format . The response will contain the created asset data in JSON format.</p>
    </td>
  </tr>
</table>

#
## Request Parameters
Required parameter <span style="color: red;">&#9733;</span>
<table style="width: 100%">
    <tr>
        <th>Parameter</th>
        <th>Description</th>
        <th>Value</th>
    </tr>
    <tr>
        <td>filename <span style="color: red;">&#9733;</span></td>
        <td>The name of the file that represents the asset</td>
        <td>string or null, max 255 characters</td>
    </tr>
    <tr>
        <td>path <span style="color: red;">&#9733;</span></td>
        <td>The relative file path where the asset will be stored</td>
        <td>string or null, max 765 characters</td>
    </tr>
    <tr>
        <td>mimeType</td>
        <td>Indicates the file format or content type</td>
        <td>string or null, max 190 characters</td>
    </tr>
    <tr>
        <td>type <span style="color: red;">&#9733;</span></td>
        <td>A category or classification for the asset</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>content <span style="color: red;">&#9733;</span></td>
        <td>Raw content or data of the asset.</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>properties </td>
        <td>A list of custom properties associated with the asset. Each property contains metadata such as name, type, and value.</td>
        <td>
            <table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>name<span style="color: red;">&#9733;</span></td>
                    <td>string</td>
                    <td>The name of the property.</td>
                </tr>
                <tr>
                    <td>type<span style="color: red;">&#9733;</span></td>
                    <td>string</td>
                    <td>The type of the property</td>
                </tr>
                <tr>
                    <td>data</td>
                    <td>string</td>
                    <td>The value or data associated with the property </td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>metadata</td>
        <td>List of metadata records related to the asset. Each record contains name, language, type, and value.</td>
        <td>
            <table style="width: 100%; margin-top: 10px; border: 1px solid #ddd;">
                <tr>
                    <td>name<span style="color: red;">&#9733;</span></td>
                    <td>string</td>
                    <td>The name or label of the metadata</td>
                </tr>
                <tr>
                    <td>language</td>
                    <td>string</td>
                    <td>The language in which the metadata is provided </td>
                </tr>
                <tr>
                    <td>type<span style="color: red;">&#9733;</span></td>
                    <td>string("input" by default)</td>
                    <td>The type can be picked from an array of Enum:<br>
                        #0 = "checkbox"<br>
                        #1 = "date"<br>
                        #2 = "input"<br>
                        #3 = "textarea"<br>
                        #4 = "select"<br> 
                    </td>
                </tr>
                <tr>
                    <td>value</td>
                    <td>any</td>
                    <td>The actual value of the metadata</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>options</td>
        <td>Optional object for custom configuration when creating the asset</td>
        <td>object</td>
    </tr>

</table>

## Responses

---
  
 </code></pre>
<h4> 201: Asset resource created </h4>

<pre><code>
 {
  "internalId": 1,
  "filename": "string",
  "path": "string",
  "mimeType": "string",
  "type": "string",
  "frontEndUrl": "string",
  "creationDate": "2025-09-04T10:56:30.719Z",
  "modificationDate": "2025-09-04T10:56:30.719Z",
  "content": "string",
  "fileSize": 0,
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "metadata": [
    {
      "assetId": 0,
      "name": "string",
      "language": "string",
      "type": "input",
      "value": "string"
    }
  ],
  "fullpath": "string",
  "formattedFileSize": "string"
}
</code></pre>

<h4>400: Invalid input</h4>
<pre><code>
  {
  "@context": "string",
  "@id": "string",
  "@type": "string",
  "id": "string",
  "title": "string",
  "detail": "string",
  "status": 404,
  "instance": "string",
  "type": "string",
  "meta": {},
  "source": {
    "pointer": "string",
    "parameter": "string",
    "header": "string"
  },
  "description": "string",
  "trace": [
    "string"
  ]
}
</code></pre>
<h4>422: An error occured</h4>
<pre><code>
  {
  "@context": "string",
  "@id": "string",
  "@type": "string",
  "status": 422,
  "violations": [
    {
      "propertyPath": "string",
      "message": "string"
    }
  ],
  "detail": "string",
  "description": "string",
  "type": "string",
  "title": "string",
  "instance": "string"
}
</code></pre>

---

#

# PUT
## /oktoplus/rest/v1/assets/{id}
### Replacing a given asset

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
  "filename": "string",
  "path": "string",
  "mimeType": "string",
  "type": "string",
  "content": "string",
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "metadata": [
    {
      "name": "string",
      "language": "string",
      "type": "input",
      "value": "string"
    }
  ],
  "options": {}
}</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint replaces a given asset resource with another one. It requires that the parameters of the object to be updated including the identifier should be specified in the request body and in their correct format . The response will contain the updated asset data in JSON format.</p>
    </td>
  </tr>
</table>

#
## /oktoplus/rest/v1/assets/path/{path}
### Replacing a given asset

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
  "filename": "string",
  "path": "string",
  "mimeType": "string",
  "type": "string",
  "content": "string",
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "metadata": [
    {
      "name": "string",
      "language": "string",
      "type": "input",
      "value": "string"
    }
  ],
  "options": {}
}</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint replaces a given asset resource with another one. It requires that the parameters of the object to be updated including its path should be specified in the request body and in their correct format . The response will contain the updated asset data in JSON format.</p>
    </td>
  </tr>
</table>

#
## Request Parameters
The parameters sent in a put request are the same as in the post request
## Responses

---
<h4>200: Ok</h4>
<pre><code>
{
  "internalId": 1,
  "filename": "string",
  "path": "string",
  "mimeType": "string",
  "type": "string",
  "frontEndUrl": "string",
  "creationDate": "2025-09-05T08:37:17.618Z",
  "modificationDate": "2025-09-05T08:37:17.618Z",
  "content": "string",
  "fileSize": 0,
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "metadata": [
    {
      "assetId": 0,
      "name": "string",
      "language": "string",
      "type": "input",
      "value": "string"
    }
  ],
  "fullpath": "string",
  "formattedFileSize": "string"
}
</code></pre>

<h4>400: Invalid input</h4>
<pre><code>
{
  "@context": "string",
  "@id": "string",
  "@type": "string",
  "id": "string",
  "title": "string",
  "detail": "string",
  "status": 404,
  "instance": "string",
  "type": "string",
  "meta": {},
  "source": {
    "pointer": "string",
    "parameter": "string",
    "header": "string"
  },
  "description": "string",
  "trace": [
    "string"
  ]
}
</code></pre>

<h4>404: Not found</h4>
<pre><code>
{
  "@context": "string",
  "@id": "string",
  "@type": "string",
  "id": "string",
  "title": "string",
  "detail": "string",
  "status": 404,
  "instance": "string",
  "type": "string",
  "meta": {},
  "source": {
    "pointer": "string",
    "parameter": "string",
    "header": "string"
  },
  "description": "string",
  "trace": [
    "string"
  ]
}
</code></pre>

<h4>422: An error occurred</h4>
<pre><code>
{
  "@context": "string",
  "@id": "string",
  "@type": "string",
  "status": 422,
  "violations": [
    {
      "propertyPath": "string",
      "message": "string"
    }
  ],
  "detail": "string",
  "description": "string",
  "type": "string",
  "title": "string",
  "instance": "string"
}
</code></pre>

---------------------

#

# DELETE
## /oktoplus/rest/v1/assets/{id}
### Removing an asset

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint removes a given asset in the system. It requires the identifier of the asset as  parameter.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>204 :Asset resource deleted</h4>
    
<h4>404 :Not found</h4>
    <pre><code>{
  "@context": "string",
  "@id": "string",
  "@type": "string",
  "title": "string",
  "detail": "string",
  "status": 404,
  "instance": "string",
  "type": "string",
  "description": "string"
}
</code></pre>
  </div>

</div>

#
## /oktoplus/rest/v1/assets/path/{path}
### Removing an asset

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint removes a given asset in the system. It requires the path of the asset as  parameter.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>204 :Asset resource deleted</h4>

<h4>404 :Not found</h4>
<pre><code>{
"@context": "string",
"@id": "string",
"@type": "string",
"title": "string",
"detail": "string",
"status": 404,
"instance": "string",
"type": "string",
"description": "string"
}
</code></pre>
  </div>

</div>

#

[Asset metadata](AssetMetadata.md)
