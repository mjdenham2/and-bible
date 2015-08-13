# Recent Changes #

## Technical Changes ##
Refactor the XML->HTML conversion code and add specific unit tests.
Integrate EventBus to simplify component interactions.
Build with Gradle.  This is Google's future planned build mechanism.

## Fix Daily Readings ##
Convert to uses of OSIS references and SimpleOSISParser which will avoid problems with simple books and book name translations.

## Abbreviate Book Names ##
Eg StrongsRealGreek -> 'StReG' instead of 'Stron' which could match several books.