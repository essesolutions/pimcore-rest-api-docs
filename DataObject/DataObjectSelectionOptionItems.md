[Data object](DataObject.md)

`Version 2024.4.4.1`

Data Object Select Option Operations
-------

# GET
## /oktoplus/rest/v1/objects/selectoptions/{config}/items
### Retrieving the collection of Data Object Select Option Items resources

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3>Parameters Description</h3>
    <p>This endpoint retrieves a list of all data object select option items resources in the system. It requires the object's identifier as parameter in the path at the place of 'config' parameter. The response will contain a list of data object select option items resources in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>[
  {
    "name": "string",
    "label": "string",
    "value": "string"
  }
]
</code></pre>
  </div>

</div>

#

### Retrieving a Data Object Select Option Item resource 

## /oktoplus/rest/v1/objects/selectoptions/{config}/items/label/{label}
### Using the 'label' parameter

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3>Parameters Description</h3>
    <p>This endpoint retrieves a data object select option resource in the system. It requires the object's identifier at the place of the 'config' parameter and the label, both should be passed as parameters in the path. The response will contain the data object selection option item resource in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>{
  "name":"string",
  "label": "string",
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

## /oktoplus/rest/v1/objects/selectoptions/{config}/items/name/{name}
### Using the 'name' parameter

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3>Parameters Description</h3>
    <p>This endpoint retrieves a data object select option resource in the system. It requires the object's identifier at the place of the 'config' parameter and the name, both should be passed as parameters in the path. The response will contain the data object selection option item resource in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>{
  "name": "string",
  "label": "string",
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

<table style="width: 100%; border: none; border-collapse: collapse;">
        <tr>
            <th>Parameter</th>
            <th>Description</th>
            <th>Value</th>
        </tr>
        <tr>
            <td>name</td>
            <td>The name of the select option</td>
            <td>string or null <br>
               matches ^(.*[a-zA-Z0-9]+.*)$ </td>
        </tr>
        <tr>
            <td> label <span style="color: red;">&#9733; </span></td>
            <td>The of the read select option.</td>
            <td>string</td>
        </tr>
        <tr>
            <td> value <span style="color: red;">&#9733; </span></td>
            <td>The value of the read select option</td>
            <td >string</td>
        </tr>
    </table>

#

# POST
## /oktoplus/rest/v1/objects/selectoptions/{config}/items
### Creating a Data Object Select Option Item resource 
<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
  "name": "string",
  "label": "string",
  "value": "string"
}</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint creates a new data object select option item into the system. It requires that the parameters of the new object should be specified in the request body and in their correct format . The response will contain the created object in JSON format.</p>
    </td>
  </tr>
</table>

## Request Parameters
The request parameters of the post method are the same as in the response parameters of the get method
#
### Responses
<h4>201: Data Object Select Option Items resource created </h4>
<pre><code>
{
  "name": "string"
  "label": "string",
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
  "status": 400,
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

#
# PUT
### Replacing a Data Object Select Option Item resource

## /oktoplus/rest/v1/objects/selectoptions/{config}/items/label/{label}
### Using the 'label' parameter

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
          "name": "string"
          "label": "string",
           "value": "string"
      }</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint replaces a given data object select option items resource with another one. It requires that the parameters of the updated object including the identifier and the label should be specified in the request body and in their correct format . The response will contain the updated object in JSON format.</p>
    </td>
  </tr>
</table>

## Request Parameters
The request parameters of the put method are the same as those of a post method
#
### Responses
<h4>200: Data Object Select Option Items resource updated </h4>
<pre><code>
{
  "name": "string"
  "label": "string",
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

## /oktoplus/rest/v1/objects/selectoptions/{config}/items/name/{name}
### Using the 'name' parameter

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
          "name": "string"
          "label": "string",
           "value": "string"
      }</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint replaces a given data object select option items resource with another one. It requires that the parameters of the updated object including the identifier and the name should be specified in the request body and in their correct format . The response will contain the updated object in JSON format.</p>
    </td>
  </tr>
</table>

### Responses
<h4>200: Data Object Select Option Items resource updated </h4>
<pre><code>
{
  "name": "string"
  "label": "string",
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
# DELETE
### Removing a Data Object Select Option Item resource

## /oktoplus/rest/v1/objects/selectoptions/{config}/items/label/{label}
### Using the 'label' parameter

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3>Parameters Description</h3>
    <p>This endpoint removes a given data object select option item in the system. It requires that the identifier and the label of the object should be passed as parameters in the path.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
   <h4>204 :Data Object Select Option Items resource deleted</h4>
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

## /oktoplus/rest/v1/objects/selectoptions/{config}/items/name/{name}
### Using the 'name' parameter

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3>Parameters Description</h3>
    <p>This endpoint removes a given data object select option item in the system. It requires that the identifier and the name of the object should be passed as parameters in the path.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>204 :Data Object Select Option Items resource deleted</h4>
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
