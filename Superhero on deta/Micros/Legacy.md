# PENDING MIGRATION SPACE BUTLER

# Introduction

- The base url is url specific to your instance of Space Bulter

# Description

The following services are available :


- Creates a new card using the metadata extract from the URL. This was a legacy capability that is now replaced with a cardlink instead of a usable card for workflow.
- For example use `>>https://www.youtube.com/watch?v=bU001cy_PE8` when creating a card.

### Trello Automation

`when a card with a name starting with ">>http{*}" is added to the board, post to url "https://r1vaz7.deta.dev/endpoint?api_key=<API Key>&token=<token>" with payload "{"card_id" : "{triggercardidlong}"}"`
