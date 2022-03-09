# Introduction

- The base url is `https://5v55yc.deta.dev`
- Redoc : https://5v55yc.deta.dev/redoc
- OpenAPI : https://5v55yc.deta.dev/docs

# Endpoints

The following endpoints are available on this micro :

## /items_due

- Looks at all open card. If the due date on item is a day away and its state is "incomplete", add a comment indicating the item is due. If a member is assigned on item item the @username will be used otherwise @card will be used instead.


### Trello Automation Use Cases

- Use the calendar command to call the endpoint to notify users ahead of time.

### Sample Payload

`{"board_id" : "{boardid}"}`

- **Note** to get the board id, add .json at the end of the board url on your browser. The first id is the board_id.
