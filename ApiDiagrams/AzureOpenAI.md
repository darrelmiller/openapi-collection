# Azure OpenAI API version 2022-12-01

OpenAPI: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/cognitiveservices/data-plane/AzureOpenAI/authoring/stable/2022-12-01/azureopenai.json
<div>
<span style="padding:2px;background-color:lightSteelBlue">GET</span>
<span style="padding:2px;background-color:SteelBlue">POST</span>
<span style="padding:2px;background-color:forestGreen">GET POST</span>
<span style="padding:2px;background-color:yellowGreen">GET PATCH DELETE</span>
<span style="padding:2px;background-color:olive">GET PUT DELETE</span>
<span style="padding:2px;background-color:darkseagreen">GET DELETE</span>
<span style="padding:2px;background-color:tomato">DELETE</span>
</div>

```mermaid
graph LR
classDef GET fill:lightSteelBlue,stroke:#333,stroke-width:2px;
classDef POST fill:SteelBlue,stroke:#333,stroke-width:2px;
classDef GETPOST fill:forestGreen,stroke:#333,stroke-width:2px;
classDef DELETEGETPATCH fill:yellowGreen,stroke:#333,stroke-width:2px;
classDef DELETEGETPUT fill:olive,stroke:#333,stroke-width:2px;
classDef DELETEGET fill:DarkSeaGreen,stroke:#333,stroke-width:2px;
classDef DELETE fill:tomato,stroke:#333,stroke-width:2px;
classDef OTHER fill:white,stroke:#333,stroke-width:2px;
/ --> /deployments[deployments]
/deployments --> /deployments/:deployment-id[:deployment-id]
class /deployments/:deployment-id DELETEGETPATCH
class /deployments GETPOST
/ --> /files[files]
/files --> /files/:file-id[:file-id]
/files/:file-id --> /files/:file-id/content[content]
class /files/:file-id/content GET
class /files/:file-id DELETEGET
/files --> /files/import[import]
class /files/import POST
class /files GETPOST
/ --> /fine-tunes[fine-tunes]
/fine-tunes --> /fine-tunes/:fine-tune-id[:fine-tune-id]
/fine-tunes/:fine-tune-id --> /fine-tunes/:fine-tune-id/events[events]
class /fine-tunes/:fine-tune-id/events GET
/fine-tunes/:fine-tune-id --> /fine-tunes/:fine-tune-id/cancel[cancel]
class /fine-tunes/:fine-tune-id/cancel POST
class /fine-tunes/:fine-tune-id DELETEGET
class /fine-tunes GETPOST
/ --> /models[models]
/models --> /models/:model-id[:model-id]
class /models/:model-id GET
class /models GET
class / OTHER
```
