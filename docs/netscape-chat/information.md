# Netscape Chat Communication Information

## Send this message when first opening the server connection to authenticate with the server
{"password":"your password","author":"your username"}

## Once authenticated, you will get this response from the server:
{"type":"broadcast","message":"You have successfully authenticated"}

## You will probably see this as well. This is the format for _all_ join messages, including yours.
{"type":"broadcast","message":"User has joined"}

## Messages to _and_ from the server are in this format.
{"author":"chaten","type":"message","message":"hi"}
