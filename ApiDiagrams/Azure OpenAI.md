# Azure OpenAI API version 2022-12-01

OpenAPI: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/cognitiveservices/data-plane/AzureOpenAI/authoring/stable/2022-12-01/azureopenai.json
<div>
<span style="padding:2px;background-color:lightSteelBlue;border: 2px solid">GET</span>
<span style="padding:2px;background-color:Lightcoral;border: 2px solid">POST</span>
<span style="padding:2px;background-color:forestGreen;border: 2px solid">GET POST</span>
<span style="padding:2px;background-color:yellowGreen;border: 2px solid">DELETE GET PATCH</span>
<span style="padding:2px;background-color:oliveDrab;border: 2px solid">DELETE GET PATCH PUT</span>
<span style="padding:2px;background-color:olive;border: 2px solid">DELETE GET PUT</span>
<span style="padding:2px;background-color:DarkSeaGreen;border: 2px solid">DELETE GET</span>
<span style="padding:2px;background-color:Tomato;border: 2px solid">DELETE</span>
<span style="padding:2px;background-color:White;border: 2px solid">OTHER</span>
</div>

```mermaid
graph LR
classDef GET fill:lightSteelBlue,stroke:#333,stroke-width:2px
classDef POST fill:Lightcoral,stroke:#333,stroke-width:2px
classDef GET_POST fill:forestGreen,stroke:#333,stroke-width:2px
classDef DELETE_GET_PATCH fill:yellowGreen,stroke:#333,stroke-width:2px
classDef DELETE_GET_PATCH_PUT fill:oliveDrab,stroke:#333,stroke-width:2px
classDef DELETE_GET_PUT fill:olive,stroke:#333,stroke-width:2px
classDef DELETE_GET fill:DarkSeaGreen,stroke:#333,stroke-width:2px
classDef DELETE fill:Tomato,stroke:#333,stroke-width:2px
classDef OTHER fill:White,stroke:#333,stroke-width:2px
/["/"] --> /deployments("deployments")
/deployments("deployments") --> /deployments/:deployment_id(("{deployment-id}"))
class /deployments/:deployment_id DELETE_GET_PATCH
class /deployments GET_POST
/["/"] --> /files("files")
/files("files") --> /files/:file_id(("{file-id}"))
/files/:file_id(("{file-id}")) --> /files/:file_id/content["content"]
class /files/:file_id/content GET
class /files/:file_id DELETE_GET
/files("files") --> /files/import>"import"]
class /files/import POST
class /files GET_POST
/["/"] --> /fine_tunes("fine-tunes")
/fine_tunes("fine-tunes") --> /fine_tunes/:fine_tune_id(("{fine-tune-id}"))
/fine_tunes/:fine_tune_id(("{fine-tune-id}")) --> /fine_tunes/:fine_tune_id/events["events"]
class /fine_tunes/:fine_tune_id/events GET
/fine_tunes/:fine_tune_id(("{fine-tune-id}")) --> /fine_tunes/:fine_tune_id/cancel>"cancel"]
class /fine_tunes/:fine_tune_id/cancel POST
class /fine_tunes/:fine_tune_id DELETE_GET
class /fine_tunes GET_POST
/["/"] --> /models["models"]
/models["models"] --> /models/:model_id["{model-id}"]
class /models/:model_id GET
class /models GET
class / OTHER
```
