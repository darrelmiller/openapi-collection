# Notion API - Public Beta

OpenAPI: https://api.apis.guru/v2/specs/notion.com/1.0.0/openapi.yaml
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
/ --> /v1[v1]
/v1 --> /v1/blocks[blocks]
/v1/blocks --> /v1/blocks/:id[:id]
/v1/blocks/:id --> /v1/blocks/:id/children[children]
class /v1/blocks/:id/children GETPATCH
class /v1/blocks/:id GETPATCH
class /v1/blocks OTHER
/v1 --> /v1/databases[databases]
/v1/databases --> /v1/databases/:id[:id]
/v1/databases/:id --> /v1/databases/:id/query[query]
class /v1/databases/:id/query POST
class /v1/databases/:id GETPATCH
class /v1/databases OTHER
/v1 --> /v1/pages[pages]
/v1/pages --> /v1/pages/:id[:id]
class /v1/pages/:id GETPATCH
class /v1/pages OTHER
/v1 --> /v1/users[users]
/v1/users --> /v1/users/:id[:id]
class /v1/users/:id GET
class /v1/users OTHER
class /v1 OTHER
class / OTHER
```
