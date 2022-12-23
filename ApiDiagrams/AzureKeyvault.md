# KeyVaultClient

OpenAPI: https://api.apis.guru/v2/specs/azure.com/keyvault/7.0-preview/swagger.yaml
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
/ --> /certificates[certificates]
/certificates --> /certificates/contacts[contacts]
class /certificates/contacts DELETEGETPUT
/certificates --> /certificates/issuers[issuers]
/certificates/issuers --> /certificates/issuers/:issuer-name[:issuer-name]
class /certificates/issuers/:issuer-name DELETEGETPATCHPUT
class /certificates/issuers GET
/certificates --> /certificates/restore[restore]
class /certificates/restore POST
/certificates --> /certificates/:certificate-name[:certificate-name]
/certificates/:certificate-name --> /certificates/:certificate-name/backup[backup]
class /certificates/:certificate-name/backup POST
/certificates/:certificate-name --> /certificates/:certificate-name/create[create]
class /certificates/:certificate-name/create POST
/certificates/:certificate-name --> /certificates/:certificate-name/import[import]
class /certificates/:certificate-name/import POST
/certificates/:certificate-name --> /certificates/:certificate-name/pending[pending]
/certificates/:certificate-name/pending --> /certificates/:certificate-name/pending/merge[merge]
class /certificates/:certificate-name/pending/merge POST
class /certificates/:certificate-name/pending DELETEGETPATCH
/certificates/:certificate-name --> /certificates/:certificate-name/policy[policy]
class /certificates/:certificate-name/policy GETPATCH
/certificates/:certificate-name --> /certificates/:certificate-name/versions[versions]
class /certificates/:certificate-name/versions GET
/certificates/:certificate-name --> /certificates/:certificate-name/:certificate-version[:certificate-version]
class /certificates/:certificate-name/:certificate-version GETPATCH
class /certificates/:certificate-name DELETE
class /certificates GET
/ --> /deletedcertificates[deletedcertificates]
/deletedcertificates --> /deletedcertificates/:certificate-name[:certificate-name]
/deletedcertificates/:certificate-name --> /deletedcertificates/:certificate-name/recover[recover]
class /deletedcertificates/:certificate-name/recover POST
class /deletedcertificates/:certificate-name DELETEGET
class /deletedcertificates GET
/ --> /deletedkeys[deletedkeys]
/deletedkeys --> /deletedkeys/:key-name[:key-name]
/deletedkeys/:key-name --> /deletedkeys/:key-name/recover[recover]
class /deletedkeys/:key-name/recover POST
class /deletedkeys/:key-name DELETEGET
class /deletedkeys GET
/ --> /deletedsecrets[deletedsecrets]
/deletedsecrets --> /deletedsecrets/:secret-name[:secret-name]
/deletedsecrets/:secret-name --> /deletedsecrets/:secret-name/recover[recover]
class /deletedsecrets/:secret-name/recover POST
class /deletedsecrets/:secret-name DELETEGET
class /deletedsecrets GET
/ --> /deletedstorage[deletedstorage]
/deletedstorage --> /deletedstorage/:storage-account-name[:storage-account-name]
/deletedstorage/:storage-account-name --> /deletedstorage/:storage-account-name/recover[recover]
class /deletedstorage/:storage-account-name/recover POST
/deletedstorage/:storage-account-name --> /deletedstorage/:storage-account-name/sas[sas]
/deletedstorage/:storage-account-name/sas --> /deletedstorage/:storage-account-name/sas/:sas-definition-name[:sas-definition-name]
/deletedstorage/:storage-account-name/sas/:sas-definition-name --> /deletedstorage/:storage-account-name/sas/:sas-definition-name/recover[recover]
class /deletedstorage/:storage-account-name/sas/:sas-definition-name/recover POST
class /deletedstorage/:storage-account-name/sas/:sas-definition-name GET
class /deletedstorage/:storage-account-name/sas GET
class /deletedstorage/:storage-account-name DELETEGET
class /deletedstorage GET
/ --> /keys[keys]
/keys --> /keys/restore[restore]
class /keys/restore POST
/keys --> /keys/:key-name[:key-name]
/keys/:key-name --> /keys/:key-name/backup[backup]
class /keys/:key-name/backup POST
/keys/:key-name --> /keys/:key-name/create[create]
class /keys/:key-name/create POST
/keys/:key-name --> /keys/:key-name/versions[versions]
class /keys/:key-name/versions GET
/keys/:key-name --> /keys/:key-name/:key-version[:key-version]
/keys/:key-name/:key-version --> /keys/:key-name/:key-version/decrypt[decrypt]
class /keys/:key-name/:key-version/decrypt POST
/keys/:key-name/:key-version --> /keys/:key-name/:key-version/encrypt[encrypt]
class /keys/:key-name/:key-version/encrypt POST
/keys/:key-name/:key-version --> /keys/:key-name/:key-version/sign[sign]
class /keys/:key-name/:key-version/sign POST
/keys/:key-name/:key-version --> /keys/:key-name/:key-version/unwrapkey[unwrapkey]
class /keys/:key-name/:key-version/unwrapkey POST
/keys/:key-name/:key-version --> /keys/:key-name/:key-version/verify[verify]
class /keys/:key-name/:key-version/verify POST
/keys/:key-name/:key-version --> /keys/:key-name/:key-version/wrapkey[wrapkey]
class /keys/:key-name/:key-version/wrapkey POST
class /keys/:key-name/:key-version GETPATCH
class /keys/:key-name DELETEPUT
class /keys GET
/ --> /secrets[secrets]
/secrets --> /secrets/restore[restore]
class /secrets/restore POST
/secrets --> /secrets/:secret-name[:secret-name]
/secrets/:secret-name --> /secrets/:secret-name/backup[backup]
class /secrets/:secret-name/backup POST
/secrets/:secret-name --> /secrets/:secret-name/versions[versions]
class /secrets/:secret-name/versions GET
/secrets/:secret-name --> /secrets/:secret-name/:secret-version[:secret-version]
class /secrets/:secret-name/:secret-version GETPATCH
class /secrets/:secret-name DELETEPUT
class /secrets GET
/ --> /storage[storage]
/storage --> /storage/restore[restore]
class /storage/restore POST
/storage --> /storage/:storage-account-name[:storage-account-name]
/storage/:storage-account-name --> /storage/:storage-account-name/backup[backup]
class /storage/:storage-account-name/backup POST
/storage/:storage-account-name --> /storage/:storage-account-name/regeneratekey[regeneratekey]
class /storage/:storage-account-name/regeneratekey POST
/storage/:storage-account-name --> /storage/:storage-account-name/sas[sas]
/storage/:storage-account-name/sas --> /storage/:storage-account-name/sas/:sas-definition-name[:sas-definition-name]
class /storage/:storage-account-name/sas/:sas-definition-name DELETEGETPATCHPUT
class /storage/:storage-account-name/sas GET
class /storage/:storage-account-name DELETEGETPATCHPUT
class /storage GET
class / OTHER
```
