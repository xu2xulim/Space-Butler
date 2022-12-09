# Introduction

- The base url is url specific to your instance of Space Bulter

# Description

The following services are available :

## /get_customfields

- Returns the custom field values for the card

### Trello Automation Use Cases

- Use {foundcardidlong} following a lookup or find.
- Or Use {triggercardidlong} when trying to replicate custom fields to a new card.

### Trello Automation Use Cases

- Below is an example of a card button automation to update the price on a card based on the price type (a custom field PTYPE) using the price on another card from the "Lookup" list. The endpoint returns the {httpresponse} containing all the custom fields on the lookup card and the price is available as {httpresponse.Price}.

`lookup a card titled "{{%PTYPE}}" in list "Lookup", post to url "https://<your Space Butler endpoint>" with payload "{"card_id" : "{foundcardidlong}"}", and set custom field "Price" to "{httpresponse.Price}`

### Payload

`{"card_id" : "{foundcardidlong}"}`

## /update_checkbox

- Updates the checkbox custom field based on the checked status on another card.

### Trello Automation Use Cases

- Can be applied in various scenarios as long as you have the {cardidlong} of both the trigger card and the target card like the {foundcardidlong} or the {newcardidlong}

### Payload

`{"card_id" : "{triggercardidlong}", "alt_card_id" : "{foundcardidlong}", "cf_name" : "CF_Checkbox", "alt_cf_name" : "Another_Checkbox"}`
