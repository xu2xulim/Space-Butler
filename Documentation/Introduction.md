This folder contains the documentation of the services available from Space Butler. There are logically group and each group is a Deta Micro using FastAPI to provide the api services therein.

Trello Http Request will require the your instance of Space Butler, the route, request method and the Payload.

### URL Format

Here's an example of a URL for a http request :
`https://husky-yqs8-space_butler.milynnus.deta.app/update_location`

where

- your Space Butler instance endpoint is `[https://w55o8f.deta.dev](https://husky-yqs8-space_butler.milynnus.deta.app/)`
- path for service is `/update_location`

### Request Method

In most cases, the request will be a **POST** http request. The option is provided from within Trello Automation > Content > Http Request
Unless otherwise specific, no headers are required. Your API Key and Token you provide will be store on your personal, private cloud in Deta Space.

### Payload

Here's an example of a Payload :

`{"card_id" : "{triggercardidlong}", "address" : "60 Lincoln Center Plaza, New York, NY 10023, United States", "locationName" : "The Juilliard School"}`

In the above case, the {triggercardidlong} is a Trello variable and when the request is called, Trello automation will insert the value of the card id.

In Trello, the following prefixes are commonly used :

- {trigger...}
- {copy...}
- {new...}
- {multiplier...}
- {previous...}
- etc

For more information on Trello variables, visit this [help page](https://help.trello.com/article/1157-variables).
