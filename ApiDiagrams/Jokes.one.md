# Jokes One API

OpenAPI: https://api.jokes.one/yaml/jokes.one.openapi.yaml?v9
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
/["/"] --> /jod["jod"]
/jod["jod"] --> /jod/categories["categories"]
class /jod/categories GET
class /jod GET
/["/"] --> /joke(("joke"))
/joke(("joke")) --> /joke/random["random"]
class /joke/random GET
/joke(("joke")) --> /joke/search["search"]
class /joke/search GET
/joke(("joke")) --> /joke/categories["categories"]
/joke/categories["categories"] --> /joke/categories/search["search"]
class /joke/categories/search GET
class /joke/categories OTHER
/joke(("joke")) --> /joke/list["list"]
class /joke/list GET
/joke(("joke")) --> /joke/tags["tags"]
/joke/tags["tags"] --> /joke/tags/add>"add"]
class /joke/tags/add POST
/joke/tags["tags"] --> /joke/tags/remove>"remove"]
class /joke/tags/remove POST
class /joke/tags OTHER
class /joke DELETE_GET_PATCH_PUT
class / OTHER
```
