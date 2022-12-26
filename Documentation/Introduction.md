This folder contains the documentation of the services available from Space Butler. There are logically group and each group is a Deta Micro using FastAPI to provide the api services therein.

Trello Http Request will require the your instance of Space Butler, the route, request method and the Payload.

### URL Format

Here's an example of a URL for a http request :
`https://husky-yqs8-space_butler.milynnus.deta.app/location/update_location`

where

- your Space Butler instance endpoint is `https://husky-yqs8-space_butler.milynnus.deta.app`
- path for the micro is `/location` (this is how the services are logically implemented)
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

### Query Parameters

Where query parameters are used, it is appended to the url e.g `https://husky-yqs8-space_butler.milynnus.deta.app/location/update_location?country=usa&zip=10023` where the query paramters is appended aka `?country=usa&zip=10023`

You can use Trello variables e.g `?country={{%Country}}&zip={{%Zip}}` where you have the country and zip values on the card as Custom Fields.

### For Assistance

You can reach out to me on [my webportal](https://dojo.hipposites.com/milynnuscrm/home)
