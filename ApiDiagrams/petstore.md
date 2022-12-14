# Swagger Petstore

OpenAPI: https://petstore.swagger.io/v2/swagger.json
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
/["/"] --> /pet["pet"]
/pet["pet"] --> /pet/:petId["{petId}"]
/pet/:petId["{petId}"] --> /pet/:petId/uploadImage>"uploadImage"]
class /pet/:petId/uploadImage POST
class /pet/:petId DELETE_GET_POST
/pet["pet"] --> /pet/findByStatus["findByStatus"]
class /pet/findByStatus GET
/pet["pet"] --> /pet/findByTags["findByTags"]
class /pet/findByTags GET
class /pet POST_PUT
/["/"] --> /store["store"]
/store["store"] --> /store/order>"order"]
/store/order>"order"] --> /store/order/:orderId(("{orderId}"))
class /store/order/:orderId DELETE_GET
class /store/order POST
/store["store"] --> /store/inventory["inventory"]
class /store/inventory GET
class /store OTHER
/["/"] --> /user>"user"]
/user>"user"] --> /user/createWithArray>"createWithArray"]
class /user/createWithArray POST
/user>"user"] --> /user/createWithList>"createWithList"]
class /user/createWithList POST
/user>"user"] --> /user/:username(("{username}"))
class /user/:username DELETE_GET_PUT
/user>"user"] --> /user/login["login"]
class /user/login GET
/user>"user"] --> /user/logout["logout"]
class /user/logout GET
class /user POST
class / OTHER
```
