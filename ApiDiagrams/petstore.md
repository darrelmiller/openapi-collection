# Swagger Petstore

OpenAPI: https://petstore.swagger.io/v2/swagger.json
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
/ --> /pet[pet]
/pet --> /pet/:petId[:petId]
/pet/:petId --> /pet/:petId/uploadImage[uploadImage]
class /pet/:petId/uploadImage POST
class /pet/:petId DELETEGETPOST
/pet --> /pet/findByStatus[findByStatus]
class /pet/findByStatus GET
/pet --> /pet/findByTags[findByTags]
class /pet/findByTags GET
class /pet POSTPUT
/ --> /store[store]
/store --> /store/order[order]
/store/order --> /store/order/:orderId[:orderId]
class /store/order/:orderId DELETEGET
class /store/order POST
/store --> /store/inventory[inventory]
class /store/inventory GET
class /store OTHER
/ --> /user[user]
/user --> /user/createWithArray[createWithArray]
class /user/createWithArray POST
/user --> /user/createWithList[createWithList]
class /user/createWithList POST
/user --> /user/:username[:username]
class /user/:username DELETEGETPUT
/user --> /user/login[login]
class /user/login GET
/user --> /user/logout[logout]
class /user/logout GET
class /user POST
class / OTHER
```
