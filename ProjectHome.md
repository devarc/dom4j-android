Dom4j use the sax parser(driver) defined in javax.xml.parsers.SAXParserFactory.

In android, the default sax parser is org.apache.harmony.xml.ExpatReader, which do not support namespace(SAX2), so some features in dom4j do not work(such as xpath).

In jdk for PC, the sax parser is com.sun.org.apache.xerces.internal.parsers.AbsractSAXParser, which support the SAX2.

So, I use another sax driver suggested on sax quich start page(http://sax.sourceforge.net/quickstart.html): org.apache.crimson.parser.XMLReaderImpl

I have test some cases but not all. They works fine.