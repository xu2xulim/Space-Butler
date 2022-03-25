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

### Trello Automation Example

Below is an example of a card button automation to update the price on a card based on the price type (a custom field PTYPE) using the price on another card from the "Lookup" list. The endpoint returns the {httpresponse} containing all the custom fields on the lookup card and the price is available as {httpresponse.Price}.

`lookup a card titled "{{%PTYPE}}" in list "Lookup", post to url "https://jviwoq.deta.dev/get_customfields?api_key=14a...........21d7&token=be9f........6cb4" with payload "{"card_id" : "{foundcardidlong}"}", and set custom field "Price" to "{httpresponse.Price}`

### Sample Payload

`{"card_id" : "{foundcardidlong}"}`

## /update_checkbox

- Updates the checkbox custom field based on the checked status on another card.

### Trello Automation Use Cases

- Can be applied in various scenarios as long as you have the {cardidlong} of both the trigger card and the target card like the {foundcardidlong} or the {newcardidlong}

### Sample Payload

`{"card_id" : "{triggercardidlong}", "alt_card_id" : "{foundcardidlong}", "cf_name" : "CF_Checkbox"}`

**Notes** current version assumes that both cards are on the same board. If this has to work across boards, a second custom field name will be required since the change must be applied with the correct custom field definition id.
