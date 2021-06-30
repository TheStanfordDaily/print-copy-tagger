# Copy tagging script tagger.py
This is the script we use on the copy computer for tagging content during print production.
See [the copy guide](https://docs.google.com/document/d/1nQ9UY9MAlwgNVPVuiWBONdZQeZme0aic2AXMitfk_qo/edit?usp=sharing) for instructions on how to use.

This program will convert a directory of .rtf files into tagged and formatted
.txt files.

(1)   Create a new folder somewhere.
(2)   For each article to be tagged, find the Wordpress post (though the admin
      page, not online). Select the "Text" tab on the top right of the post 
      content frame. This will display a stripped-down version of the text and
      may contain HTML tags. Select all the text and copy/paste it into a new
      TextEdit document. 
(3)   Save the document:
      - the file format should be "Rich Text Document"
      - name the file using the usual convension but add a space followed by
        the author's name at the end, e.g. "NEWassu26 Catherine Dong"
      - save in the folder you created in step (1)
(4)   

USAGE:    python tagger.py [dirpath]
e.g.:     python tagger.py /Users/Catherine/Documents/Daily/tagging

# NOTES: 
- Must fill in @NewsHeader (NEWS) and Series Title (OPS) tags
- Must replace FIRST LETTER in dropcaps (OPS and A&L)
- Does not handle underlined text

## ISSUES:
- blockquotes don't get deleted
- identifies last paragraph as @@line if there is a tag with a @
- class years followed by punctuation (Catherine '16, blablaba)

# CHANGELOG:

### Author: Catherine Dong
9/30/14
------------------------------------------------------------------------------
### Updated: Do-Hyoung Park
1/30/15
Added more staff writers/editors, added sports column header
------------------------------------------------------------------------------
### Updated: Stephanie Chen
2/16/16
- updated directory, added new weekender italic tags
- removes extra whitespace (doublespacing after periods, ends of paragraphs)
- adds <*d(0)> on dropcaps articles
- fixed arts (non weekender) header
- added @ATTRIB for briefs
- first letter should be handled (????)

### 10/2/16
- moved weekender script to usage: python tagger.py tagging weekender
-     note: but we don't use weekender anymore, yay
-     also note: weekender script is buggy re: tabbing on bold/italic headers, italics on contact lines 

### 10/12/16
- drop letter details on quotation marks + "I" sentences
------------------------------------------------------------------------------

### STAFF LIST UPDATED: 9/21/16
