# Spotify Web API

OpenAPI: https://api.apis.guru/v2/specs/spotify.com/2021.8.15/openapi.yaml
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
/["/"] --> /albums["albums"]
/albums["albums"] --> /albums/:id["{id}"]
/albums/:id["{id}"] --> /albums/:id/tracks["tracks"]
class /albums/:id/tracks GET
class /albums/:id GET
class /albums GET
/["/"] --> /artists["artists"]
/artists["artists"] --> /artists/:id["{id}"]
/artists/:id["{id}"] --> /artists/:id/albums["albums"]
class /artists/:id/albums GET
/artists/:id["{id}"] --> /artists/:id/related_artists["related-artists"]
class /artists/:id/related_artists GET
/artists/:id["{id}"] --> /artists/:id/top_tracks["top-tracks"]
class /artists/:id/top_tracks GET
class /artists/:id GET
class /artists GET
/["/"] --> /audio_analysis["audio-analysis"]
/audio_analysis["audio-analysis"] --> /audio_analysis/:id["{id}"]
class /audio_analysis/:id GET
class /audio_analysis OTHER
/["/"] --> /audio_features["audio-features"]
/audio_features["audio-features"] --> /audio_features/:id["{id}"]
class /audio_features/:id GET
class /audio_features GET
/["/"] --> /browse["browse"]
/browse["browse"] --> /browse/categories["categories"]
/browse/categories["categories"] --> /browse/categories/:category_id["{category_id}"]
/browse/categories/:category_id["{category_id}"] --> /browse/categories/:category_id/playlists["playlists"]
class /browse/categories/:category_id/playlists GET
class /browse/categories/:category_id GET
class /browse/categories GET
/browse["browse"] --> /browse/featured_playlists["featured-playlists"]
class /browse/featured_playlists GET
/browse["browse"] --> /browse/new_releases["new-releases"]
class /browse/new_releases GET
class /browse OTHER
/["/"] --> /episodes["episodes"]
/episodes["episodes"] --> /episodes/:id["{id}"]
class /episodes/:id GET
class /episodes GET
/["/"] --> /markets["markets"]
class /markets GET
/["/"] --> /me["me"]
/me["me"] --> /me/albums(("albums"))
/me/albums(("albums")) --> /me/albums/contains["contains"]
class /me/albums/contains GET
class /me/albums DELETE_GET_PUT
/me["me"] --> /me/episodes(("episodes"))
/me/episodes(("episodes")) --> /me/episodes/contains["contains"]
class /me/episodes/contains GET
class /me/episodes DELETE_GET_PUT
/me["me"] --> /me/following(("following"))
/me/following(("following")) --> /me/following/contains["contains"]
class /me/following/contains GET
class /me/following DELETE_GET_PUT
/me["me"] --> /me/player["player"]
/me/player["player"] --> /me/player/currently_playing["currently-playing"]
class /me/player/currently_playing GET
/me/player["player"] --> /me/player/devices["devices"]
class /me/player/devices GET
/me/player["player"] --> /me/player/next>"next"]
class /me/player/next POST
/me/player["player"] --> /me/player/pause["pause"]
class /me/player/pause PUT
/me/player["player"] --> /me/player/play["play"]
class /me/player/play PUT
/me/player["player"] --> /me/player/previous>"previous"]
class /me/player/previous POST
/me/player["player"] --> /me/player/queue>"queue"]
class /me/player/queue POST
/me/player["player"] --> /me/player/recently_played["recently-played"]
class /me/player/recently_played GET
/me/player["player"] --> /me/player/repeat["repeat"]
class /me/player/repeat PUT
/me/player["player"] --> /me/player/seek["seek"]
class /me/player/seek PUT
/me/player["player"] --> /me/player/shuffle["shuffle"]
class /me/player/shuffle PUT
/me/player["player"] --> /me/player/volume["volume"]
class /me/player/volume PUT
class /me/player GET_PUT
/me["me"] --> /me/playlists["playlists"]
class /me/playlists GET
/me["me"] --> /me/shows(("shows"))
/me/shows(("shows")) --> /me/shows/contains["contains"]
class /me/shows/contains GET
class /me/shows DELETE_GET_PUT
/me["me"] --> /me/top["top"]
/me/top["top"] --> /me/top/:type["{type}"]
class /me/top/:type GET
class /me/top OTHER
/me["me"] --> /me/tracks(("tracks"))
/me/tracks(("tracks")) --> /me/tracks/contains["contains"]
class /me/tracks/contains GET
class /me/tracks DELETE_GET_PUT
class /me GET
/["/"] --> /playlists["playlists"]
/playlists["playlists"] --> /playlists/:playlist_id["{playlist_id}"]
/playlists/:playlist_id["{playlist_id}"] --> /playlists/:playlist_id/followers["followers"]
/playlists/:playlist_id/followers["followers"] --> /playlists/:playlist_id/followers/contains["contains"]
class /playlists/:playlist_id/followers/contains GET
class /playlists/:playlist_id/followers DELETE_PUT
/playlists/:playlist_id["{playlist_id}"] --> /playlists/:playlist_id/images["images"]
class /playlists/:playlist_id/images GET_PUT
/playlists/:playlist_id["{playlist_id}"] --> /playlists/:playlist_id/tracks["tracks"]
class /playlists/:playlist_id/tracks DELETE_GET_POST_PUT
class /playlists/:playlist_id GET_PUT
class /playlists OTHER
/["/"] --> /recommendations["recommendations"]
/recommendations["recommendations"] --> /recommendations/available_genre_seeds["available-genre-seeds"]
class /recommendations/available_genre_seeds GET
class /recommendations GET
/["/"] --> /search["search"]
class /search GET
/["/"] --> /shows["shows"]
/shows["shows"] --> /shows/:id["{id}"]
/shows/:id["{id}"] --> /shows/:id/episodes["episodes"]
class /shows/:id/episodes GET
class /shows/:id GET
class /shows GET
/["/"] --> /tracks["tracks"]
/tracks["tracks"] --> /tracks/:id["{id}"]
class /tracks/:id GET
class /tracks GET
/["/"] --> /users["users"]
/users["users"] --> /users/:user_id["{user_id}"]
/users/:user_id["{user_id}"] --> /users/:user_id/playlists("playlists")
class /users/:user_id/playlists GET_POST
class /users/:user_id GET
class /users OTHER
class / OTHER
```
