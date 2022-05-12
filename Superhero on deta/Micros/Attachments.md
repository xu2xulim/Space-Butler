# Introduction

- The base url is `https://moklxc.deta.dev`
- Redoc : https://moklxc.deta.dev/redoc
- OpenAPI : https://moklxc.deta.dev/docs

# Endpoints

The following endpoints are available on this micro :

## /copy_attachments

- Copy attachments from a card to another. This will ignore all card and board links.


### Trello Automation Use Cases

- copy the attachments from the source card to a new new card.

### Sample Payload

`{"card_id" : "{triggercardidlong}", "alt_card_id" : "{newcardidlong}", "option" : ""}`

where option can be

`"" for all attachments,
"first" - the first attachment added on the source/trigger card or
"last" - the last attachment added on the source/trigger card`

## /setcover

- Set the first or last attachment as the cover.


### Trello Automation Use Cases

- Trello defaults to the first attachment uploaded to the card. Use this endpoint to change it to the last upload automatically.

### Sample Payload

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

### Sample Payload

`{"card_id" : "{triggercardidlong}", "alt_card_id" : "{newcardidlong}"}`


## Other Notes

- This collection of endpoints involves downloading and creating attachments. It should be noted that here is a 10s timeout for each trigger.
