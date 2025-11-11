[Asset](Asset.md)

`Version 2024.4.4.1`

Asset Metadata Operations
-------
# GET
## /oktoplus/rest/v1/assets/{assetId}/metadata
### Retrieving the collection of all asset metadata
<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint retrieves a list of all asset metadata resources in the system. It requires the asset metadata identifier as parameter in the path. The response will contain a list of asset metadata resources in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>[
  {
    "assetId": 0,
    "name": "string",
    "language": "string",
    "type": "input",  
    "value": "string"
  }
]
</code></pre>
  </div>

</div>


## Retrieving an Asset Metadata resource
## /oktoplus/rest/v1/assets/{assetId}/metadata/language/{language}
### Using the 'Language' parameter

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint retrieves a list of all asset metadata resources in the system. It requires that the asset metadata identifier and the language should be passed as parameters in the path. The response will contain  the asset metadata resource in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>[
  {
    "assetId": 0,
    "name": "string",
    "language": "string",
    "type": "input",
    "value": "string"
  }
]</code></pre>
  </div>

</div>


## /oktoplus/rest/v1/assets/{assetId}/metadata/{name}
### Retrieving one asset resource
### Using the 'name' parameter

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint retrieves an asset metadata resource in the system. It requires the asset metadata's identifier and the name should be passed as parameters in the path. The response will contain the asset metadata resource in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>{
  "assetId": 0,
  "name": "string",
  "language": "string",
  "type": "input",
  "value": "string"
}</code></pre>

<h4>404: Not found </h4>
<pre><code>
{
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

## /oktoplus/rest/v1/assets/{assetId}/metadata/{name}/language/{language}
### Using the 'name' and 'language' parameters

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint retrieves an asset metadata resources in the system. It requires the asset metadata's identifier, name and language  should be passed as parameters in the path. The response will contain a list of asset metadata resources in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>{
  "assetId": 0,
  "name": "string",
  "language": "string",
  "type": "input",
  "value": "string"
}</code></pre>

<h4>404: Not found </h4>
<pre><code>
{
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

## Response Parameters
Required parameter <span style="color: red;">&#9733;</span>
<table style="width: 100%">
    <tr>
        <th>Parameter</th>
        <th>Description</th>
        <th>Value</th>
    </tr>
    <tr>
        <td>assetId </td>
        <td>The identifier of the asset</td>
        <td>integer or null</td>
    </tr>
    <tr>
        <td>name <span style="color: red;">&#9733;</span></td>
        <td>The name of the asset metadata</td>
        <td>string or null, max 190 characters</td>
    </tr>
    <tr>
        <td>language</td>
        <td>The language in which the metadata is provided</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>type <span style="color: red;">&#9733;</span></td>
        <td>A category or classification for the asset metadata,The type can be picked from an array of Enum:<br>
                        #0 = "checkbox"<br>
                        #1 = "date"<br>
                        #2 = "input"<br>
                        #3 = "textarea"<br>
                        #4 = "select"<br> </td>
        <td>string</td>
    </tr>
    <tr>
        <td>value <span style="color: red;">&#9733;</span></td>
        <td>The actual value of the metadata.</td>
        <td>any</td>
    </tr>

</table>

-------------
#

# POST
## /oktoplus/rest/v1/assets/{assetId}
### Creating an asset metadata resource

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
  "name": "string",
  "language": "string",
  "type": "input",
  "value": "string"
}</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint created a new asset metadata into the system. It requires that the parameters of the new object should be specified in the request body and in their correct format . The response will contain the created asset data in JSON format.</p>
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
        <td>name <span style="color: red;">&#9733;</span></td>
        <td>The name of the asset metadata</td>
        <td>string or null, max 190 characters</td>
    </tr>
    <tr>
        <td>language</td>
        <td>The language in which the metadata is provided</td>
        <td>string or null</td>
    </tr>
    <tr>
        <td>type <span style="color: red;">&#9733;</span></td>
        <td>A category or classification for the asset metadata,The type can be picked from an array of Enum:<br>
                        #0 = "checkbox"<br>
                        #1 = "date"<br>
                        #2 = "input"<br>
                        #3 = "textarea"<br>
                        #4 = "select"<br> </td>
        <td>string</td>
    </tr>
    <tr>
        <td>value <span style="color: red;">&#9733;</span></td>
        <td>The actual value of the metadata.</td>
        <td>any</td>
    </tr>

</table>

#
## Responses
<h4>201: Asset Metadata resource created </h4>
<pre><code>
{
  "assetId": 0,
  "name": "string",
  "language": "string",
  "type": "input",
  "value": "string"
}
</code></pre>
<h4>400: Invalid input </h4>
<pre><code>
{
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
<h4>422: An error occurred </h4>
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

-------------------

#
# PUT

### Replacing a given asset
## /oktoplus/rest/v1/assets/{assetId}/metadata/{name}
###  Using the 'name' parameter

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
  "name": "string",
  "language": "string",
  "type": "input",
  "value": "string"
}</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint replaces a given asset metadata resource with another one. It requires that the parameters of the updated object including the identifier and the name should be specified in the request body and in their correct format . The response will contain the updated asset metadata in JSON format.</p>
    </td>
  </tr>
</table>

#

## Request Parameters
The parameters sent in a put request are the same as in the post request
## Responses 

-------
<h4>200:Asset Metadata resource updated </h4>
<pre><code>
 {
  "assetId": 0,
  "name": "string",
  "language": "string",
  "type": "input",
  "value": "string"
}
</code></pre>

<h4>400: Invalid input </h4>
<pre><code>
 {
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

<h4>404: Not found </h4>
<pre><code>
{
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

<h4>422: An error occurred </h4>
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

-------------------
#

## /oktoplus/rest/v1/assets/{assetId}/metadata/{name}/language/{language}
### Using the 'language' and 'name' parameters

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{{
  "name": "string",
  "language": "string",
  "type": "input",
  "value": "string"
}</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint replaces a given asset metadata resource with another one. It requires that the parameters of the updated object including the identifier, the name and the language should be specified in the request body and in their correct format . The response will contain the updated asset metadata in JSON format.</p>
    </td>
  </tr>
</table>

#

### Responses

------

<h4>200: Asset Metadata updated</h4>
<pre><code>

"assetId": 0,
"name": "string",
"language": "string",
"type": "input",
"value": "string"
}
</code></pre>

<h4> 400: Invalid input</h4>
<pre><code>
{
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

<h4> 404: Not found</h4>
<pre><code>
{
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

<h4>422: An error occurred </h4>
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

#

# DELETE
## Removing an asset metadata
## /oktoplus/rest/v1/assets/{assetId}/metadata/{name}
### Using the 'name' parameter

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint removes a given asset in the system. It requires that the identifier and the name of the asset metadata should be passed as parameters in the path.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
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
}</code></pre>
  </div>

</div>

## /oktoplus/rest/v1/assets/{assetId}/metadata/{name}/language/{language}
### Using the 'name' and 'language' parameters

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint removes a given asset in the system. It requires that the identifier, the name and the language of the asset metadata should be passed as parameters in the path.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
     <h4>204 :Asset Metadata resource deleted</h4>
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
}</code></pre>
  </div>

</div>

#

[Data Object](../DataObject/DataObject.md)
