# Introduction

- The base url is `https://w55o8f.deta.dev`
- Redoc : https://w55o8f.deta.dev/redoc
- OpenAPI : https://w55o8f.deta.dev/docs

# Endpoints

The following endpoints are available on this micro :

## /update_location

Geocode an address and update a card location attributes

### Trello Automation Use Cases

- Parse form input to set the location attributes on the card
- When addr_custom_field and location_name_custom_fields are completed

### Sample Payload

`{"card_id" : "{newcardidlong}", "address" : "60 Lincoln Center Plaza, New York, NY 10023, United States", "locationName" : "The Juilliard School" }`

## /copy_location

Copy the location attributes from one card to another.

### Trello Automation Use Cases

- Create a new card and copy the location attributes from the trigger card to the new card
- Find a job card and copy the details from the customer card to the job card.

### Sample Payload

`{"card_id" : "{triggercardidlong}", "alt_card_id" : "{foundcardidlong}"}`
