Library of Javascript objects designed to retrieve data out of eID- and SIS cards using the applet from the eID Middleware SDK version 3.5.

The interface and implementation (identity data) of EIDCard and SISCard are designed to be eID Middleware independent.<br>
The interface and implementation of EIDCardBuilder35 and SISCardBuilder35 are designed for eID Middleware 3.5.<br>
The interface of CardReader is designed to be Middleware independent.<br>
The implementation of CardReader uses EIDCardBuilder35- and SISCardBuilder35 objects and so it is designed for eID Middleware 3.5.<br>

If a new EID Middleware is released, only new EIDCardBuilder- and SISCardBuilder objects should be created and <br>
only small changes will need to be applied to the implementation of the CardReader.<br>
<br>
The interface of CardReader, EIDCard and SISCard will not change.<br>
Therefore code that uses the CardReader-, EIDCard- and SISCard-objects will not have to be changed if a new eID Middleware is released.<br>

The library is supposed to work on Windows in Internet Explorer 5.5 and higher, in Mozilla Firefox 2 and higher, and in Opera 9 and higher.<br>
Other browsers and other platforms were not tested.<br>

SIS cards can only be read when using a SIS card plugin. A SIS card plugin for the ACS ACR38U reader is available in the eID Quick Install.<br>
More information about SIS card plugins in the eID V3 middleware can be found at:<br> <a href='http://eid.belgium.be/nl/binaries/eid3_siscardplugins_tcm147-22479.pdf'>http://eid.belgium.be/nl/binaries/eid3_siscardplugins_tcm147-22479.pdf</a><br>
<br>
@version 1.8 14/05/2011<br>
@author Johan De Schutter (eidjavascriptlib AT gmail DOT com), <a href='http://code.google.com/p/eid-javascript-lib/'>http://code.google.com/p/eid-javascript-lib/</a><br>
<br>

<br>
<br>
<B><br>
<br>
How to run the examples on your computer<br>
<br>
</B><br>
<br>
<br>
<br>
<ol><li>Download the archive eidjavascriptlib.zip from <a href='http://code.google.com/p/eid-javascript-lib/'>http://code.google.com/p/eid-javascript-lib/</a>
<ul><li>The archive contains the following subdirectories: examples, jsdoc and src.<br>
</li><li>Unzip the archive in a directory, for example c:\eid-javascript-lib<br><br>
</li></ul></li><li>Install eID software with the eID Quick install. Instructions can be found at<br>
<ul><li><a href='http://eid.belgium.be/nl/Hoe_installeer_je_de_eID/Quick_Install/'>http://eid.belgium.be/nl/Hoe_installeer_je_de_eID/Quick_Install/</a> or<br>
</li><li><a href='http://eid.belgium.be/fr/Comment_installer_l_eID/Quick_Install/'>http://eid.belgium.be/fr/Comment_installer_l_eID/Quick_Install/</a><br><br>
</li></ul></li><li>Download the "eID MW SDK 3.5.3 JARs Signed 2011-2016"<br>
<ul><li>Download the "eID MW SDK 3.5.3 JARs Signed 2011-2016" from <a href='http://code.google.com/p/eid-mw/downloads/detail?name=signed-2011-2016.zip&can=1&q='>http://code.google.com/p/eid-mw/downloads/detail?name=signed-2011-2016.zip&amp;can=1&amp;q=</a>
</li><li>Unzip signed-2011-2016.zip<br>
</li><li>Copy the following files to the examples subdirectory of the eid-javascript-lib:<br>
<ul><li>applet-launcher.jar<br>
</li><li>beid35JavaWrapper-linux.jar<br>
</li><li>beid35JavaWrapper-mac.jar<br>
</li><li>beid35JavaWrapper-win.jar<br>
</li><li>beid35libjava.jar<br>
</li><li>BEID_Applet.jar<br>
</li></ul></li><li>Rename beid35libjava.jar to beid35libJava.jar (the J in Java should be a capital J)<br><br>
</li></ul></li><li>Go to the examples subdirectory and open beid.jnlp in notepad or any other text editor.<br>The codebase directory should be changed to the examples subdirectory of the eid-javascript-lib:<br>
<pre><code>   If your examples subdirectory is C:\eid-javascript-lib\examples\<br>
<br>
   change <br>
	&lt;jnlp codebase="http://127.0.0.1/" href="beid.jnlp"&gt; <br>
   into <br>
	&lt;jnlp codebase="file:///C:/eid-javascript-lib/examples/" href="beid.jnlp"&gt;<br>
<br>
   This is also explained in readme.txt and copy_binaries.bat in the Samples\misc\Applet\Basic\java subdirectory of the eID SDK.<br>
</code></pre>
</li><li>Open beid_java_plugin.jnlp in notepad or any other text editor.<br>The codebase directory should be changed to the examples subdirectory of the eid-javascript-lib:<br>
<pre><code>   If your examples subdirectory is C:\eid-javascript-lib\examples\<br>
<br>
   change <br>
	&lt;jnlp codebase="http://127.0.0.1/" href="beid_java_plugin.jnlp"&gt; <br>
   into <br>
	&lt;jnlp codebase="file:///C:/eid-javascript-lib/examples/" href="beid_java_plugin.jnlp"&gt;<br>
</code></pre>
</li><li>Open the examples in a browser.</li></ol>

<br>
<br>
<B><br>
<br>
How to deploy the examples on a webserver<br>
<br>
</B><br>
<br>
<br>
<br>
<ol><li>I presume you have a webserver located at <a href='http://hostname.domainname.be'>http://hostname.domainname.be</a><br><br>
</li><li>Create a directory (or webcontext) named examples on your webserver.<br>Make sure the directory is accessible at <a href='http://hostname.domainname.be/examples'>http://hostname.domainname.be/examples</a> (surf with a browser to this url)<br><br>
</li><li>Copy the following files to the examples directory<br>
<ul><li>applet-launcher.jar (from signed-2011-2016.zip)<br>
</li><li>beid35JavaWrapper-linux.jar (from signed-2011-2016.zip)<br>
</li><li>beid35JavaWrapper-mac.jar (from signed-2011-2016.zip)<br>
</li><li>beid35JavaWrapper-win.jar (from signed-2011-2016.zip)<br>
</li><li>beid35libjava.jar (from signed-2011-2016.zip)<br>
</li><li>BEID_Applet.jar (from signed-2011-2016.zip)<br>
</li><li>beid.jnlp (from eid-javascript-lib)<br>
</li><li>beid_java_plugin.jnlp (from eid-javascript-lib)<br>
</li><li>example.html (from eid-javascript-lib)<br>
</li><li>Rename beid35libjava.jar to beid35libJava.jar (the J in Java should be a capital J)<br>
</li><li>if needed, other examples files from eid-javascript-lib<br><br>
</li></ul></li><li>Create a subdirectory named src in directory examples.<br>
<ul><li>Copy be_belgium_eid.js (from eid-javascript-lib) to the examples\src directory<br>
</li><li>If needed, copy base64.js (from <a href='http://hellerim.net/base64_src.php'>http://hellerim.net/base64_src.php</a>) to the examples\src directory<br>
</li><li>Make sure the directory is accessible at <a href='http://hostname.domainname.be/examples/src'>http://hostname.domainname.be/examples/src</a> (surf with a browser to this url)<br>
</li><li>If you want to put be_belgium_eid.js and base64.js in the examples directory, you need to change the following in example.html<br>
<pre><code>        change<br>
        &lt;script type="text/javascript" src="..\src\be_belgium_eid.js"&gt;&lt;/script&gt;<br>
        into<br>
        &lt;script type="text/javascript" src="be_belgium_eid.js"&gt;&lt;/script&gt;<br>
</code></pre>
</li></ul></li><li>Go to the examples directory and open beid.jnlp in notepad or any other text editor.<br>
<blockquote>The codebase parameter should be changed to <a href='http://hostname.domainname.be/examples/'>http://hostname.domainname.be/examples/</a><br>
More info about the codebase parameter: <a href='http://download.oracle.com/javase/6/docs/technotes/guides/jweb/applet/codebase_determination.html'>http://download.oracle.com/javase/6/docs/technotes/guides/jweb/applet/codebase_determination.html</a>
<pre><code>   change <br>
   &lt;jnlp codebase="http://127.0.0.1/" href="beid.jnlp"&gt; <br>
   into <br>
   &lt;jnlp codebase="http://hostname.domainname.be/examples/" href="beid.jnlp"&gt;<br>
</code></pre>
Open beid_java_plugin.jnlp in notepad or any other text editor.<br>
The codebase parameter should also be changed to <a href='http://hostname.domainname.be/examples/'>http://hostname.domainname.be/examples/</a>
<pre><code>   change <br>
   &lt;jnlp codebase="http://127.0.0.1/" href="beid_java_plugin.jnlp"&gt; <br>
   into <br>
   &lt;jnlp codebase="http://hostname.domainname.be/examples/" href="beid_java_plugin.jnlp"&gt;<br>
</code></pre>
</blockquote></li><li>Add jnlp to the configuration of your webserver<br>
<blockquote>Make sure that the webserver, for example Internet Information Services (IIS), does NOT block files with extension jnlp (or files with MIME type application/x-java-jnlp-file).<br>
The default configuration of some webservers does not allow files with extension jnlp. Therefore you need to add the extension jnlp to the default configuration.<br><br>
<ul><li>How to change configuration of Internet Information Services (IIS):<br>
<ul><li><a href='http://technet.microsoft.com/en-us/library/cc725608(WS.10).aspx'>http://technet.microsoft.com/en-us/library/cc725608(WS.10).aspx</a>
</li><li><a href='http://nirlevy.blogspot.com/2010/01/iis-jnlp-404-problem.html'>http://nirlevy.blogspot.com/2010/01/iis-jnlp-404-problem.html</a><br><br>
</li></ul></li><li>How can I add JNLP MIME-types to my ISP's Apache Web Server?<br>
<ul><li><a href='http://lopica.sourceforge.net/faq.html#apachemime'>http://lopica.sourceforge.net/faq.html#apachemime</a><br><br>
</li></ul></li><li>Web Start returns a Bad MIME Type error. What's wrong?<br>
<ul><li><a href='http://lopica.sourceforge.net/faq.html#badmimetype'>http://lopica.sourceforge.net/faq.html#badmimetype</a><br><br>
</li></ul></li><li>Unofficial Java Web Start/JNLP FAQ<br>
<ul><li><a href='http://lopica.sourceforge.net/faq.html'>http://lopica.sourceforge.net/faq.html</a>
</li></ul></li></ul></blockquote></li><li>Test your configuration<br>
<blockquote>Enter <a href='http://hostname.domainname.be/examples/beid_java_plugin.jnlp'>http://hostname.domainname.be/examples/beid_java_plugin.jnlp</a> or <a href='http://hostname.domainname.be/examples/beid.jnlp'>http://hostname.domainname.be/examples/beid.jnlp</a> in the address bar (url bar) of a browser.<br>
Normally, a Java Web Start icon or Java Web Start popup is shown, or a popup with a question if you want to download this file is shown.<br>
If a "404 Not Found" is shown, something is wrong. Check your configuration of your webserver. <a href='http://nirlevy.blogspot.com/2010/01/iis-jnlp-404-problem.html'>http://nirlevy.blogspot.com/2010/01/iis-jnlp-404-problem.html</a>
</blockquote></li><li>Open <a href='http://hostname.domainname.be/examples/example.html'>http://hostname.domainname.be/examples/example.html</a> in a browser.</li></ol>

<br>
<br>
<B><br>
<br>
Remarks<br>
<br>
</B><br>
<br>
<br>
<br>
<ol><li>The Base64 encoding only works in Internet Explorer, if JRE 6 Update 10 (Java Runtime Environment 1.6.0_10) or higher is installed<br>and if the Next-Generation Java Plug-in is enabled (this is the default setting) in the Java Control Panel.<br>The code for base64.js can be downloaded at <a href='http://hellerim.net/base64_src.php'>http://hellerim.net/base64_src.php</a><br>More details about base64 encoding are explained in the examples example_picture.html and example_upload_picture.html<br><br>
</li><li>If you are using Internet Explorer 7 or 8 on Vista to view the local examples files, it could be that the examples doesn't work.<br>Normally if you open the examples, saved in a directory on your hard disk, in Internet Explorer, there should be a warning:<br> <b>"To help protect your security, Internet Explorer has restricted this webpage from running scripts or ActiveX controls that could access to your computer. Click here for options ..."</b>.<br>If this warning is not displayed, Java applets in that webpage are blocked.<br><br>The problem is caused by Protected Mode for IE7 and IE8 in Windows Vista.<br>More info about Protected Mode for Internet Explorer at: <a href='http://blogs.msdn.com/ie/archive/2007/04/04/protected-mode-for-ie7-in-windows-vista-is-it-on-or-off.aspx'>http://blogs.msdn.com/ie/archive/2007/04/04/protected-mode-for-ie7-in-windows-vista-is-it-on-or-off.aspx</a><br><br>You can solve this problem using the following solution:<br>
<ul><li>Open the html-file.<br>
</li><li>Add a whitespace.<br>
</li><li>Delete the whitespace.<br>
</li><li>Save the html-file using a different filename.<br><br>
</li></ul></li><li>A foreigner eID card and a kids eID contains the same data as an eID card for Belgian citizens.<br>The only difference is the card number. A foreign eID card number starts with B. And a kids eID card number starts with 610.