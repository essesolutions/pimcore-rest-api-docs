
[Introduction](../README.md)

`Version 2024.4.4.1`

Authentication
-------
The Pimcore REST API uses Bearer token authentication, following the OAuth 2.0 standard. You need to include your API key as a Bearer token in the Authorization header for all API calls.
### Obtaining Your API Key

<ol>
<li>Log in to your Pimcore admin panel</li>
<li>Navigate to Settings > Users</li>
<li>Select your user account or create a new API user</li>
<li>Generate an API key in the API Keys section</li>
<li>Copy and securely store your API key</li>
</ol>

Using Bearer Authentication
Include your API key as a Bearer token in the Authorization header with every request:
<pre><code>Authorization: Bearer your-api-key-here</code></pre>


Endpoint
--------
<pre><code>https://oktoplus/rest/[API_VERSION]/[ENDPOINT]</code></pre>
<table style="width: 100%; border: none; border-collapse: collapse;">
 <tr>
   <td>API_VERSION</td>
   <td>The current version of the api</td>
 </tr>
<tr>
   <td>ENDPOINT</td>
   <td>The endpoint you want to call</td>
 </tr>
</table>


HTTP Status Codes
--------
The API uses standard HTTP status codes:

<ul>
<li> 200 OK: Request succeeded </li>
<li>201 Created: Resource successfully created</li>
<li>204 No Content: Request succeeded with no response body</li>
<li>400 Bad Request: Invalid request parameters</li>
<li>401 Unauthorized: Invalid or missing API key</li>
<li>403 Forbidden: Insufficient permissions</li>
<li>404 Not Found: Resource does not exist</li>
<li>429 Too Many Requests: Rate limit exceeded</li>
<li>500 Internal Server Error: Server-side error occurred</li>
</ul>

[Asset](../Asset/Asset.md)
