# Web Search Client

OpenAPI: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/cognitiveservices/data-plane/WebSearch/stable/v1.0/WebSearch.json
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
/["/"] --> /search["search"]
class /search GET
class / OTHER
```
