# Introduction

- The base url is `https://jviwoq.deta.dev`
- Redoc : https://jviwoq.deta.dev/redoc
- OpenAPI : https://jviwoq.deta.dev/docs

# Endpoints

The following endpoints are available on this micro :

## /get_customfields

- Returns the custom field values for the card


### Trello Automation Use Cases

- Use {foundcardidlong} following a lookup or find.
- Or Use {triggercardidlong} when trying to replicate custom fields to a new card.

### Sample Payload

`{"card_id" : "{foundcardidlong}"}`

## /add_dropdown_option

- Adds the new dropdown list option if it is not on the list. It does not take into consideration the colour of the item to be added.

### Trello Automation Use Cases

- Add a new option to an existing dropdown custom field by name.

### Sample Payload

`{"card_id" : "{triggercardidlong}", "new_option" : "Add", "dropdown_name" : "Operation"}`

- **Note** the card_id can be any card on the board. It is used to search through the board's custom field definitions only.
