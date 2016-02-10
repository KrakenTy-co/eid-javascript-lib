Javascript library to be used with the applet from eID Middleware SDK version 3.5.

The library is supposed to work on Windows in Internet Explorer 5.5 and higher, in Mozilla Firefox 2 and higher, in Opera 9 and higher and Google Chrome. Also tested in Mozilla Firefox 3 on Linux. Other browsers and other platforms were not tested.

This project is not started by or has any connection with FedICT, Zetes, CSC or any organisation or company involved with the eID project. I do not work for or have any connection with these organistations or companies.

I released version 1.8 on 27/11/2011.

1.8 14/05/2011
  * Fix for [issue2](https://code.google.com/p/eid-javascript-lib/issues/detail?id=2): In Firefox 4, method GetPicture of applet returns a value of type "function". The value is converted into an array.

1.7 21/10/2010
  * Added foreigner eID and Kids-ID object.
  * Detection of foreigner eID based on card number starting with B.
  * Detection of Kids-ID based on card number starting with 610.
  * Fix: Previous versions of the library could not read the card number of a foreigner eID.
1.6 03/09/2010
  * Added reset method. This method will reset the applet and clear the picture shown in the applet.
1.5 19/12/2009
  * Added isCardPresent method. Added an example which demonstrates automatic detection of card insert and removal.
1.4 03/09/2009
  * Fix for JRE 6 Update 15: check if applet is loaded as sub applet (using applet-launcher) or as main applet (using Next-Generation Java Plug-in).
  * Fix for [issue1](https://code.google.com/p/eid-javascript-lib/issues/detail?id=1): Conversion of Java String objects returned by the applet into Javascript Number objects fails in Safari. Therefore Java String objects are first converted to Javascript String objects and then converted to Javascript Number objects.
  * Fix for [issue1](https://code.google.com/p/eid-javascript-lib/issues/detail?id=1): Dateformatter is used to format dates in toString methods of Card-, EIDCard- or SISCard objects.
1.3 16/08/2009
  * Added Dateformatter
  * If the third first name is detected while parsing the first names, it is saved in the firstName3 property.
  * If someone has three firstnames and a first and second firstname that does not contain a space, the first is saved in the firstName1 property and the second in firstName2 property.
  * Applet not found handler added.
  * Applet exception handler added.
1.2 26/04/2009
  * Added Card object. This object is the base for EIDCard and SISCard.
1.1 28/03/2009
  * The parsing of the dates on the SIS cards failed, this is corrected.
  * The parsing of the social security number on the SIS cards failed, this is corrected.
  * The getters of the EIDCard, SISCard - objects do not return Number or Boolean objects anymore, they will return primitive numbers and primitive booleans instead.
1.0 24/03/2009
  * First release