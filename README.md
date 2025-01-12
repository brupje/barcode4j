# Barcode4J

Barcode4J is a flexible generator for barcodes written in Java.

Website: http://barcode4j.sourceforge.net

For instructions on how to get started please read the documentation on the
website or the one included in the binary distribution.

If you need any assistance please post questions on the following mailing list:
barcode4j-users@lists.sourceforge.net

You can subscribe here: http://sourceforge.net/mail/?group_id=96670

We appreciate any feedback (positive or negative). This helps us to improve the
package.

We would like to invite you to participate in the development of Barcode4J.
The development mailing list is barcode4j-developers@lists.sourceforge.net


## Installation in Tomcat

This step requires apache fop 2.6

1. Copy barcode4j-fop-ext-complete.jar into <TOMCAT_ROOT>/webapps/fop/WEB-INF/lib
2. Place avalon-framework-impl-4.2.0.jar  into <TOMCAT_ROOT>/lib
3. Restart apache tomcat


##  XSL-FO Example

This example renders a barcode from a XML data

```
<fo:block>
  <fo:instream-foreign-object>
    <barcode:barcode xmlns:barcode="http://barcode4j.krysalis.org/ns"  orientation="0">
          <xsl:attribute name="message">
          <xsl:value-of select="BARCODE" />
          </xsl:attribute>
      <barcode:code128>
        <barcode:height>16mm</barcode:height>
      </barcode:code128>
    </barcode:barcode>
  </fo:instream-foreign-object>
</fo:block>
```                


*************************************

Barcode4J is licensed under the the Apache License, Version 2.0.
The license text can be found under legal/barcode4j.LICENSE.txt.
