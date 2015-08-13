# Update #

To avoid problems with incorrect readings for non-English readers and difficulty specifying single chapter books Reading Plans are being changed to use OSIS ids instead of the current free format passage references.

Non-OSIS references will be deprecated.  I have made some attempt to ensure old free-format references will continue to work but this is not guaranteed.

Passage references must be changed from the following style: "Gen 1, Matt 1-2, Psalm 119:1-10"
To: "Gen.1,Matt.1-Matt.2,Ps.119.1-Ps.119.10"

Example reading plans can be found [here](https://github.com/mjdenham/and-bible/tree/master/AndBible/assets/readingplan).

A full list of OSIS book names can be found [here](http://www.crosswire.org/wiki/OSIS_Book_Abbreviations)


# Reading Plan #

Reading plans are accessible via Menu/More/Reading Plan.

On first access you select a plan and are taken to the Daily Reading screen for the first day.

The Done button will be enabled after pressing Speak or Passage for each passage.  Done causes the Daily Reading to move to the next day and if you are behind will take you to the next day's readings.

## Custom Reading Plans ##
It is possible to create a custom reading plan for use with And Bible.

You will need to create a file similar to the examples [here](https://github.com/mjdenham/and-bible/tree/master/AndBible/assets/readingplan) which are the reading plans distributed with And Bible.  The name of the file will be the name of the plan.  The file extension must be .properties and you must place it on your mobile's sdcard in a folder named jsword/readingplan.  Use a simple text editor to create the file e.g. Notepad++ and do not use something like Word.  The file must contain a series of rows in the format day=reading1,reading2 E.g.
```
1=Gen.1, Matt.1
2=Gen.2, Matt.2
3=Gen.3, Matt.3
4=Ps.119
5=1Cor.1, Jude
```

It is possible to skip days e.g. if you do not wish to a reading at the weekend. E.g.
```
1=Gen.1, Matt.1
3=Gen.2, Matt.2
```

OSIS format references must be used and OSIS Bible book names must be used.  These will be translated to the current language when displayed in And Bible.

##### Deuterocanonical Books #####
The default versification for reading plans is KJV.  If you wish to include deuterocanonical books  in your plan you must specify the versification in the properties file.  E.g.:
```
Versification=Vulg
1=Sir.1-Sir.2
2=1Macc.1-1Macc.2
3=Bar.1-Bar.2
```

## Set Start to Jan 1st ##
If you started the readings on 1st Jan and have just switched to And Bible then select Menu form the Daily Reading screen and then select 'Start Jan 1'.  You may then jump to 'Move the current day to a specific day' below to skip over readings you have already done.

## Abandon Reading Plan ##
Press Menu/Reset from the Daily Reading screen.

## Switch between Reading Plans ##
Select the first button in the toolbar when in the Daily Reading screen.  By this means it is possible to use several plans simultaneously.

## Preview a plans readings ##
When in the Daily Reading screen select the second button in the toolbar.

## Go to a specific day ##
When in the Daily Reading screen select the second button in the toolbar.  Then select the required day from the list.

## Move the current day to a specific day ##
This is useful if you have been using a reading plan externally from And Bible.  A sequence of actions might be i) select plan ii) Set start date to Jan 1st (as above) iii) Move the current day to a specific day (as below)
Go to the day prior to the desired day as described in the above paragraph.  Select Menu/Done (not the normal Done button at the bottom) this bypasses checks and marks the current day as Done and the next day will become the current day.