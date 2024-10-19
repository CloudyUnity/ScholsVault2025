```xml
<OpeningTag> Data </ClosingTag>
```

Meta-Language
	

Vocab
	

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

Document Type Definition (DTD)

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