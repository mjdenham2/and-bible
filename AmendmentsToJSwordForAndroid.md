# Introduction #

JSword provides a quality, robust, mature and proven Java library that delivers theological documents stored in a variety of readily available formats, but especially OSIS documents from the CrossWire site.

Android provides a Java environment and ui framework for mobile phones.

The combination of Android, JSword, and CrossWire OSIS documents provides a good foundation for the development of a tool to display scripture and theological works on a mobile platform.

This page summarises some of the challenges in adapting JSword to the mobile environment.

# Details #

I will be putting lots of (hopefully interesting) info here.

# Fetch and Display of Bible Text #
JSword fetches raw OSIS text from a file, converts the text into a DOM model using JDOM, requests a SAXEventProvider from JDOM which is normally passed through an XSLT processor to convert the OSIS to HTML format ready for display.

## Changes to Optimise Fetch and Display of Text ##
### Architectural Change to Stream Data from Backend to View ###
I have heard JDOM is slow and with Android running on low spec and low memory machines I decided to remove JDOM.  Also, when considering simple raw text to html translation I considered the intermediate DOM model created by JSword added a lot of processing overhead, some functionality that I did not intend to use some of which could be done in SAX with the html conversion, so I removed the intermediate DOM model.

The refined architecture was to contain one InputStream of data from raw OSIS text through to web browser.  Use of a stream would avoid instantiating the whole document in several states and therefore consume less memory and hopefully be a lot faster.

=== Minor Change To Zip
ZVerseBackend is the raw OSIS text provider for most documents and ZVerseBackend uses org.crosswire.common.compress.Zip.uncompress().

Initially I saw many OutOfMemory exceptions emanating from Zip.uncompress() until I removed the redundant Buffer and set the initial size of the ByteArrayOutputStream which was had been at it's default value.

## Changes to Optimise Performance ##

## Changes to Workaround Android Deficiencies ##
Classloader problems on older Android version meant much of the dynamic class loading in JSword had to be backed up with default hard-coded class instantiation.

Lack of any javax.xml.transform functionality to support xslt on Android pre2.2 meant I used SAX.  I find Java easier than xslt for many things but there would have been advantages in using the existing mature xslt.  It may be necessary to switch back to it later.