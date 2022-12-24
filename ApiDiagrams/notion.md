# Notion API - Public Beta

OpenAPI: https://api.apis.guru/v2/specs/notion.com/1.0.0/openapi.yaml
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
/["/"] --> /v1["v1"]
/v1["v1"] --> /v1/blocks["blocks"]
/v1/blocks["blocks"] --> /v1/blocks/:id["{id}"]
/v1/blocks/:id["{id}"] --> /v1/blocks/:id/children["children"]
class /v1/blocks/:id/children GET_PATCH
class /v1/blocks/:id GET_PATCH
class /v1/blocks OTHER
/v1["v1"] --> /v1/databases["databases"]
/v1/databases["databases"] --> /v1/databases/:id["{id}"]
/v1/databases/:id["{id}"] --> /v1/databases/:id/query>"query"]
class /v1/databases/:id/query POST
class /v1/databases/:id GET_PATCH
class /v1/databases OTHER
/v1["v1"] --> /v1/pages["pages"]
/v1/pages["pages"] --> /v1/pages/:id["{id}"]
class /v1/pages/:id GET_PATCH
class /v1/pages OTHER
/v1["v1"] --> /v1/users["users"]
/v1/users["users"] --> /v1/users/:id["{id}"]
class /v1/users/:id GET
class /v1/users OTHER
class /v1 OTHER
class / OTHER
```
