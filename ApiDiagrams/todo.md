# Simple Todo API

OpenAPI: https://app-api-nnzrpdbgmm5ec.azurewebsites.net/openapi.yaml
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
/ --> /lists[lists]
/lists --> /lists/:listId[:listId]
/lists/:listId --> /lists/:listId/items[items]
/lists/:listId/items --> /lists/:listId/items/:itemId[:itemId]
class /lists/:listId/items/:itemId DELETEGETPUT
/lists/:listId/items --> /lists/:listId/items/state[state]
/lists/:listId/items/state --> /lists/:listId/items/state/:state[:state]
class /lists/:listId/items/state/:state GETPUT
class /lists/:listId/items/state OTHER
class /lists/:listId/items GETPOST
class /lists/:listId DELETEGETPUT
class /lists GETPOST
class / OTHER
```
