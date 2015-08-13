# Introduction #

Experiences with Chromium

# Details #

[User](AB.md) used the directions from this lifehacker webpage to get things running, then used the And Bible download found in this document here.

The version they use is an older build, but it is the only one I've had success with downloading modules with. So, I downloaded the modules I want with that version, then I swapped the old .apk they have in there with your latest .apk from the google drive folder you provide. So I have all the modules I want already, running as a Chrome extension.
In the extensions page, you can click Details > Create Shortcuts in order to make a shortcut directly to And Bible.

When I was on Linux, I remember that package managers typically had Chromium in them, which was different from the Chrome package thats downloadable from Google.

# Logcat #
Open your debug APK in ARC Welder and run it
Open Chrome and type "chrome://inspect/#apps" in the address bar
Hopefully you see your App name listed, click the 'inspect' link for your app.
In the Javascript Console that appears type
plugin.shell('logcat');
Source: https://developer.chrome.com/apps/getstarted_arc#bestpractices

# Error #
https://code.google.com/p/chromium/issues/detail?id=384940

/AbstractSwordInstaller(  204): Failed to reload cached index file
E/AbstractSwordInstaller(  204): org.crosswire.jsword.book.install.InstallException: Unable to find: http://www.crosswire.org/ftpmirror/pub/sword/wyclifferaw/mods.d.tar.gz
E/AbstractSwordInstaller(  204): 	at org.crosswire.jsword.book.install.sword.HttpSwordInstaller.download(HttpSwordInstaller.java:87)
E/AbstractSwordInstaller(  204): 	at org.crosswire.jsword.book.install.sword.AbstractSwordInstaller.reloadBookList(AbstractSwordInstaller.java:283)
E/AbstractSwordInstaller(  204): 	at org.crosswire.jsword.book.install.sword.AbstractSwordInstaller.loadCachedIndex(AbstractSwordInstaller.java:324)
E/AbstractSwordInstaller(  204): 	at org.crosswire.jsword.book.install.sword.AbstractSwordInstaller.getBooks(AbstractSwordInstaller.java:141)
E/AbstractSwordInstaller(  204): 	at net.bible.service.download.DownloadManager.getDownloadableBooks(DownloadManager.java:79)
E/AbstractSwordInstaller(  204): 	at net.bible.service.download.RepoBase.getBookList(RepoBase.java:25)
E/AbstractSwordInstaller(  204): 	at net.bible.service.download.WycliffeRepo.getRepoBooks(WycliffeRepo.java:28)
E/AbstractSwordInstaller(  204): 	at net.bible.service.sword.SwordDocumentFacade.getDownloadableDocuments(SwordDocumentFacade.java:228)
E/AbstractSwordInstaller(  204): 	at net.bible.android.control.download.DownloadControl.getDownloadableDocuments(DownloadControl.java:67)
E/AbstractSwordInstaller(  204): 	at net.bible.android.view.activity.download.Download.getDocumentsFromSource(Download.java:112)
E/AbstractSwordInstaller(  204): 	at net.bible.android.view.activity.base.DocumentSelectionBase$3.doInBackground(DocumentSelectionBase.java:261)
E/AbstractSwordInstaller(  204): 	at net.bible.android.view.activity.base.DocumentSelectionBase$3.doInBackground(DocumentSelectionBase.java:1)
E/AbstractSwordInstaller(  204): 	at android.os.AsyncTask$4.call(AsyncTask.java:372)
E/AbstractSwordInstaller(  204): 	at java.util.concurrent.FutureTask.run(FutureTask.java:237)
E/AbstractSwordInstaller(  204): 	at android.os.AsyncTask$SerialExecutor$2.run(AsyncTask.java:280)
E/AbstractSwordInstaller(  204): 	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1112)
E/AbstractSwordInstaller(  204): 	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:587)
E/AbstractSwordInstaller(  204): 	at java.lang.Thread.run(Thread.java:841)
E/AbstractSwordInstaller(  204): Caused by: org.crosswire.common.util.LucidException: Unable to find: http://www.crosswire.org/ftpmirror/pub/sword/wyclifferaw/mods.d.tar.gz
E/AbstractSwordInstaller(  204): 	at org.crosswire.common.util.WebResource.copy(WebResource.java:288)
E/AbstractSwordInstaller(  204): 	at org.crosswire.jsword.book.install.sword.HttpSwordInstaller.copy(HttpSwordInstaller.java:104)
E/AbstractSwordInstaller(  204): 	at org.crosswire.jsword.book.install.sword.HttpSwordInstaller.download(HttpSwordInstaller.java:84)
E/AbstractSwordInstaller(  204): 	... 17 more
E/AbstractSwordInstaller(  204): Caused by: java.net.SocketException: setsockopt failed: EINVAL (Invalid argument)
E/AbstractSwordInstaller(  204): 	at libcore.io.IoBridge.setSocketOption(IoBridge.java:306)
E/AbstractSwordInstaller(  204): 	at java.net.PlainSocketImpl.setOption(PlainSocketImpl.java:289)
E/AbstractSwordInstaller(  204): 	at java.net.Socket.setKeepAlive(Socket.java:453)
E/AbstractSwordInstaller(  204): 	at org.apache.http.impl.conn.HttpClientConnectionOperator.connect(HttpClientConnectionOperator.java:134)
E/AbstractSwordInstaller(  204): 	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.connect(PoolingHttpClientConnectionManager.java:314)
E/AbstractSwordInstaller(  204): 	at org.apache.http.impl.execchain.MainClientExec.establishRoute(MainClientExec.java:373)
E/AbstractSwordInstaller(  204): 	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:225)
E/AbstractSwordInstaller(  204): 	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:195)
E/AbstractSwordInstaller(  204): 	at org.apache.http
shell.js:141 .impl.execchain.RetryExec.execute(RetryExec.java:86)
E/AbstractSwordInstaller(  204): 	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:108)
E/AbstractSwordInstaller(  204): 	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:186)
E/AbstractSwordInstaller(  204): 	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
E/AbstractSwordInstaller(  204): 	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:106)
E/AbstractSwordInstaller(  204): 	at org.crosswire.common.util.WebResource.copy(WebResource.java:251)
E/AbstractSwordInstaller(  204): 	... 19 more
E/AbstractSwordInstaller(  204): Caused by: libcore.io.ErrnoException: setsockopt failed: EINVAL (Invalid argument)
E/AbstractSwordInstaller(  204): 	at libcore.io.Posix.setsockoptInt(Native Method)
E/AbstractSwordInstaller(  204): 	at libcore.io.ForwardingOs.setsockoptInt(ForwardingOs.java:122)
E/AbstractSwordInstaller(  204): 	at libcore.io.IoBridge.setSocketOptionErrno(IoBridge.java:338)
E/AbstractSwordInstaller(  204): 	at libcore.io.IoBridge.setSocketOption(IoBridge.java:304)
E/AbstractSwordInstaller(  204): 	... 32 more
W/net.bible.service.download.DownloadManager(  204): Reloading book list