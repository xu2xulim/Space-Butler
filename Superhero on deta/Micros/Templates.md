# Introduction

- The base url is `https://lwdb8h.deta.dev`
- Redoc : https://lwdb8h.deta.dev/redoc
- OpenAPI : https://lwdb8h.deta.dev/docs

# Endpoints

The following endpoints are available on this micro :

## /update_cardlinks

- Inspects newly created template board to look for cardlinks and update them to point to the cards on the new board.


### Trello Automation Use Cases

- New boards from a template boards contains links that are pointing to cards on the template board.

### Sample Payload

`{"board_id" : "{boardid}"}`
