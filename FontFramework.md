# Font Framework #

Fonts can be overridden by module or language either manually by each user or centrally for all users.

## Reason for Font Framework ##
There have been lots of e-mails regarding font problems during the past year and I have made a start with an attempt to address some of those problems.

The main issues that have been raised are:
  1. Greek breathing marks are not displayed.
  1. Hebrew vowels not displayed because they prevent correct rtl display.
  1. Certain language fonts are not available on Android
  1. Certain language character shaping and rtl are not correct - related to 2.

## Manual Override ##

Experienced Sword users can associate a font with a module or language using sdcard/jsword/fonts folder.

  1. Create this folder on your Android mobile:  mnt/sdcard/jsword/fonts
  1. Create fonts.properties containing mappings like 'SBLGNT=GalSILR.ttf' or 'fr=myFrenchFont.ttf' and copy the file to the above folder
  1. Copy any referenced font (ttf) files to the same folder
  1. Restart And Bible and test the font
  1. To adjust the font size you may also add settings like 'myFrenchFont.ttf=2' to increase the font size by 2.

## Central Font Override ##

This will hopefully address 1 and begin to address 3 for non complex languages.

  1. Store fonts on a server.
  1. Associate fonts with a module or language.
  1. When a module is downloaded check the font association list and download a font if required.
  1. When displaying a page add the css to the header to load any required font

The above will hopefully provide the correct display of modules with no user intervention.  Experienced users will be able to change font using the jsword/fonts folder.

Currently only the SBLGNT font is overridden.

## Shaping ##
It has been suggested that And Bible includes Graphite integration to display rtl and complex languages and I hope to look into this and try it out.  Any comments from current users would be appreciated.

Graphite still requires fonts to be distributed so this would build on the initial font distribution framework.

The Android integration of Graphite seems to be being refined.

## Current Status ##
I have been testing various Greek fonts with the SBLGNT module.
| GentiumPlus-R.ttf | squares due to missing chars in SBLGNT |
|:------------------|:---------------------------------------|
| SBL\_grk.ttf      | looks perfect to me                    |
| LinLibertine\_R.otf | squares due to missing chars in SBLGNT |
| LinBiolinum\_R.otf | squares due to missing chars in SBLGNT |
| GalSILR.ttf       | looks good, possible missing char in Matt 1:6, etc |
| GalSILR-webfont.woff | woff doesn't seem to work - I think it is just Android 3.0+ but see http://stackoverflow.com/questions/3200069/css-fonts-on-android for fall back technique |