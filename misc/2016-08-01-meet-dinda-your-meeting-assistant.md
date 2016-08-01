Title: Meet Dinda, Your Meeting Assistant
Date: 2016-08-01
Tags: snippet

Melengkapi bot yg sudah ada, mulai hari di cigadung#general **dinda** sudah mulai aktif. List perintah dapat dilihat dengan `.ms help`.

```bash
.ms new meeting - New service session (idle -> active)
.ms cancel - Cancel session (active -> idle)
.ms help - Display this message
.ms status - Display service json
.ms set reminder <s> - Set reminder interval s seconds
.participant add <u..> - Add conversation users u..
.participant remove <u..> - Remove users u..
.participant reset - Reset users to default (only host)
.participant all - Set all recognized users to active session
.title <t> - Set title of the session
.token assign <u..> - Assign speech token to users u..
.token reset - Reset / erase all tokens
.token status - Print all token related variables
.conclude - Render + gist (active -> concluded)
.reactivate - Revert / reactivate (concluded->active)
.close - End session (concluded -> idle)
```



Workflow yg simple misalnya spt ini:



```bash
# open session
.ms new meeting

# add participant
.participant add dewiprass edimulyana rifani adil arifpriyop

# cek status
.ms status

# meeting title 
.title koordinasi project batman

# recording
[any chat of the participants is captured]

# assign chat/speech token
.token assign adil arifpriyop

# cek token
.token status

# conclude -> gist
.conclude

# close session
.close
```