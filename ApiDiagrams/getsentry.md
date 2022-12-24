# API Reference

OpenAPI: https://raw.githubusercontent.com/getsentry/sentry/master/api-docs/openapi.json
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
/["/"] --> /api["api"]
/api["api"] --> /api/0["0"]
/api/0["0"] --> /api/0/organizations["organizations"]
/api/0/organizations["organizations"] --> /api/0/organizations/:organization_slug["{organization_slug}"]
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/teams["teams"]
class /api/0/organizations/:organization_slug/teams OTHER
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/eventids["eventids"]
/api/0/organizations/:organization_slug/eventids["eventids"] --> /api/0/organizations/:organization_slug/eventids/:event_id["{event_id}"]
class /api/0/organizations/:organization_slug/eventids/:event_id OTHER
class /api/0/organizations/:organization_slug/eventids OTHER
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/repos["repos"]
/api/0/organizations/:organization_slug/repos["repos"] --> /api/0/organizations/:organization_slug/repos/:repo_id["{repo_id}"]
/api/0/organizations/:organization_slug/repos/:repo_id["{repo_id}"] --> /api/0/organizations/:organization_slug/repos/:repo_id/commits["commits"]
class /api/0/organizations/:organization_slug/repos/:repo_id/commits OTHER
class /api/0/organizations/:organization_slug/repos/:repo_id OTHER
class /api/0/organizations/:organization_slug/repos OTHER
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/stats["stats"]
class /api/0/organizations/:organization_slug/stats OTHER
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/sessions["sessions"]
class /api/0/organizations/:organization_slug/sessions OTHER
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/users["users"]
class /api/0/organizations/:organization_slug/users OTHER
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/shortids["shortids"]
/api/0/organizations/:organization_slug/shortids["shortids"] --> /api/0/organizations/:organization_slug/shortids/:short_id["{short_id}"]
class /api/0/organizations/:organization_slug/shortids/:short_id OTHER
class /api/0/organizations/:organization_slug/shortids OTHER
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/releases["releases"]
/api/0/organizations/:organization_slug/releases["releases"] --> /api/0/organizations/:organization_slug/releases/:version["{version}"]
/api/0/organizations/:organization_slug/releases/:version["{version}"] --> /api/0/organizations/:organization_slug/releases/:version/files["files"]
/api/0/organizations/:organization_slug/releases/:version/files["files"] --> /api/0/organizations/:organization_slug/releases/:version/files/:file_id["{file_id}"]
class /api/0/organizations/:organization_slug/releases/:version/files/:file_id OTHER
class /api/0/organizations/:organization_slug/releases/:version/files OTHER
/api/0/organizations/:organization_slug/releases/:version["{version}"] --> /api/0/organizations/:organization_slug/releases/:version/commits["commits"]
class /api/0/organizations/:organization_slug/releases/:version/commits OTHER
/api/0/organizations/:organization_slug/releases/:version["{version}"] --> /api/0/organizations/:organization_slug/releases/:version/commitfiles["commitfiles"]
class /api/0/organizations/:organization_slug/releases/:version/commitfiles OTHER
/api/0/organizations/:organization_slug/releases/:version["{version}"] --> /api/0/organizations/:organization_slug/releases/:version/deploys["deploys"]
class /api/0/organizations/:organization_slug/releases/:version/deploys OTHER
class /api/0/organizations/:organization_slug/releases/:version OTHER
class /api/0/organizations/:organization_slug/releases OTHER
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/sentry_app_installations["sentry-app-installations"]
class /api/0/organizations/:organization_slug/sentry_app_installations OTHER
/api/0/organizations/:organization_slug["{organization_slug}"] --> /api/0/organizations/:organization_slug/scim["scim"]
/api/0/organizations/:organization_slug/scim["scim"] --> /api/0/organizations/:organization_slug/scim/v2["v2"]
/api/0/organizations/:organization_slug/scim/v2["v2"] --> /api/0/organizations/:organization_slug/scim/v2/Groups["Groups"]
class /api/0/organizations/:organization_slug/scim/v2/Groups OTHER
class /api/0/organizations/:organization_slug/scim/v2 OTHER
class /api/0/organizations/:organization_slug/scim OTHER
class /api/0/organizations/:organization_slug OTHER
class /api/0/organizations OTHER
/api/0["0"] --> /api/0/teams["teams"]
/api/0/teams["teams"] --> /api/0/teams/:organization_slug["{organization_slug}"]
/api/0/teams/:organization_slug["{organization_slug}"] --> /api/0/teams/:organization_slug/:team_slug["{team_slug}"]
/api/0/teams/:organization_slug/:team_slug["{team_slug}"] --> /api/0/teams/:organization_slug/:team_slug/projects["projects"]
class /api/0/teams/:organization_slug/:team_slug/projects OTHER
/api/0/teams/:organization_slug/:team_slug["{team_slug}"] --> /api/0/teams/:organization_slug/:team_slug/stats["stats"]
class /api/0/teams/:organization_slug/:team_slug/stats OTHER
class /api/0/teams/:organization_slug/:team_slug OTHER
class /api/0/teams/:organization_slug OTHER
class /api/0/teams OTHER
/api/0["0"] --> /api/0/projects["projects"]
/api/0/projects["projects"] --> /api/0/projects/:organization_slug["{organization_slug}"]
/api/0/projects/:organization_slug["{organization_slug}"] --> /api/0/projects/:organization_slug/:project_slug["{project_slug}"]
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/files["files"]
/api/0/projects/:organization_slug/:project_slug/files["files"] --> /api/0/projects/:organization_slug/:project_slug/files/dsyms["dsyms"]
class /api/0/projects/:organization_slug/:project_slug/files/dsyms OTHER
class /api/0/projects/:organization_slug/:project_slug/files OTHER
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/users["users"]
class /api/0/projects/:organization_slug/:project_slug/users OTHER
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/tags["tags"]
/api/0/projects/:organization_slug/:project_slug/tags["tags"] --> /api/0/projects/:organization_slug/:project_slug/tags/:key["{key}"]
/api/0/projects/:organization_slug/:project_slug/tags/:key["{key}"] --> /api/0/projects/:organization_slug/:project_slug/tags/:key/values["values"]
class /api/0/projects/:organization_slug/:project_slug/tags/:key/values OTHER
class /api/0/projects/:organization_slug/:project_slug/tags/:key OTHER
class /api/0/projects/:organization_slug/:project_slug/tags OTHER
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/stats["stats"]
class /api/0/projects/:organization_slug/:project_slug/stats OTHER
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/user_feedback["user-feedback"]
class /api/0/projects/:organization_slug/:project_slug/user_feedback OTHER
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/keys["keys"]
/api/0/projects/:organization_slug/:project_slug/keys["keys"] --> /api/0/projects/:organization_slug/:project_slug/keys/:key_id["{key_id}"]
class /api/0/projects/:organization_slug/:project_slug/keys/:key_id OTHER
class /api/0/projects/:organization_slug/:project_slug/keys OTHER
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/hooks["hooks"]
/api/0/projects/:organization_slug/:project_slug/hooks["hooks"] --> /api/0/projects/:organization_slug/:project_slug/hooks/:hook_id["{hook_id}"]
class /api/0/projects/:organization_slug/:project_slug/hooks/:hook_id OTHER
class /api/0/projects/:organization_slug/:project_slug/hooks OTHER
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/events["events"]
/api/0/projects/:organization_slug/:project_slug/events["events"] --> /api/0/projects/:organization_slug/:project_slug/events/:event_id["{event_id}"]
class /api/0/projects/:organization_slug/:project_slug/events/:event_id OTHER
class /api/0/projects/:organization_slug/:project_slug/events OTHER
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/issues["issues"]
class /api/0/projects/:organization_slug/:project_slug/issues OTHER
/api/0/projects/:organization_slug/:project_slug["{project_slug}"] --> /api/0/projects/:organization_slug/:project_slug/releases["releases"]
/api/0/projects/:organization_slug/:project_slug/releases["releases"] --> /api/0/projects/:organization_slug/:project_slug/releases/:version["{version}"]
/api/0/projects/:organization_slug/:project_slug/releases/:version["{version}"] --> /api/0/projects/:organization_slug/:project_slug/releases/:version/files["files"]
/api/0/projects/:organization_slug/:project_slug/releases/:version/files["files"] --> /api/0/projects/:organization_slug/:project_slug/releases/:version/files/:file_id["{file_id}"]
class /api/0/projects/:organization_slug/:project_slug/releases/:version/files/:file_id OTHER
class /api/0/projects/:organization_slug/:project_slug/releases/:version/files OTHER
/api/0/projects/:organization_slug/:project_slug/releases/:version["{version}"] --> /api/0/projects/:organization_slug/:project_slug/releases/:version/commits["commits"]
class /api/0/projects/:organization_slug/:project_slug/releases/:version/commits OTHER
/api/0/projects/:organization_slug/:project_slug/releases/:version["{version}"] --> /api/0/projects/:organization_slug/:project_slug/releases/:version/resolved["resolved"]
class /api/0/projects/:organization_slug/:project_slug/releases/:version/resolved OTHER
class /api/0/projects/:organization_slug/:project_slug/releases/:version OTHER
class /api/0/projects/:organization_slug/:project_slug/releases OTHER
class /api/0/projects/:organization_slug/:project_slug OTHER
class /api/0/projects/:organization_slug OTHER
class /api/0/projects OTHER
/api/0["0"] --> /api/0/issues["issues"]
/api/0/issues["issues"] --> /api/0/issues/:issue_id["{issue_id}"]
/api/0/issues/:issue_id["{issue_id}"] --> /api/0/issues/:issue_id/tags["tags"]
/api/0/issues/:issue_id/tags["tags"] --> /api/0/issues/:issue_id/tags/:key["{key}"]
/api/0/issues/:issue_id/tags/:key["{key}"] --> /api/0/issues/:issue_id/tags/:key/values["values"]
class /api/0/issues/:issue_id/tags/:key/values OTHER
class /api/0/issues/:issue_id/tags/:key OTHER
class /api/0/issues/:issue_id/tags OTHER
/api/0/issues/:issue_id["{issue_id}"] --> /api/0/issues/:issue_id/hashes["hashes"]
class /api/0/issues/:issue_id/hashes OTHER
/api/0/issues/:issue_id["{issue_id}"] --> /api/0/issues/:issue_id/events["events"]
/api/0/issues/:issue_id/events["events"] --> /api/0/issues/:issue_id/events/oldest["oldest"]
class /api/0/issues/:issue_id/events/oldest OTHER
/api/0/issues/:issue_id/events["events"] --> /api/0/issues/:issue_id/events/latest["latest"]
class /api/0/issues/:issue_id/events/latest OTHER
class /api/0/issues/:issue_id/events OTHER
class /api/0/issues/:issue_id OTHER
class /api/0/issues OTHER
/api/0["0"] --> /api/0/sentry_app_installations["sentry-app-installations"]
/api/0/sentry_app_installations["sentry-app-installations"] --> /api/0/sentry_app_installations/:uuid["{uuid}"]
/api/0/sentry_app_installations/:uuid["{uuid}"] --> /api/0/sentry_app_installations/:uuid/external_issues["external-issues"]
/api/0/sentry_app_installations/:uuid/external_issues["external-issues"] --> /api/0/sentry_app_installations/:uuid/external_issues/:external_issue_id["{external_issue_id}"]
class /api/0/sentry_app_installations/:uuid/external_issues/:external_issue_id OTHER
class /api/0/sentry_app_installations/:uuid/external_issues OTHER
class /api/0/sentry_app_installations/:uuid OTHER
class /api/0/sentry_app_installations OTHER
class /api/0 OTHER
class /api OTHER
class / OTHER
```
