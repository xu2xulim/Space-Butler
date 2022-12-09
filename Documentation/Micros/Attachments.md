# Introduction

- The base url is url specific to your instance of Space Bulter

# Description

The following services are available :

## /copy_attachments

- Copy attachments from a card to another. This will ignore all card and board links.


### Trello Automation Use Cases

- copy the attachments from the source card to a new new card.

### Payload

`{"card_id" : "{triggercardidlong}", "alt_card_id" : "{newcardidlong}", "option" : ""}`

where option can be

`"" for all attachments,
"first" - the first attachment added on the source/trigger card or
"last" - the last attachment added on the source/trigger card`


## /setcover

- Set the first or last attachment as the cover.

### Trello Automation Use Cases

- Trello defaults to the first attachment uploaded to the card. Use this endpoint to change it to the last upload automatically.

### Payload

`{"card_id" : "{triggercardidlong}", "option" : ""}`

where option can be

`
"first" - the first attachment added on the source/trigger card or
"last" - the last attachment added on the source/trigger card
`

## /usecover

- The endpoint will get the cover from one card and set it as the cover on a second card.

### Trello Automation Use Cases

- /setcover alls you change cover to use the last/first upload file. You can use this endpoint to set a cover for a new card from either a lookup or the source card.

- this endpoint will not work with covers that are created from Unsplash.

### Payload

`{"card_id" : "{triggercardidlong}", "alt_card_id" : "{newcardidlong}"}`


## /usesticker

- The endpoint will get the cover from one card and set it as the cover on a second card.

### Trello Automation Use Cases

- You can use this endpoint to set a sticker for a new card from either a lookup or the source card.
- When there is more than 1 sticker, the first on the list will be used.

### Payload

`{"card_id" : "{triggercardidlong}", "alt_card_id" : "{newcardidlong}"}`

## Other Notes
- This collection of endpoints involves downloading and creating attachments. It should be noted that here is a 10s timeout for each trigger.
