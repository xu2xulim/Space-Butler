This folder contains a brief documentation of the endpoints in each **Deta Micro** including url to the OpenAPI and redoc documentation.

### URL Format

Here's an example of a URL for a http request :
`https://r1vaz7.deta.dev/endpoint?api_key=<API Key>&token=<token>`

where

- the Base URL is `https://r1vaz7.deta.dev`
- path for the endpoint is `/endpoint`
- your api key is `<API Key>`
- your token is `<token>`

### Payload

Here's an example of a Payload :

`{"card_id" : "{triggercardidlong}", "address" : "60 Lincoln Center Plaza, New York, NY 10023, United States", "locationName" : "The Juilliard School"}`

In the above case, the card_id is a Trello variable and when the request is called, Trello automation will insert the value of the card id.
