# Netscape Chat Communication Information

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


#### Messages to _and_ from the server are in this format.
`{"author":"chaten","type":"message","message":"hi"}`

## Status

#### If a user joins, you will receive a message like this
`{"type":"join","message":"username"}`

#### If a user quits, you will receive a message like this
`{"type":"quit","message":"username"}`
