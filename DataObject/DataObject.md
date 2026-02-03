[Asset metadata](../Asset/AssetMetadata.md)

`Version 2024.4.9.0`

Data Object Operations
-------

# GET
## /oktoplus/rest/v1/objects
### Retrieving the collection of Data Object resources

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3> Description</h3>
    <p>This endpoint retrieves a list of all data object resources in the system. The returned collection could be filtered using parameters like the page,path,class or whether it retrieves also unpublished objects or not. The response will contain a list of data object resources in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>{
  "elements": [
    {
      "id": "string",
      "key": "string",
      "path": "string",
      "classId": "string",
      "className": "string",
      "type": "string",
      "parent": {
        "id": 0,
        "type": "string",
        "path": "string",
        "classId": "string",
        "className": "string"
      },
      "creationDate": "2025-10-27T11:47:01.844Z",
      "modificationDate": "2025-10-27T11:47:01.844Z"
    }
  ],
  "page": 0,
  "elementsPerPage": 0,
  "totalElements": 0,
  "lastPage": 0
}
</code></pre>
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
            <td>integer <br>
               (default value:1)</td>
        </tr>
        <tr>
            <td> path</td>
            <td>The path of the data object collection</td>
            <td>string</td>
        </tr>
        <tr>
            <td> class </td>
            <td>The data object class id or class name used to filter the collection.Multiple values can be inserted seperated by a comma <br>
              (Example: OBJ1,OBJ2,OBJ3)</td>
            <td>string</td>
        </tr>
       <tr>
            <td>includeUnpublished</td>
            <td>The option to add unpublished object or not </td>
            <td>boolean</td>
        </tr>
   </table>

#
## /oktoplus/rest/v1/objects/{classId}/{id}
### Retrieving a Data Object resource

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3>Parameters Description</h3>
    <p>This endpoint retrieves a list of all data object resources in the system. 
        It requires  the object identifier and the class identifier as parameters in the path.
        The response will contain the created data object in JSON format.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>200 :OK</h4>
    <pre><code>{
  "id": "string",
  "key": "string",
  "path": "string",
  "classId": "string",
  "className": "string",
  "type": "string",
  "parent": {
    "id": 0,
    "type": "string",
    "path": "string",
    "classId": "string",
    "className": "string"
  },
  "creationDate": "2025-09-05T14:55:13.568Z",
  "modificationDate": "2025-09-05T14:55:13.568Z",
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "attributes": [
    {
      "name": "string",
      "type": "string",
      "value": "string",
      "properties": [
        {
          "name": "string",
          "value": "string"
        }
      ]
    }
  ]
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
  </div>

</div>

#

## Response Parameters

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
        <td>Timestamp indicating the time the object was last modified</td>
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
                    <td>name of the property.</td>
                </tr>
                <tr>
                    <td>type<span style="color: red;">&#9733;</span></td>
                    <td>string</td>
                    <td>Type of the property</td>
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
        <td>page</td>
        <td>The page number from which the data object collection has been retrieved</td>
        <td>integer</td>
    </tr>
   <tr>
            <td>elementsPerPage</td>
            <td>The number of data object per page</td>
            <td>integer</td>
        </tr>
        <tr>
            <td>totalElements</td>
            <td>The total amount of objects retrieved from that particular page</td>
            <td>integer</td>
        </tr>
       <tr>
            <td>lastPage</td>
            <td>The number of the last page</td>
            <td>integer</td>
        </tr>
    <tr>
        <td>attributes</td>
        <td>A list of attributes of the object. </td>
        <td>
       Each attribute is configured in a special way according to its type.
        </td>
    </tr>

</table>

### Attribute type configuration: <br>


| Attribute Group | Attribute Type                                                                    |
|-----------------|-----------------------------------------------------------------------------------|
| Text            | [Textarea](Attributes/Textarea.md)                                                |
| Text            | [Input](Attributes/Input.md)                                                      |
| Text            | [WYSIWYG](Attributes/WYSIWYG.md)                                                  |
| Text            | [Password](Attributes/Password.md)                                                |
| Text            | [InputQuantityValue](Attributes/InputQuantity.md)                                 |
| Date            | [Date](Attributes/Date.md)                                                        |
| Date            | [Time](Attributes/Time.md)                                                        |
| Date            | [DateRange](Attributes/DateRange.md)                                              |
| Date            | [DateTime](Attributes/DateTime.md)                                                |
| Number          | [Numeric](Attributes/Numeric.md)                                                  |
| Structured      | [ObjectBrick](Attributes/ObjectBrick.md)                                          |
| Structured      | [LocalizedFields](Attributes/LocalizedField.md)                                   |
| Structured      | [FieldCollection](Attributes/FieldCollection.md)                                  |
| Structured      | [ClassificationStore](Attributes/CertificationStore.md)                           |
| Relation        | [ManyToOneRelation](Attributes/ManyToOneRelation.md)                              |
| Relation        | [ManyToManyRelation](Attributes/ManyToManyRelation.md)                            |
| Relation        | [ManyToManyObjectRelation](Attributes/ManyToManyObjectRelation.md)                |
| Relation        | [AdvancedManyToManyRelation](Attributes/AdvancedManyToManyRelation.md)            |
| Relation        | [AdvancedManyToManyObjectRelation](Attributes/AdvancedManyToManyObjectRelation.md) |
| Other           | [CalculatedValue](Attributes/CalculatedValue.md)                                  |
| Other           | [Checkbox](Attributes/CheckBox.md)                                                |
| Media           | [Image](Attributes/Image.md)                                                      |
| Media           | [ImageGallery](Attributes/ImageGallery.md)                                        |
| Media           | [Video](Attributes/Video.md)                                                      |
| Media           | [HotspotImage](Attributes/HotspotImage.md)                                        |
| Select          | [Select](Attributes/Select.md)                                                    |

#
# POST
##  /oktoplus/rest/v1/objects
### Creating a Data Object resource

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
  "id": "string",
  "key": "string",
  "classId": "string",
  "className": "string",
  "type": "string",
  "parent": {
    "id": 0,
    "type": "string",
    "path": "string",
    "classId": "string",
    "className": "string"
  },
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "attributes": [
    {
      "name": "string",
      "type": "string",
      "value": "string",
      "properties": [
        {
          "name": "string",
          "value": "string"
        }
      ]
    }
  ],
  "options": [
    {
      "name": "string",
      "value": "string"
    }
  ]
}</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint created a new data object into the system. It requires that the
        parameters of the new object should be specified in the request body and in their 
        correct format . The response will contain the created asset data in JSON format.</p>
    </td>
  </tr>
</table>

## Request Parameters
The request parameters of the post method are the same as in the response parameters of the get method
#
## Responses

--------
<h4> 201: Data Object resource created</h4>
<pre><code>
{
  "id": "string",
  "key": "string",
  "path": "string",
  "classId": "string",
  "className": "string",
  "type": "string",
  "parent": {
    "id": 0,
    "type": "string",
    "path": "string",
    "classId": "string",
    "className": "string"
  },
  "creationDate": "2025-09-05T15:04:41.083Z",
  "modificationDate": "2025-09-05T15:04:41.083Z",
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "attributes": [
    {
      "name": "string",
      "type": "string",
      "value": "string",
      "properties": [
        {
          "name": "string",
          "value": "string"
        }
      ]
    }
  ]
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
#

# PUT
## /oktoplus/rest/v1/objects/{classId}/{id}
### Replaces a Data Object resources

<table style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td style="width: 50%; vertical-align: top; padding-right: 20px; padding-left: 10px;">
      <h3> Request Body</h3>
      <pre><code>{
  "id": "string",
  "key": "string",
  "classId": "string",
  "className": "string",
  "type": "string",
  "parent": {
    "id": 0,
    "type": "string",
    "path": "string",
    "classId": "string",
    "className": "string"
  },
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "attributes": [
    {
      "name": "string",
      "type": "string",
      "value": "string",
      "properties": [
        {
          "name": "string",
          "value": "string"
        }
      ]
    }
  ],
  "options": [
    {
      "name": "string",
      "value": "string"
    }
  ]
}</code></pre>
    </td>
    <td style="width: 50%; vertical-align: top; padding-left: 20px;">
      <h3>Request Description</h3>
      <p>This endpoint updates an existing data object into the system. It requires that the
         parameters of the new object,it's class identifier and object identifier should be 
         specified in the request body and in their correct format . The response will 
         contain the updated data object in JSON format.</p>
    </td>
  </tr>
</table>

## Request Parameters
The parameters sent in a put request are the same as in the post request

## Responses

-----

<h4>200: Data Object resource update </h4>
<pre><code>
{
  "id": "string",
  "key": "string",
  "path": "string",
  "classId": "string",
  "className": "string",
  "type": "string",
  "parent": {
    "id": 0,
    "type": "string",
    "path": "string",
    "classId": "string",
    "className": "string"
  },
  "creationDate": "2025-09-05T15:11:36.876Z",
  "modificationDate": "2025-09-05T15:11:36.876Z",
  "properties": [
    {
      "name": "string",
      "type": "text",
      "data": "string"
    }
  ],
  "attributes": [
    {
      "name": "string",
      "type": "string",
      "value": "string",
      "properties": [
        {
          "name": "string",
          "value": "string"
        }
      ]
    }
  ]
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

<h4>404: Not found  </h4>
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

<h4> 422: An error occurred</h4>
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
## /oktoplus/rest/v1/objects/{classId}/{id}
### Removes the Data Object resource

<div style="display: flex; justify-content: space-between; align-items: flex-start;">

  <div style="flex: 1; margin-right: 20px;">
    <h3>Parameters Description</h3>
    <p>This endpoint removes a given data object in the system. It requires that the object 
        identifier and the class identifier should be passed as parameters in the path.</p>
  </div>

  <div style="flex: 1; border-left: 2px solid #ddd; padding-left: 20px;">
    <h3>Response</h3>
    <h4>204 :DataObject resource deleted</h4>
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
}</code></pre>
  </div>

</div>

#

[Data object select option item](DataObjectSelectionOptionItems.md)