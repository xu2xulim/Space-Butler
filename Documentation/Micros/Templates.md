# PENDING MIGRATION SPACE BUTLER

# Introduction

- The base url is url specific to your instance of Space Bulter

# Description

The following services are available :

## /update_cardlinks

- Inspects newly created board to look for cardlinks and update them to point to the cards on the new board. The lookup will be based on card name.


### Trello Automation Use Cases

- New boards from a template boards contains links that are pointing to cards on the template board.

### Sample Payload

`{"board_id" : "{boardid}"}`

### Limitations
- Too many cards and cardlinks due to possible timeout at the endpoint.
- Cards have the same name on the board.
