
![[{0BDA3AB9-74D2-4C5F-9718-9671E832AD31}.png]]

```xml
<bib>
 <book year="1994">
        <title>TCP/IP Illustrated</title>
        <author><lastname>Stevens</lastname><firstname>W.</firstname></author>
        <publisher>Addison-Wesley</publisher>
        <price>65.95</price>
 </book>
 <book year="1992">
    <title>Advanced Programming in the Unix environment</title>
    <author><lastname>Stevens</lastname><firstname>W.</firstname></author>
    <publisher>Addison-Wesley</publisher>
    <price>65.95</price>
 </book>
 <book year="2000">
    <title>Data on the Web</title>
    <author><lastname>Abiteboul</lastname><firstname>Serge</firstname></author>
    <author><lastname>Buneman</lastname><firstname>Peter</firstname></author>
    <author><lastname>Suciu</lastname><firstname>Dan</firstname></author>
    <publisher>Morgan Kaufmann Publishers</publisher>
    <price>39.95</price>
 </book>
 <book year="1999">
    <title>The Economics of Technology and Content for Digital TV</title>
    <editor><lastname>Gerbarg</lastname><firstname>Darcy</firstname><affiliation>CITI</affiliation></editor>
    <publisher>Kluwer Academic Publishers</publisher>
    <price>129.95</price>
 </book> 
</bib>
```

> [!question]- ![[{EED0163D-5F20-4F11-8E56-709F5EE18B7E}.png]]
 doc("bib.xml")/bib

> [!question]- ![[{8979A202-D008-4C16-A9E7-75884D33139E}.png]]
for $book in doc("bib.xml")/bib
return $book/book/title

> [!question]- ![[{2962BF7E-5D75-4571-8D10-13A7DDBA39DC}.png]]
for $book in doc("bib.xml")/bib
return $book/book/author/firstname/text()

> [!question]- ![[{68BDCBD2-4389-48F9-B6FB-98A1E0983952}.png]]
for $book in doc("bib.xml")/bib/book
where exists($book/editor) 
return $book 

> [!question]- ![[{9DEBE70F-7DA9-46F2-AC77-B25F36A3AD9B}.png]]
for $book in doc("bib.xml")/bib/book
where $book[@year > 1998]
return $book

> [!question]- ![[{5F375917-E35A-47DF-8C03-28F3B21C2A6A}.png]]
for $book in doc("bib.xml")/bib/book
where $book/title/text() = "Data on the Web"
return $book

> [!question]- ![[{64A41FFA-EA3A-4495-9599-2E01814CF397}.png]]
for $book in doc("bib.xml")/bib/book
where $book/title/text() = "Data on the Web" 
return $book/author[2]

> [!question]- ![[{9B0DB8EF-6750-49D2-82D0-3E91EE73D758}.png]]
for $book in doc("bib.xml")/bib/book
where $book/price <= 100 and $book/price >= 50
return $book

> [!question]- ![[{6BE4E723-05E4-495C-A2CC-E8EB8ABFCB2E}.png]]
for $book in doc("bib.xml")/bib/book
where $book/publisher/text() != "Addison-Wesley"
return $book

