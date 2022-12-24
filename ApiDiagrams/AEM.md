# Adobe Experience Manager (AEM) API

OpenAPI: https://api.apis.guru/v2/specs/adobe.com/aem/3.5.0-pre.0/openapi.yaml
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
/["/"] --> /_cqactions_html>".cqactions.html"]
class /_cqactions_html POST
/["/"] --> /apps["apps"]
/apps["apps"] --> /apps/system["system"]
/apps/system["system"] --> /apps/system/config["config"]
/apps/system/config["config"] --> /apps/system/config/com_adobe_granite_auth_saml_SamlAuthenticationHandler_config>"com.adobe.granite.auth.saml.SamlAuthenticationHandler.config"]
class /apps/system/config/com_adobe_granite_auth_saml_SamlAuthenticationHandler_config POST
/apps/system/config["config"] --> /apps/system/config/com_shinesolutions_aem_passwordreset_Activator>"com.shinesolutions.aem.passwordreset.Activator"]
class /apps/system/config/com_shinesolutions_aem_passwordreset_Activator POST
/apps/system/config["config"] --> /apps/system/config/com_shinesolutions_healthcheck_hc_impl_ActiveBundleHealthCheck>"com.shinesolutions.healthcheck.hc.impl.ActiveBundleHealthCheck"]
class /apps/system/config/com_shinesolutions_healthcheck_hc_impl_ActiveBundleHealthCheck POST
/apps/system/config["config"] --> /apps/system/config/org_apache_felix_http>"org.apache.felix.http"]
class /apps/system/config/org_apache_felix_http POST
/apps/system/config["config"] --> /apps/system/config/org_apache_http_proxyconfigurator_config>"org.apache.http.proxyconfigurator.config"]
class /apps/system/config/org_apache_http_proxyconfigurator_config POST
/apps/system/config["config"] --> /apps/system/config/org_apache_sling_jcr_davex_impl_servlets_SlingDavExServlet>"org.apache.sling.jcr.davex.impl.servlets.SlingDavExServlet"]
class /apps/system/config/org_apache_sling_jcr_davex_impl_servlets_SlingDavExServlet POST
/apps/system/config["config"] --> /apps/system/config/org_apache_sling_security_impl_ReferrerFilter>"org.apache.sling.security.impl.ReferrerFilter"]
class /apps/system/config/org_apache_sling_security_impl_ReferrerFilter POST
/apps/system/config["config"] --> /apps/system/config/org_apache_sling_servlets_get_DefaultGetServlet>"org.apache.sling.servlets.get.DefaultGetServlet"]
class /apps/system/config/org_apache_sling_servlets_get_DefaultGetServlet POST
/apps/system/config["config"] --> /apps/system/config/:configNodeName>"{configNodeName}"]
class /apps/system/config/:configNodeName POST
class /apps/system/config OTHER
class /apps/system OTHER
class /apps OTHER
/["/"] --> /bin["bin"]
/bin["bin"] --> /bin/querybuilder_json("querybuilder.json")
class /bin/querybuilder_json GET_POST
class /bin OTHER
/["/"] --> /crx["crx"]
/crx["crx"] --> /crx/explorer["explorer"]
/crx/explorer["explorer"] --> /crx/explorer/ui["ui"]
/crx/explorer/ui["ui"] --> /crx/explorer/ui/setpassword_jsp>"setpassword.jsp"]
class /crx/explorer/ui/setpassword_jsp POST
class /crx/explorer/ui OTHER
class /crx/explorer OTHER
/crx["crx"] --> /crx/packmgr["packmgr"]
/crx/packmgr["packmgr"] --> /crx/packmgr/installstatus_jsp["installstatus.jsp"]
class /crx/packmgr/installstatus_jsp GET
/crx/packmgr["packmgr"] --> /crx/packmgr/service_jsp>"service.jsp"]
class /crx/packmgr/service_jsp POST
/crx/packmgr["packmgr"] --> /crx/packmgr/service["service"]
/crx/packmgr/service["service"] --> /crx/packmgr/service/_json[".json"]
/crx/packmgr/service/_json[".json"] --> /crx/packmgr/service/_json/:path>"{path}"]
class /crx/packmgr/service/_json/:path POST
class /crx/packmgr/service/_json OTHER
/crx/packmgr/service["service"] --> /crx/packmgr/service/script_html["script.html"]
class /crx/packmgr/service/script_html GET
class /crx/packmgr/service OTHER
/crx/packmgr["packmgr"] --> /crx/packmgr/update_jsp>"update.jsp"]
class /crx/packmgr/update_jsp POST
class /crx/packmgr OTHER
/crx["crx"] --> /crx/server["server"]
/crx/server["server"] --> /crx/server/crx_def_ault["crx.default"]
/crx/server/crx_def_ault["crx.default"] --> /crx/server/crx_def_ault/jcr:root["jcr:root"]
/crx/server/crx_def_ault/jcr:root["jcr:root"] --> /crx/server/crx_def_ault/jcr:root/_1_json[".1.json"]
class /crx/server/crx_def_ault/jcr:root/_1_json GET
class /crx/server/crx_def_ault/jcr:root OTHER
class /crx/server/crx_def_ault OTHER
class /crx/server OTHER
class /crx OTHER
/["/"] --> /etc["etc"]
/etc["etc"] --> /etc/packages["packages"]
/etc/packages["packages"] --> /etc/packages/:group["{group}"]
/etc/packages/:group["{group}"] --> /etc/packages/:group/:name_:version_zip["{name}-{version}.zip"]
/etc/packages/:group/:name_:version_zip["{name}-{version}.zip"] --> /etc/packages/:group/:name_:version_zip/jcr:content["jcr:content"]
/etc/packages/:group/:name_:version_zip/jcr:content["jcr:content"] --> /etc/packages/:group/:name_:version_zip/jcr:content/vlt:definition["vlt:definition"]
/etc/packages/:group/:name_:version_zip/jcr:content/vlt:definition["vlt:definition"] --> /etc/packages/:group/:name_:version_zip/jcr:content/vlt:definition/filter_tidy_2_json["filter.tidy.2.json"]
class /etc/packages/:group/:name_:version_zip/jcr:content/vlt:definition/filter_tidy_2_json GET
class /etc/packages/:group/:name_:version_zip/jcr:content/vlt:definition OTHER
class /etc/packages/:group/:name_:version_zip/jcr:content OTHER
class /etc/packages/:group/:name_:version_zip GET
class /etc/packages/:group OTHER
class /etc/packages OTHER
/etc["etc"] --> /etc/replication["replication"]
/etc/replication["replication"] --> /etc/replication/agents_:runmode__1_json["agents.{runmode}.-1.json"]
class /etc/replication/agents_:runmode__1_json GET
/etc/replication["replication"] --> /etc/replication/agents_:runmode["agents.{runmode}"]
/etc/replication/agents_:runmode["agents.{runmode}"] --> /etc/replication/agents_:runmode/:name["{name}"]
class /etc/replication/agents_:runmode/:name DELETE_GET_POST
class /etc/replication/agents_:runmode OTHER
/etc/replication["replication"] --> /etc/replication/treeactivation_html>"treeactivation.html"]
class /etc/replication/treeactivation_html POST
class /etc/replication OTHER
/etc["etc"] --> /etc/truststore>"truststore"]
/etc/truststore>"truststore"] --> /etc/truststore/truststore_p12["truststore.p12"]
class /etc/truststore/truststore_p12 GET
class /etc/truststore POST
class /etc OTHER
/["/"] --> /libs["libs"]
/libs["libs"] --> /libs/granite["granite"]
/libs/granite["granite"] --> /libs/granite/core["core"]
/libs/granite/core["core"] --> /libs/granite/core/content["content"]
/libs/granite/core/content["content"] --> /libs/granite/core/content/login_html["login.html"]
class /libs/granite/core/content/login_html GET
class /libs/granite/core/content OTHER
class /libs/granite/core OTHER
/libs/granite["granite"] --> /libs/granite/security["security"]
/libs/granite/security["security"] --> /libs/granite/security/post["post"]
/libs/granite/security/post["post"] --> /libs/granite/security/post/authorizables>"authorizables"]
class /libs/granite/security/post/authorizables POST
/libs/granite/security/post["post"] --> /libs/granite/security/post/sslSetup_html>"sslSetup.html"]
class /libs/granite/security/post/sslSetup_html POST
/libs/granite/security/post["post"] --> /libs/granite/security/post/truststore>"truststore"]
class /libs/granite/security/post/truststore POST
class /libs/granite/security/post OTHER
/libs/granite/security["security"] --> /libs/granite/security/truststore_json["truststore.json"]
class /libs/granite/security/truststore_json GET
class /libs/granite/security OTHER
class /libs/granite OTHER
class /libs OTHER
/["/"] --> /system["system"]
/system["system"] --> /system/console["console"]
/system/console["console"] --> /system/console/bundles["bundles"]
/system/console/bundles["bundles"] --> /system/console/bundles/:name>"{name}"]
class /system/console/bundles/:name POST
class /system/console/bundles OTHER
/system/console["console"] --> /system/console/configMgr["configMgr"]
/system/console/configMgr["configMgr"] --> /system/console/configMgr/com_adobe_granite_auth_saml_SamlAuthenticationHandler>"com.adobe.granite.auth.saml.SamlAuthenticationHandler"]
class /system/console/configMgr/com_adobe_granite_auth_saml_SamlAuthenticationHandler POST
class /system/console/configMgr GET
/system/console["console"] --> /system/console/jmx["jmx"]
/system/console/jmx["jmx"] --> /system/console/jmx/com_adobe_granite:type=Repository["com.adobe.granite:type=Repository"]
/system/console/jmx/com_adobe_granite:type=Repository["com.adobe.granite:type=Repository"] --> /system/console/jmx/com_adobe_granite:type=Repository/op["op"]
/system/console/jmx/com_adobe_granite:type=Repository/op["op"] --> /system/console/jmx/com_adobe_granite:type=Repository/op/:action>"{action}"]
class /system/console/jmx/com_adobe_granite:type=Repository/op/:action POST
class /system/console/jmx/com_adobe_granite:type=Repository/op OTHER
class /system/console/jmx/com_adobe_granite:type=Repository OTHER
class /system/console/jmx OTHER
/system/console["console"] --> /system/console/status_productinfo_json["status-productinfo.json"]
class /system/console/status_productinfo_json GET
class /system/console OTHER
/system["system"] --> /system/health["health"]
class /system/health GET
class /system OTHER
/["/"] --> /:intermediatePath["{intermediatePath}"]
/:intermediatePath["{intermediatePath}"] --> /:intermediatePath/:authorizableId_ks_html>"{authorizableId}.ks.html"]
class /:intermediatePath/:authorizableId_ks_html POST
/:intermediatePath["{intermediatePath}"] --> /:intermediatePath/:authorizableId_ks_json["{authorizableId}.ks.json"]
class /:intermediatePath/:authorizableId_ks_json GET
/:intermediatePath["{intermediatePath}"] --> /:intermediatePath/:authorizableId["{authorizableId}"]
/:intermediatePath/:authorizableId["{authorizableId}"] --> /:intermediatePath/:authorizableId/keystore["keystore"]
/:intermediatePath/:authorizableId/keystore["keystore"] --> /:intermediatePath/:authorizableId/keystore/store_p12["store.p12"]
class /:intermediatePath/:authorizableId/keystore/store_p12 GET
class /:intermediatePath/:authorizableId/keystore OTHER
class /:intermediatePath/:authorizableId OTHER
class /:intermediatePath OTHER
/["/"] --> /:path>"{path}"]
/:path>"{path}"] --> /:path/:name["{name}"]
class /:path/:name DELETE_GET_POST
/:path>"{path}"] --> /:path/:name_rw_html>"{name}.rw.html"]
class /:path/:name_rw_html POST
class /:path POST
class / OTHER
```
