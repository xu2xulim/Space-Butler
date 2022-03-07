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

`{"card_id" : "{triggercardidlong}", "alt_card_id" : {newcardidlong}}`
