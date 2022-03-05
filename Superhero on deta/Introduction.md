This folder contains a brief documentation of the endpoints in each **Deta Micro** including url to the OpenAPI and redoc documentation.

Trello Http Request will require the URL, request method and the Payload.

### URL Format

Here's an example of a URL for a http request :
`https://w55o8f.deta.dev/update_location?api_key=<API Key>&token=<token>`

where

- the Base URL is `https://w55o8f.deta.dev`
- path for the endpoint is `/update_location`
- your api key is `<API Key>`
- your token is `<token>`

### Request Method

In most cases, the request will be a **POST** http request.

### Payload

Here's an example of a Payload :

`{"card_id" : "{triggercardidlong}", "address" : "60 Lincoln Center Plaza, New York, NY 10023, United States", "locationName" : "The Juilliard School"}`

In the above case, the {triggercardidlong} is a Trello variable and when the request is called, Trello automation will insert the value of the card id. For more information on Trello variables, visit this [help page](https://help.trello.com/article/1157-variables).
