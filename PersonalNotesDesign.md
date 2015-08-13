# New Design with Integrated Notes, Bookmarks, Highlights #

## Objective ##

The new design will require fewer menu items but be more consistent and comprehensive for both bookmark and note use. The flow will mean it is easier to add labels to new bookmarks immediately.  Eventually highlights will be added to the My Notes functionality.

## Overview ##
In Standard Menu there will be a single "My Notes" menu item instead of Bookmarks, and My Notes.  The context menu will have just Add/Edit My Note.

## Add/Edit My Note Screen ##
To the current My Note screen will be added checkboxes for Bookmark and Highlight, and a button providing access to Labels functionality.

Layout:
Bookmark   Highlight  Labels  < 2 check boxes and a button or test field
Large text field for note < the current note entry field

Menu will contain: My Notes (list)

## My Notes (list) ##
Similar to Bookmarks list showing either verse or note (if there is a note).  Can view just notes, bookmarks, or highlights.

Select: Notes, Bookmarks, Highlights, All  < top row will have 2 select boxes
Select: label1, label2,

Menu will contain: Sort by date



# Old Design of My Notes (to be deprecated) #

# Introduction #

Initially a simple implementation allowing notes for any bible verse to be saved in a database on the mobile phone and later viewed or edited via a Notes list.

There will be an 'Edit Note' screen to allow notes to be entered and viewed, and a 'Notes List' allowing selection of previous notes.

Two new menu items will be made available.  'Notes' will take you to the Notes list.  'Add/Edit Note will take you to the 'Edit Note' screen for the current verse.  Notes can only be entered for bible verses.

There will initially be no synchronization, export, or backup functions although these may be added in future releases.

# Details #

## Database ##
  * Key // OSIS ID of current verse
  * Timestamp // Date-time of creation
  * Note // User note - simple text at first

Do we want some sort of Label functionality similar to bookmark labels?  I think not because we don't have that in Commentaries.

## Navigation Integration ##
### Create a note ###
[Add|Edit] Note // from Verse menu

### Edit a note ###
[Add|Edit] Note // from Verse menu

### Delete a Note ###
Context menu on Notes list.
Delete button on Edit Note screen

### View Notes ###
Access Notes List from the 'Notes' menu item

## Interface ##
### Notes List ###
Notes menu item and Contents Menu item accessible from Edit Note screen  shows list of previous notes including verse, 1st line (and date if landscape)

### New/Edit Note ###
Current verse: read-only
Text Box: enter note here

## Points ##
### No Commentary Integration ###
Notes will not be integrated into the current Commentary screens because it is not anticipated there will be enough Notes created to make Commentary like navigation work.