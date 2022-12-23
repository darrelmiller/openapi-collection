# OpenAI API

<div>
<span style="padding:2px;background-color:lightSteelBlue">GET</span>
<span style="padding:2px;background-color:SteelBlue">POST</span>
<span style="padding:2px;background-color:forestGreen">GET POST</span>
<span style="padding:2px;background-color:yellowGreen">GET PATCH DELETE</span>
<span style="padding:2px;background-color:olive">GET PUT DELETE</span>
<span style="padding:2px;background-color:darkseagreen">GET DELETE</span>
<span style="padding:2px;background-color:tomato">DELETE</span>
</div>

`
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
/ --> /engines[engines]
/engines --> /engines/:engine_id[:engine_id]
/engines/:engine_id --> /engines/:engine_id/search[search]
class /engines/:engine_id/search POST
class /engines/:engine_id GET
class /engines GET
/ --> /completions[completions]
class /completions POST
/ --> /edits[edits]
class /edits POST
/ --> /images[images]
/images --> /images/generations[generations]
class /images/generations POST
/images --> /images/edits[edits]
class /images/edits POST
/images --> /images/variations[variations]
class /images/variations POST
class /images OTHER
/ --> /embeddings[embeddings]
class /embeddings POST
/ --> /files[files]
/files --> /files/:file_id[:file_id]
/files/:file_id --> /files/:file_id/content[content]
class /files/:file_id/content GET
class /files/:file_id DELETEGET
class /files GETPOST
/ --> /answers[answers]
class /answers POST
/ --> /classifications[classifications]
class /classifications POST
/ --> /fine-tunes[fine-tunes]
/fine-tunes --> /fine-tunes/:fine_tune_id[:fine_tune_id]
/fine-tunes/:fine_tune_id --> /fine-tunes/:fine_tune_id/cancel[cancel]
class /fine-tunes/:fine_tune_id/cancel POST
/fine-tunes/:fine_tune_id --> /fine-tunes/:fine_tune_id/events[events]
class /fine-tunes/:fine_tune_id/events GET
class /fine-tunes/:fine_tune_id GET
class /fine-tunes GETPOST
/ --> /models[models]
/models --> /models/:model[:model]
class /models/:model DELETEGET
class /models GET
/ --> /moderations[moderations]
class /moderations POST
class / OTHER
```
