# PENDING MIGRATION SPACE BUTLER

# Introduction

- The base url is url specific to your instance of Space Bulter

# Description

The following services are available :

## /items_due

- Looks at all open card. If the due date on item is a day away and its state is "incomplete", add a comment indicating the item is due. If a member is assigned on item item the @username will be used otherwise @card will be used instead.


### Trello Automation Use Cases

- Use the calendar command to call the endpoint to notify users ahead of time.

### Sample Payload

`{"board_id" : "{boardid}"}`

- **Note**
  - to get the board id, add .json at the end of the board url on your browser. The first id is the board_id.
  - A timeout may occur if you are trying to process too many open cards on the board.

## /time_on_list

- Computes the time on list in seconds / miunutes / hour / days. This includes time spent upon re-entry


### Trello Automation Use Cases

- Typically use to measure performance on a task as represented by the card.

### Sample Payload

`{"card_id" : "{cardidlong}", "listname" : "Doing"}`

- **Note**
 - future enhancement can include multiple list and a list that stops the time recording
