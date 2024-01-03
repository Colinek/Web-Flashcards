# Web based Flashcards
## Using Google Sheets as a database

I created this Flashcard app which utilises my Google Sheets spreadsheet 
(Column A contains the word | Column B contains the definition) 

| word1 | definition1 |
|-------|-------------|
| word2 | definition2 |
| word3 | definition3 |
| ...   |             |

*There are no column titles in the sheets*

You can create new tabs in the spreadsheet (for different topics) - the app will pick up on these and popuplate the drop-down menu accordingly.

### Changes you need to make

You need to add your own Google Sheets info to the code:

In File menu: Share -> __Publish to Web__
Link: 
Entire Document | Web page

Paste the result into Line 169:
const sheetUrl = *https ://docs.google.com ... * from


Line 176:

Line 199:
