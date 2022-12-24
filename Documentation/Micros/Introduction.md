# Status

The services documented herein and the services from following micros are available on the app :
- Custom Fields : path is /customfields
- Attachments : path is /attachments


# Introduction

- The base url is url specific to your instance of Space Bulter. *Note: * there is no path associated with the use to the services documented on this page.

# Description

The following services are available :

## /get_card

- Returns the card name

### Trello Automation Use Cases

- Use {cardidlong} inside the payload to test your setup

### Payload

`{"card_id" : "{cardidlong}"}`

## /delete_card

- Delete the card using its id.

### Trello Automation Use Cases

- From `for each card linked from a item in checklist <your checklistname>` in which case each item is the {cardidlong} . You can collect and build this checklist using the "collect card" actions to delete the cards you want.

### Payload

`{"card_id" : "{checklistitemname}"}` following the example in use case where item is the {cardidlong}


### WARNING
- The delete action **NOT REVERSIBLE**

## /set_reminder

- Set custom reminders for card due dates

### Trello Automation Use Cases

- To set custom reminders for a card due date based on the number of days or hours

### Query parameters

`?number=<int>&unit=<day/hour/minute>`

where
- number is an integer value which used to compute the number minutes to be used with the api
- unit can be any value : day, hour, minute

### Payload

`{"card_id" : "{cardidlong}"}`
