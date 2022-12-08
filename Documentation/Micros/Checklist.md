# PENDING MIGRATION SPACE BUTLER

# Introduction

- The base url is url specific to your instance of Space Bulter

# Description

The following services are available :

## /item_assign_due

- Creates an new card if not found on first list of a board and then create an advanced checklist with option to assign a member and or a due date.


### Trello Automation Use Cases

- While add a checklist, assign a member and assign a due date is available on Trello Automation, using them in conjunction with an data source such as spreadsheet, csv, todo list proofs to be more challenging. By providing this endpoint, you would be able to use e.g. Zapier transfer to create an advanced checklist on a board.

### Sample Payload

`{
    "item_name": "An Item on Advanced Checklist",
    "username": "@any_username",
    "due": "2022-05-16",
    "checklist_name": "Advanced Checklist from Zapier",
    "cardname": "Advanced Checklist from Zapier",
    "board_id": "5fdd5.........792101e"
}`

### Notes
- Username will be checked against the board members before it is assigned to the item.
- While the date format showned in example is in YYYY-MM-DD, it can be any standard date format such as DD-MM-YYYY. Do test it using your test period.
- Board name can be found by appending **.json** to the board url e.g. `https://trello.com/b/CkgNRQgc/dojo-1.json` The resulting screen show the board json file and the board id is the first string e.g. `{"id":"5fdd53039a97d380e792101e","name":"Dojo

## /new_item_assign_due

- Automate the assignment and due date when an item is added to an advanced checklist using custom fields.


### Trello Automation Use Cases

- Here's an example :
`
when an item is added to checklist "{*}" in a card with custom fields "Name" and "Date (Text)" completed, post to url "https://hfetwp.deta.dev/new_item_assign_due?api_key=<your api key>&token=<your token>" with payload "{ "card_id": "{cardidlong}", "checklist_name": "{checklistname}", "item_name": "{checklistitemname}", "username": "{{%Name}}", "due": "{{%Date (Text)}}"}"
`
### Notes
- The username format is @any_username . It has to have the prefix @.
- Date format is recommended to be YYYY-MM-DD
