# Web based Flashcards
### Using Google Sheets as a database

I created this Flashcard app which utilises my Google Sheets spreadsheet 
(Column A contains the word | Column B contains the definition) 

| word1 | definition1 |
|-------|-------------|
| word2 | definition2 |
| word3 | definition3 |
| ...   |             |

*There are no column titles in the sheets*

You can create new tabs in the spreadsheet (for different topics) - the app will pick up on these and popuplate the drop-down menu accordingly.

Once you have your Spreadsheet created, you need to Publish it to the Web

You need to add your own Google Sheets info to the code:

In File menu: Share -> __Publish to Web__

Link  
Entire Document | Web page  
**[Publish]**
___
## Changes you need to make

You need to add your own Google Sheets info to the code:

In File menu: Share -> __Publish to Web__
Link   
Entire Document | Web page 

Paste the result into Line 169:
`const sheetUrl = "https ://docs.google.com ... /pubhtml";`


Then, still in the Publish to the Web window:  
1st_Tab_in_Spreadsheet | Comma-separated values (.csv)
**[Publish]**

Copy the link that appears. Trim the beginning (up to 2PACX), the end (after/pub?gid=) and paste it into Line 176:
`const baseUrl = "2PACX-1xx2qq ... /pub?gid=";`


Using the same csv Link, paste the code into Line 199
Remove the number (first TAB on Spreadsheet is '0'; second TAB is about 10 digits long) between pub?gid=   and  &single=true&output=csv

Line 199:
``let tabUrl = `https ://docs.google.com/spreadsheets/d/e/2PACX-1xx2qq ... /pub?gid=${tabId}&single=true&output=csv`;``


