The following notes are a high level overview.  Please embellish and correct according to your experience.

When compiling you will notice warnings regarding anonymous inner classes.  These can be ignored and are due to libraries compiled with JDK 1.4.

# Eclipse #

Eclipse is the IDE used for development of And Bible.

  1. Download and install jdk 1.7.
  1. Install the [Android SDK](http://developer.android.com/sdk/index.html).
  1. Install [Eclipse](http://www.eclipse.org/downloads/) for Java EE developers or for Java Developers
  1. Select Java 7 as the installed jre and compliance level in Window/Preferences.
  1. Install the [Eclipse ADT plugin](http://developer.android.com/sdk/eclipse-adt.html).
  1. Ensure Eclipse has a Git plugin e.g. eGit or install Git for use from the command line (see below for more details).
  1. Clone the [And Bible source](https://github.com/mjdenham/and-bible)
  1. Install Gradle, Enide, and download required jars as described in Gradle below.
  1. Install Android Support v7 App Compat library as described below.
  1. In eclipse right-click the And Bible project and select Run As/Android Application

# Git #

You could take one of at least 2 approaches to get And Bible source code from Github - 1) use the EGit plugin for Eclipse 2) use pure git commands e.g 'git pull'

You will probably want to install egit anyway so if you do then you can follow the ['Starting from existing repositories'](http://wiki.eclipse.org/EGit/User_Guide#Starting_from_existing_Git_Repositories) instructions.

If you install basic command line [git](http://git-scm.com/) then you could do the following:
md andbible
cd andbible
git init
git pull git://github.com/mjdenham/and-bible.git

# Android Support Library App Bar Compat v7 (4.4.2 19) #
The App Bar Compat library is now required.  If using Eclipse this must be configured as a Library Project.

Follow [Adding libraries with resources](http://developer.android.com/tools/support-library/setup.html#libs-with-res) on the Android [Support Library](http://developer.android.com/tools/support-library) page.
Check appcompat-proj/project.properties to ensure the compat library sdk version is consistent with And Bible's and has been downloaded using the Android SDK.

After installation you should see a project named android-support-v7-appcompat in your eclipse IDE.

# Other IDEs #

Some IDEs like IDEA already have custom embedded Android Tools which can be used.  See this [Google Help Page](http://developer.android.com/guide/developing/other-ide.html) for more information.

# Gradle #
Building with gradle is supported but eclipse is my main development environment so integration with IDEA is up to the user.  Most libraries are no longer pre-installed in the libs folder but using gradle will automatically download and copy the required libraries to the libs folder for use in eclipse builds.  To force population of the libs folder run:
> gradle copyJarDependencies
from the AndBible folder.

Gradle 1.12 should be installed as described at:
http://www.gradle.org/installation

The Enide Gradle eclipse plugin can be downloaded from the Eclipse Marketplace.

Ensure ANDROID\_HOME environment variable is set correctly.  In Linux I found this needed to be in .profile (not .bashrc) and do a restart after setting it:
export ANDROID\_HOME=/opt/android-sdk-linux

## Running RobeElectric Tests in Eclipse ##
Roboelectric and junit tests can be found under AndBible/test.  These can be configured and run in Eclipse by following [Create a JAVA project for your tests](http://robolectric.org/eclipse-quick-start/).

## Initialisation ##
After first install you will need to force Gradle to download required jars and make them available to eclipse in the libs folder by:
  * right-click build.gradle in the And Bible project and select: Run As/Gradle build Gradle build
  * press F5 on the libs folder to refresh it


To build either:
  * right-click build.gradle in the And Bible project and select: Run As/Gradle installDebug Gradle Android start
Or
  * from the command prompt type: gradle appStart

# Problems #
## ActionBar cannot be resolved to a type ##
You need to install the App Bar Compat library as described in the links above.

## Android 5 SDK ##
The Android 5 SDK is not currently supported although if you are on this version you should be able to get And Bible working but the ActionBar will look a little different.

I did briefly upgrade to Android 5 but various things broke (I don't plan to look at the Android 5 SDK again for a while).  It was just before a minor release so I downgraded again, but the downgrade was not easy.  If you have installed the Android 5 SDK you should be able to get it working reasonably well but not perfectly.  If you need to downgrade from 5 to 4.4.2 I have pasted in some downgrade notes I made below.  The hardest thing was finding the older versions of the appcompat library

I don't recall if I really needed to downgrade the tools but if you need to you may follow these instructions:
http://stackoverflow.com/questions/9555337/how-to-downgrade-my-sdk-version
http://dl-ssl.google.com/android/repository/tools_r22-linux.zip
from July 2014

I definitely needed to downgrade the appcompat library.  On my pc it is in /opt/android-sdk-linux/extras/android/support.
Older versions of the appcompat library can be accessed as follows:
https://dl-ssl.google.com/android/repository/support_r19.zip
https://dl-ssl.google.com/android/repository/support_r19.1.zip