# KeyVaultClient

OpenAPI: https://api.apis.guru/v2/specs/azure.com/keyvault/7.0-preview/swagger.yaml
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
/["/"] --> /certificates["certificates"]
/certificates["certificates"] --> /certificates/contacts(("contacts"))
class /certificates/contacts DELETE_GET_PUT
/certificates["certificates"] --> /certificates/issuers["issuers"]
/certificates/issuers["issuers"] --> /certificates/issuers/:issuer_name(("{issuer-name}"))
class /certificates/issuers/:issuer_name DELETE_GET_PATCH_PUT
class /certificates/issuers GET
/certificates["certificates"] --> /certificates/restore>"restore"]
class /certificates/restore POST
/certificates["certificates"] --> /certificates/:certificate_name{"{certificate-name}"}
/certificates/:certificate_name{"{certificate-name}"} --> /certificates/:certificate_name/backup>"backup"]
class /certificates/:certificate_name/backup POST
/certificates/:certificate_name{"{certificate-name}"} --> /certificates/:certificate_name/create>"create"]
class /certificates/:certificate_name/create POST
/certificates/:certificate_name{"{certificate-name}"} --> /certificates/:certificate_name/import>"import"]
class /certificates/:certificate_name/import POST
/certificates/:certificate_name{"{certificate-name}"} --> /certificates/:certificate_name/pending(("pending"))
/certificates/:certificate_name/pending(("pending")) --> /certificates/:certificate_name/pending/merge>"merge"]
class /certificates/:certificate_name/pending/merge POST
class /certificates/:certificate_name/pending DELETE_GET_PATCH
/certificates/:certificate_name{"{certificate-name}"} --> /certificates/:certificate_name/policy["policy"]
class /certificates/:certificate_name/policy GET_PATCH
/certificates/:certificate_name{"{certificate-name}"} --> /certificates/:certificate_name/versions["versions"]
class /certificates/:certificate_name/versions GET
/certificates/:certificate_name{"{certificate-name}"} --> /certificates/:certificate_name/:certificate_version["{certificate-version}"]
class /certificates/:certificate_name/:certificate_version GET_PATCH
class /certificates/:certificate_name DELETE
class /certificates GET
/["/"] --> /deletedcertificates["deletedcertificates"]
/deletedcertificates["deletedcertificates"] --> /deletedcertificates/:certificate_name(("{certificate-name}"))
/deletedcertificates/:certificate_name(("{certificate-name}")) --> /deletedcertificates/:certificate_name/recover>"recover"]
class /deletedcertificates/:certificate_name/recover POST
class /deletedcertificates/:certificate_name DELETE_GET
class /deletedcertificates GET
/["/"] --> /deletedkeys["deletedkeys"]
/deletedkeys["deletedkeys"] --> /deletedkeys/:key_name(("{key-name}"))
/deletedkeys/:key_name(("{key-name}")) --> /deletedkeys/:key_name/recover>"recover"]
class /deletedkeys/:key_name/recover POST
class /deletedkeys/:key_name DELETE_GET
class /deletedkeys GET
/["/"] --> /deletedsecrets["deletedsecrets"]
/deletedsecrets["deletedsecrets"] --> /deletedsecrets/:secret_name(("{secret-name}"))
/deletedsecrets/:secret_name(("{secret-name}")) --> /deletedsecrets/:secret_name/recover>"recover"]
class /deletedsecrets/:secret_name/recover POST
class /deletedsecrets/:secret_name DELETE_GET
class /deletedsecrets GET
/["/"] --> /deletedstorage["deletedstorage"]
/deletedstorage["deletedstorage"] --> /deletedstorage/:storage_account_name(("{storage-account-name}"))
/deletedstorage/:storage_account_name(("{storage-account-name}")) --> /deletedstorage/:storage_account_name/recover>"recover"]
class /deletedstorage/:storage_account_name/recover POST
/deletedstorage/:storage_account_name(("{storage-account-name}")) --> /deletedstorage/:storage_account_name/sas["sas"]
/deletedstorage/:storage_account_name/sas["sas"] --> /deletedstorage/:storage_account_name/sas/:sas_definition_name["{sas-definition-name}"]
/deletedstorage/:storage_account_name/sas/:sas_definition_name["{sas-definition-name}"] --> /deletedstorage/:storage_account_name/sas/:sas_definition_name/recover>"recover"]
class /deletedstorage/:storage_account_name/sas/:sas_definition_name/recover POST
class /deletedstorage/:storage_account_name/sas/:sas_definition_name GET
class /deletedstorage/:storage_account_name/sas GET
class /deletedstorage/:storage_account_name DELETE_GET
class /deletedstorage GET
/["/"] --> /keys["keys"]
/keys["keys"] --> /keys/restore>"restore"]
class /keys/restore POST
/keys["keys"] --> /keys/:key_name["{key-name}"]
/keys/:key_name["{key-name}"] --> /keys/:key_name/backup>"backup"]
class /keys/:key_name/backup POST
/keys/:key_name["{key-name}"] --> /keys/:key_name/create>"create"]
class /keys/:key_name/create POST
/keys/:key_name["{key-name}"] --> /keys/:key_name/versions["versions"]
class /keys/:key_name/versions GET
/keys/:key_name["{key-name}"] --> /keys/:key_name/:key_version["{key-version}"]
/keys/:key_name/:key_version["{key-version}"] --> /keys/:key_name/:key_version/decrypt>"decrypt"]
class /keys/:key_name/:key_version/decrypt POST
/keys/:key_name/:key_version["{key-version}"] --> /keys/:key_name/:key_version/encrypt>"encrypt"]
class /keys/:key_name/:key_version/encrypt POST
/keys/:key_name/:key_version["{key-version}"] --> /keys/:key_name/:key_version/sign>"sign"]
class /keys/:key_name/:key_version/sign POST
/keys/:key_name/:key_version["{key-version}"] --> /keys/:key_name/:key_version/unwrapkey>"unwrapkey"]
class /keys/:key_name/:key_version/unwrapkey POST
/keys/:key_name/:key_version["{key-version}"] --> /keys/:key_name/:key_version/verify>"verify"]
class /keys/:key_name/:key_version/verify POST
/keys/:key_name/:key_version["{key-version}"] --> /keys/:key_name/:key_version/wrapkey>"wrapkey"]
class /keys/:key_name/:key_version/wrapkey POST
class /keys/:key_name/:key_version GET_PATCH
class /keys/:key_name DELETE_PUT
class /keys GET
/["/"] --> /secrets["secrets"]
/secrets["secrets"] --> /secrets/restore>"restore"]
class /secrets/restore POST
/secrets["secrets"] --> /secrets/:secret_name["{secret-name}"]
/secrets/:secret_name["{secret-name}"] --> /secrets/:secret_name/backup>"backup"]
class /secrets/:secret_name/backup POST
/secrets/:secret_name["{secret-name}"] --> /secrets/:secret_name/versions["versions"]
class /secrets/:secret_name/versions GET
/secrets/:secret_name["{secret-name}"] --> /secrets/:secret_name/:secret_version["{secret-version}"]
class /secrets/:secret_name/:secret_version GET_PATCH
class /secrets/:secret_name DELETE_PUT
class /secrets GET
/["/"] --> /storage["storage"]
/storage["storage"] --> /storage/restore>"restore"]
class /storage/restore POST
/storage["storage"] --> /storage/:storage_account_name(("{storage-account-name}"))
/storage/:storage_account_name(("{storage-account-name}")) --> /storage/:storage_account_name/backup>"backup"]
class /storage/:storage_account_name/backup POST
/storage/:storage_account_name(("{storage-account-name}")) --> /storage/:storage_account_name/regeneratekey>"regeneratekey"]
class /storage/:storage_account_name/regeneratekey POST
/storage/:storage_account_name(("{storage-account-name}")) --> /storage/:storage_account_name/sas["sas"]
/storage/:storage_account_name/sas["sas"] --> /storage/:storage_account_name/sas/:sas_definition_name(("{sas-definition-name}"))
class /storage/:storage_account_name/sas/:sas_definition_name DELETE_GET_PATCH_PUT
class /storage/:storage_account_name/sas GET
class /storage/:storage_account_name DELETE_GET_PATCH_PUT
class /storage GET
class / OTHER
```
