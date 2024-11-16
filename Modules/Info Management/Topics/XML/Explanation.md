
```xml
<OpeningTag> Data </ClosingTag>
```

Tags that contain other tags are CDATA
Tags that contain data are PCDATA (Parsed)

Markup Indicators == Tags

Meta-Language
	XML/SGML
	...

Vocabulary
	HTML/SVG/XTM
	...

Standard Generalised Mark-Up Language (SGML)
	ISO Standard since 1986
	Meta-Language for defining document markup vocab
	HTML is a SGML vocab

Supporting SGML on the web was too difficult so HTML made simplifications
	Not extensible 
	Limited structure
	Not content oriented
	Cannot be validated 

XML is another simplified subset of SGML but retains the lost features of HTML
	XML is also a meta-language
	Easy to read by both humans and computers
	Self describing
	Cannot have spaces in tag names
	Cannot start tag with "XML"

XML Declaration 
	Required 
	Informs the xml version, character encoding, whether or not external declarations affect the doc
```xml
<?xml version='1.0' encoding='ISO-8859-1' standalone='no' ?>
```

Attributes
```xml
<Tag att="attVal"> Data </Tag>
```

Empty Tag
```xml
<Tag></Tag>
<SelfClosingTag/>
```

Comments
```xml
<!-- one-line -->
<!--
Multi
line
-->
```

Document Type Definition (DTD)
	Defines the structure of a XML doc
	Defines elements/cardinality/attributes/aggregation 
	Validates XML docs
	Can be external or internal to XML doc
	Occurrences:
		$?$ = 0/1
		$+$ = 0+
		$*$ = 1+
```dtd
<!DOCTYPE database [ <!-- database is root -->
<!ELEMENT database (person*)> <!-- database contains 0+ persons -->
<!ELEMENT person (name, hobby*)> <!-- person contains name and 0+ hobbies -->
<!ATTLIST person age CDATA #IMPLIED> <!-- person contains age attribute ??? -->
<!ELEMENT name (title?, firstname+, surname)> <!-- name has 0/1 title, 1+ firstname and a surname -->
<!ELEMENT hobby (#PCDATA)> <!-- hobby is PCDATA -->
]>
```

XQuery

XPath

XLink

XBase

XPointer

Resource Description Framework (RDF)

RDF Schema

XML Schema

RelaxNG

Topics Maps

Ontology Web Language

UML Class to XML
```xml
<ClassName>
	<ClassName.var1> var1Val </ClassName.var1>
	<ClassName.var2> var2Val </ClassName.var2>
	...
</ClassName>
```

UML Class to XML with Inheritance
```xml
<SubClassName>
	<ParentClassName.var1> var1Val </ParentClassName.var1>
	<ParentClassName.var2> var2Val </ParentClassName.var2>
	...
	<SubClassName.var3> var3Val </SubClassName.var3>
	<SubClassName.var4> var4Val </SubClassName.var3>
	...
</SubClassName>
```

UML Class to XML Associations
Assume ClassName points to ClassName2
```xml
<ClassName>
	<ClassName2 idref="s1"/>
</ClassName>

<ClassName2 id="s1">
	...
</ClassName2>
```

XML Validator:
	https://www.xmlvalidation.com/