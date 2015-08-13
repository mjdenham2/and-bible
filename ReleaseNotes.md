# Release Notes #

## Release 2.2.2 (10 July 2015) ##
  * Fix unsynchronised window initialisation
  * New window is unsynchronised if unsynchronised window is active
  * Update Korean and Latvian localisations
  * Attempt to fix occasional 'The specified child already has a parent.' building windows
  * Try to avoid rare NPE in ControlFactory

## Release 2.2.1 (2 July 2015) ##
  * Prevent race condition when initialising windows
  * Fix logic error switching between My Note view and Bible view - caused window flashes following links
  * Consequent Android 2.3 issues affecting swipe, bookmarks, ...
## Release 2.2.0 (26 June 2015) ##
  * Windows replace split-screen (see Menu/Window or [see demo](http://tiny.cc/abdemo))
  * Links open in dedicated window.
  * Unlimited windows synchronized or independent
  * Row of minimised windows at bottom

## Release 2.1.11 (11 April 2015) ##
  * Custom css stylesheet support (see And Bible wiki for details)
  * Updated Dutch localisation
  * Updated JSword library with many fixes
  * Synodal Prot versification mapping
  * Map zoom control fix
  * Support new paragraph type
  * Fewer Xiphos repo checks

## Release 2.1.9 (10 Jan 2015) ##
Layout improvements and fixes
  * Refactored OSIS to html parser
  * More unit tests
  * Improved `<l>` handling especially for rusCars poetry
  * Add milestone quote handler e.g. ESV start of Jn 3:16 had a missing quote
  * Avoid extra redundant note in HunUj due to trailing space after references
  * Allow red letter in non-Bible modules
  * Correct name of hi super css class
  * Derive x-reference verse from osisRef not reference text because some modules like UZIBT do not have a valid text in x-references.
  * Add support for OSIS table, row, and cell
  * Add support for OSIS list and item
  * Display divine name in lower caps

## Release 2.1.8 (26 Dec 2014) ##
  * Fix prev/next chapter swipe on old devices
  * Updated cs, hu localisations

## Release 2.1.7 (20 Dec 2014) ##
  * New 2 year reading plan
  * Fix inadvertent scroll on double-tap(maximise)
  * Fix rare error going Back to book chapter when book has multiple sections.

## Release 2.1.6 (22 Nov 2014) ##
  * Fix SynodalProt versification error affecting mudules like Russian CARS
  * Work around for offline X repository
  * Some localisation updates
  * Brighter red letter in Night mode

## Release 2.1.5 (11 Oct 2014) ##
  * Fix minor JSword bug preventing index of Gill
  * Azerbaijani localisation
  * Reading plans now use OSIS references to fix single chapter book, and non-English reference problems.
  * Remember all Search settings when using Back/History to return to a previous Search screen
  * Can build using Gradle
  * Components kept in synch using EventBus rather than mediator and listeners
  * Fix missing-search-results problem

## Release 2.1.1 (31 May 2014) ##
  * Fix crash when adding MyNote for deuterocanonical verse
  * Allow deuterocanonical passages in personal reading plans
  * Fix occasional missing verse number in action bar
  * New Slovak localisation
  * Updated es, fr, hu, kk, ky localisations
  * Improve abbreviated document names in Action bar buttons
  * Fix: Book sort order by initials in Action bar quick buttons
  * Fix: Bookmarks and selected label added to History list allowing Back to previous bookmark selection

## Release 2.1.0 (17 May 2014) ##
Improve Bible book selector:
  * List by column in Portrait to show longer lists i.e. 6x11 instead of 11x6.
  * Enable sort alphabetically (for novices) or Biblical order
  * Page for deuterocanonical books.
  * Only display books available in current document e.g. NT only
Other changes:
  * Pause Speak when a phone call occurs, not when app moves to background.
  * Include modules from Wycliffe repository
  * Updated JSword library
  * Bug fixes

## Release 2.0.1 (8 March 2014) ##
  * Updated Chinese and Hebrew localisations
  * Fix some exceptions
  * Workaround to avoid error when updating to a newer Document

## Release 2.0.0 (15 February 2014) ##
  * New Ichthys launcher icon which is safer for persecuted users
  * More standard ActionBar replaces toolbar
  * Possible to increase text size more for the poor sighted
  * JSword Updates and optimizations in JSword library
  * Lights out mode when maximized
  * Bug fixes
## Release 1.9.3 (1st January 2014) ##
  * Allow selection of Bookmark sort order - date or Biblical.
  * Allow selection of My Note sort order - date or Biblical.
  * Allow edit/rename of bookmark labels via label context menu.
  * Fix multiple Bookmark lists in History after Label view
  * Cope with missing repositories in Download Documents
## Release 1.9.2 (30th November 2013) ##
  * Change Speak Smiley to Speaker icon
  * Fix for squashed verse button on small screens if Strongs available
  * Fix to show verse button in My Note
  * Fix auto-scroll after return from My Note
## Release 1.9.1 (23rd November 2013) ##
  * Kazakh, Kirgyz, Slovenian, and Telugu interface translations
  * Bug fixes
## Release 1.9.0 (13th June 2013) ##
  * Alternate versifications
  * Mapping between Synodal, German, Leningrad, Vulgate, KJV, and NRSV versifications
  * See versification demonstration video at http://youtu.be/dTSTW6s_qFU
  * Completed Spanish localisation (Laura)
  * Greek localisation (Wasilis)
  * Updated JSword library
  * Central Asian documents from IBT now available
  * Russian Synodal Bible now available
  * Bug fixes
## Release 1.8.0 (19th March 2013) ##
  * Split screen functionality - see [demonstration video](http://tinyurl.com/SplitDemo)
  * Support for Samsung multi-window
  * Ability to limit Search to current Bible book
  * Bug fixes
## Release 1.7.3 (9th January 2013) ##
  * Custom And Bible screen sleep timeout setting
  * Partial Spanish translation
  * Font framework fixes
## Release 1.7.0 (15th December 2012) ##
  * Speak controls (Pause/Rewind/Forward)
  * Hindi localisation (Sijo)
  * Improved Chinese localisation (Chislon)
  * Arabic localisation (Emad)
  * Malayalam localisation (Android 4.1+; Jeesmon)
  * Improved Latvian localisation (Martins)
  * Partial Japanese localisation (Kyongun/Chislon)
  * Auto-scroll optimised and acceleration adjusted
  * Bookmarks page now included in History
  * Various bug fixes

## Release 1.6.0 (12th August 2012) ##
  * Italian localisation (Orall & Carla)
  * Estonian localisation (Rivo)
  * Partial Arabic localisation (Emad)
  * Add Quick Speak button to toolbar and remove maps and books buttons
  * Fix repeated merged verses e.g. TurNTB Eph 2:4-5
  * Fix incorrect spacing at bottom of page
  * Fix all black or white screen when using auto night mode
  * Various fixes and changes including ICS issues

## Release 1.5.5 (6th June 2012) ##
  * New Vietnamese localisation (Hiệp)
  * Fixes including ICS speak fix
  * Add 'Unlabelled' bookmark label
  * Minor dictionary improvements
  * Partial TEI support in dictionaries
  * Support custom Reading Plans (see [wiki entry](http://code.google.com/p/and-bible/wiki/ReadingPlan))

## Release 1.5.0 (28th April 2012) ##
  * Indonesian user interface
  * Backup and restore My Notes and Bookmarks to SD card
  * Tweak toolbar and button size
  * Bug fixes

## Release 1.4.1 (3rd April 2012) ##
Not released via App Market
  * New launcher icon

## Release 1.4.0 (31st March 2012) ##
  * Geographical maps e.g. Palestine in the time of Christ, Canaan after the conquest
  * Improved document download screen includes upgraded module notification
  * Hebrew vowels displayed for recent CyanogenMod and Android 4.0.3+
  * Alternative Strongs dictionaries added - StrongsRealGreek, StrongsRealHebrew (Greek & Hebrew font issues in Android 2.1)

## Release 1.3.0 (25th February 2012) ##
  * Compare translations
  * Improved bible formatting
  * Bug fixes

## Release 1.2.0 (13th February 2012) ##
  * Reading plans (Menu/More/Reading Plan)
  * Tilt to scroll (Settings/Tilt to scroll; Android 2.2+ only)
  * Automatic night/day mode (Settings/Night mode/Automatic)
  * Night mode extended to all pages
  * Formatting improvements to titles and paragraphs
  * Bug fixes

## Release 1.1.1 (22nd December 2011) ##
  * Improved error recovery for unusually formatted documents
  * Turkish bible and interface localisation
  * Norwegian interface localisation

## Release 1.0.2 (5/11/2011) ##
  * Android 4.0 compatibility fixed
  * French translation updated
  * UKJV fixes

## Release 1.0.1 (29/10/2011) ##
Fixes context menu operation in Android 2.1

## Release 1.0.0 (29/10/2011) ##
  * Enter and edit My Notes
    * Add/edit/view MyNote via verse context menu
    * List MyNotes to view or delete notes via Main menu
  * Afrikaans user interface translation
  * Flexible text selection for copy to clipboard
  * Touch bottom of screen to page down
  * Improved formatting
  * Jonathan Edwards' Sermons book

## Release 0.7.2 (23/9/2011) ##
  * Fix various localised interface issues

## Release 0.7.1 (16/9/2011) ##
  * Fix error in Dutch localisation causing crash

## Release 0.7.0 (16/9/2011) ##
  * Font improvements - SBLGNT
  * References within Strong's are now links
  * New button to toggle Strong's numbers on/off
  * Toggle fullscreen on/off by double-tapping the screen
  * Japanese & Pinyin bibles added
  * Calvin's commentaries added
  * Bug: add languages missing from language list in Settings: Croatian, Korean, Latvian, Dutch, Ukrainian

## Version 0.5.07 (15/7/2011) ##
  * Remember line number when switching between commentary, book, or dictionary
  * Turn off Speech on phone call or whenever application moves to background
  * Option to show words of Christ in red
  * Option to turn off section headings
  * Italicize translator's additions in KJV
  * Bug fixes
  * Refactor html generation and JSword interface

## Version 0.5.0 (25/6/2011) ##
Fixes:
  * Chinese bible names blank outside of China
  * Swipe sometimes moves forward several pages
  * FarsiOPV Bible would not display
Enhancements:
  * Cross-reference links e.g. in TSK

## Version 0.4.0 (17/6/2011) ##
  * Improved user interface localisations
  * List of occurrences of a Strongs number
  * Integrate search results into history
  * Dictionary and Book shortcut keys
  * Navigate to verse
  * Robinson's Greek morphological codes displayed
  * Long press back button to show History list
  * Bug fixes

## Version 0.3.1 (4/4/2011) ##
  * Bug fixes
  * Added Polish Biblia Tysiaclecia

## Version 0.3.0 (26/3/2011) ##
  * Ability to search in Chinese bibles (contributed by Guan)
  * Ability to share a verse via Twitter and Facebook (contributed by Filipe)
  * Ability to display one verse per line (contributed by Stephen)
  * More powerful speech control
    * speak multiple chapters
    * use local pronunciation
    * repeat speech
    * speaks bibles, commentaries, dictionaries and books
  * Christian books e.g. Calvin's Institutes, Hodge's Systematic Theology, Pilgrim's Progress
  * Gill's Commentary now available
  * Quick links to module list and navigation in header
  * Change user interface language
  * Structured document selector
  * Fix Strong's links in Russian bibles
  * Several bug fixes

## Version 0.2.01 (2/2/2011) ##
  * Fix bug affecting Russian mobile phones

## Version 0.2.00 (28/1/2011) ##
  * Navigation using grid slide and go
    * slide to the required book/chapter and lift to go
  * Better Hebrew bible support
    1. right-to-left display
    1. Vowel points and cantillations removed pending Android fixes to allow rtl display
  * Use short bible book names in the header when in portrait mode so they always fit
  * New Lithuanian, Finnish, Hebrew (known issues), Portuguese and Faroese user interface translations (thanks Linas, Jori, Michael, Filipe and Sigurð)
  * Update to latest JSword including full Java 5 code

## Version 0.0.17 (31/12/2010) ##
  * Build for App Market
  * New Polish UI translation and updated Hungarian and Russian UI translations
  * Minor fixes

## Version 0.0.16 (27/12/2010) ##
  * Bookmarks - Add a bookmark via the context menu when viewing a bible and edit or return to the bookmark using the Bookmarks manager accessible via the main menu.
  * Bookmark Labels - Bookmarks can be grouped together using labels.  Example labels might be  'Memory verses',  'Forgiveness', or 'Evangelism'.  The idea is taken from the way labels are used in gmail.  This is slightly different to the conventional bookmark categories because a bookmark can have several labels but could only be in one category.
  * New Czech ui translation
  * Updated French, and Norwegian interface translations
  * Many changes in JSword code related to upgrading libraries to JDK 1.5 versions
  * New jars for file download and search
  * Allow fine adjustment of text size
  * Retain current commentary selection in quick change button
  * Smaller apk
  * Faster downloads
  * 'Notes and refs' moved to context menu
  * Bug fixes

## Version 0.0.17 (31/12/2010) ##
  * Build for App Market
  * New Polish UI translation and updated Hungarian and Russian UI translations
  * Minor fixes

## Version 0.0.16 (27/12/2010) ##
  * Bookmarks - Add a bookmark via the context menu when viewing a bible and edit or return to the bookmark using the Bookmarks manager accessible via the main menu.
  * Bookmark Labels - Bookmarks can be grouped together using labels.  Example labels might be  'Memory verses',  'Forgiveness', or 'Evangelism'.  The idea is taken from the way labels are used in gmail.  This is slightly different to the conventional bookmark categories because a bookmark can have several labels but could only be in one category.
  * New Czech ui translation
  * Updated French, and Norwegian interface translations
  * Many changes in JSword code related to upgrading libraries to JDK 1.5 versions
  * New jars for file download and search
  * Allow fine adjustment of text size
  * Retain current commentary selection in quick change button
  * Smaller apk
  * Faster downloads
  * 'Notes and refs' moved to context menu
  * Bug fixes

## Release 0.0.15 (22/11/2010) ##
  * Build for App Market
  * Send current verse via SMS

## Release 0.0.14 (19/11/2010) ##
  * Strongs Numbers display and link to Strong's Dictionary
  * Adjustable text size
  * Bug fixes - App switching, dictionary
  * Index download
  * Percentage complete in download progress bar now reflects actual file size
  * Delete document, About document accessible via context menu
  * Quick switch to another bible/commentary via title bar buttons
  * Copy current verse to Clipboard
  * Smaller apk (reduced from 5 Mb to 1.5 Mb)
  * D-Pad support for chapter changes

## Release 0.0.13 (23/10/2010) ##
  * Fix a memory leak
  * Improve display of any error messages from JSword
  * Add Help page
  * update App Market

## Release 0.0.12 (20/10/2010) ##
  * Simple dictionary prototype (no Strongs integration yet)
  * New and tidier look
  * Bug fixes

## Release 0.0.11 (8/10/2010) ##
This build contains a minor bug fix.  Errors occurring were not being displayed in the ui thread causing a secondary uncaught error.

## Release 0.0.10 was skipped ##

## Release 0.0.9 (6/10/2010) ##
This build contains bug fixes for issues discovered in build 0.0.8
  * fix for notifications that cannot be cleared if indexing or downloading fail
  * incorrect version number in translated uis
  * a few other subtle improvements in background task monitoring and thread creation

## Release 0.0.8 (4/10/2010) ##
If you have used a previous version of and-bible you will need to uninstall the old version before installing version 0.0.8 because a new encryption key is being used.

  * Faster navigation using grouped books and chapters
  * Improve synchronization of page change, hourglass, and verse update
  * Text to speech - listen to the bible read to you
  * Make swipe more sensitive
  * Download to dir deleted on app uninstall (Android 2.2) but still allow use of sdcard/jsword for manual installs
  * New icon (thanks John)
  * French localisation (thanks Dominique)
  * Improved initial install and download flow
  * Android Notification bar integration for download and index
  * Machine automated translations of the ui for Chinese, Korean, and German users (thanks Thomas)

## Release 0.0.7 (18/09/2010) ##
  * Exact verse calculation
  * Splash screen
  * History
  * Add Norwegian ui text (thanks Lars)
Fixes
  * Fix increasing number of duplicate page loads resulting in gradual slow down of bible
  * Fix duplicate calls to display commentary pages
  * Darker night mode & larger font
  * Avoid double quotes before Jesus Christ's words in esv

## Release 0.0.6 (20/08/2010) ##
  * Experimenting with a new name 'and God said'
  * Module download from CrossWire site
  * Jump to verse
  * Hungarian ui translation started (thanks Gabor)
  * Download documents displayed on first run so SdcardBibles.zip should no longer be required.
  * Night mode option (white text on black background)
  * index creation works but is very slow

## Release 0.0.5 (3/8/2010) ##
  * Fixed and enhanced search functionality - you need to get the new indexes from SdcardBibles2.zip too
  * Swedish user interface translation started (thanks Thomas)

## Release 0.0.4 (23/7/2010) ##
  * better visual pages
    * using WebView instead of TextView
    * noticeably faster due to use of WebView
    * tweak default font and spacing
    * pop-up footnotes & cross-references and allow navigation direct to cross-references (works well in ESV)
  * options page for display options e.g. turn off verse numbers, notes, ...
  * fix - page forward/back in a commentary sometimes causes a blank screen
  * fix swipe sensitivity problem affecting Droid

## Release 0.0.3 14/7/10 ##
  * fix to allow use of non OSIS ztext modules

## Release 0.0.2 14/7/10 ##
  * Use standard menu instead of toolbar
  * Optimised page loading
  * Slightly improved book/chapter selection
  * Current verse estimation and improved bible-commentary synch
  * fix back-a-page swipe
  * trackball support for next/prev page
  * application icon
  * tidy search results
  * save & restore state