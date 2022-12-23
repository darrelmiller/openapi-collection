# Jokes One API

OpenAPI: https://api.jokes.one/yaml/jokes.one.openapi.yaml?v9
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
/ --> /jod[jod]
/jod --> /jod/categories[categories]
class /jod/categories GET
class /jod GET
/ --> /joke[joke]
/joke --> /joke/random[random]
class /joke/random GET
/joke --> /joke/search[search]
class /joke/search GET
/joke --> /joke/categories[categories]
/joke/categories --> /joke/categories/search[search]
class /joke/categories/search GET
class /joke/categories OTHER
/joke --> /joke/list[list]
class /joke/list GET
/joke --> /joke/tags[tags]
/joke/tags --> /joke/tags/add[add]
class /joke/tags/add POST
/joke/tags --> /joke/tags/remove[remove]
class /joke/tags/remove POST
class /joke/tags OTHER
class /joke DELETEGETPATCHPUT
class / OTHER
```
