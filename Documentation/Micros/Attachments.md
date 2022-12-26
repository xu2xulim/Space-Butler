# Introduction

- The base url is url specific to your instance of Space Bulter + `/attachments` (path for the micro)

# Description

The following services are available :

## /get_attachment

- get the content of an attachment using the attachment id. Current image, pdf and text files are supported


### Trello Automation Use Cases

- returns the content of an attachment

### Method
- GET

### Query Parameters

`?card_id={triggercardidlong}&attach_id=<attachment ID in first 24 chars of string>`

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

### Other Notes
- This collection of endpoints involves downloading and creating attachments. It should be noted that here is a 10s timeout for each trigger.


## /list_attachments

- The endpoint to create a checklist "Attachments - <option>" containing the `<attachment id> || <attachment name>`

### Trello Automation Use Cases

- Use together with "for each item" and the service "/get_attachment" you will be able to use it with other api that requires a copy of the attachment eg to send attachment via email or send it to a White Hole using the Deta Space App "Black Hole" to share your Trello content for images

### Payload
`{ "card_id": "{cardidlong}" , "option": "pdf" }`

the support values for option are : `all, pdf, images`
