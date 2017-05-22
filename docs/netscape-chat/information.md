# Netscape Chat Communication Information

## Future Proofing your Client

In case you want to have your client updated and ready before the server makes changes, the specification containing current future plans can be found [here](https://gist.github.com/SpoopySaitama/33f45f7bf27151542330ce3a67658ba0).

## Authentication

#### Send this message when first opening the server connection to authenticate with the server
`{"password":"your password","author":"your username"}`

#### If this is your first time authenticating with a username and it has not yet been registered, you will receive this message
`{"type":"auth","message":"You have successfully registered a new account and logged in"}`

#### If you have logged into a registered name with incorrect credentials, you will receive this message and will not be able to send messages
`{"type":"auth","message":"Those credentials are incorrect"}`

#### If you have logged into an already existing account, you will receive this message
`{"type":"auth","message":"You have successfully authenticated an already existing account"}`

## Chat Messages


#### Messages from the server will be in this format
`{"author":"chaten","type":"message","message":"hi"}`

#### Messages to the server should be in this format (They should NOT include an author string: This is disregarded by the server and replaced with the username you have authenticated with)
`{"type":"message","message":"hi"}`

## Status

#### If a user joins, you will receive a message like this
`{"type":"join","message":"username"}`

#### If a user quits, you will receive a message like this
`{"type":"quit","message":"username"}`

## Managing an Online List

When you connect to the server, you will receive a message like this containing the list of online users

`{"type":"user_list","users":["folder","zachary","stalin"]}`

This can be used to create your online user list, which you can update in realtime based on join and quit packets.
