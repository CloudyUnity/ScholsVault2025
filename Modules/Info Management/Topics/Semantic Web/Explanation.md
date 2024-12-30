
#todo 
	Write down benefits and challenges of every topic.
	Make sure you understand EVERYTHING REALLY WELL

Challenges with managing data
	Volume
		Too much data, not enough storage
	Velocity
		Data needs to processed as its streamed to maximize value
	Validity
		Data protections, privacy and ethics
	Variety
		Not all data is structured (text, audio, video, etc)

The web has made data easily available due to easy publication and infrastructure for retrieving, representing docs and accessing data

Semantic Interoperation
	Understanding what data means
	Linking data in insightful ways
	Automated support for data integration
	Smart applications

Web of Documents
	Created by humans for humans
	Links between docs have little meaning for machines and little structured info
	Like a global file system of documents

Web of Data
	Like a global database of descriptions
	Links between things have high structure 
	Designed for both humans and computers 

Ontology
	The formal structured representation of knowledge
	Defines concepts, relationships and rules
	e.g. Classes, Properties, Instances, etc

The Semantic Web
	This is a web of data
	Provides an env where apps can query data, draw inferences using vocab, etc
	Needs a huge amount of data in a standard format. Relationships among data needs to be available 
	The web is an abstract idea/goal, not an existing physical thing

The Semantic Web Stack
	The stack is not an abstract idea, it is a technical realization to achieve the semantic web using various technologies like RDF/OWL/XML/etc
	Advantages over traditional web stack:
		More standardised 
		More powerful searches and queries based on meaning rather than keywords
		Data has more context
		Ontologies can derive new insights and relationships between data
	Disadvantages:
		More complex, higher learning curve
		Performance is slower and more resource intensive 
		Less secure due to more linking and sharing of data
		Protecting against misuse remains a challenge
	Layers:
		Base Layers
			URI/Unicode			
		Data Layers
			XML/XML Schema
			RDF/RDFS
		Knowledge Layers
			OWL
			Rules (RIF/SWRL)
		Query Layer
			SPARQL		
		Logic/Proof/Trust Layers:
			Description Logics/Logic Frameworks
			Proof/Trust
			Cryptography
		Top Layer:
			User Interface

Linked Data
	Started off as an initiative called the Linking Open Data (LOD) project
	A global initiative to publish and interlink structured data on the web 
	Used standardized technologies:
		Uniform Resource Identifiers (URI) to name things
		Resource Description Framework (RDF) to represent things
		HTTP Infrastructure to obtain those representations 
	Advantages:
		Has improved data integration and interoperability, can combine data from different sources seamlessly 
		Datasets are more discoverable and accessible 
		Data has more context/meaning allowing more intelligent programs 
	Disadvantages:
		More complex, higher learning curve
		Harder to scale and keep up to date
		Ensuring data and relationship quality is a challenge

Uniform Resource Identifier (URI)
	Compact sequence of chars identifying an abstract or physical resource
	`URI = scheme://hier-part [? query] [# fragment]`
	Example:
		http://scheme.com:8042/path?name=ferret#nose
	Scheme is not the same as protocol 
	When URIs use the `http:` scheme they can be looked up by dereferencing the URI over the HTTP protocol 
	Humans see HTML, PDFs, Images
	Machines want formats like RDF
	Scheme:
		Indicates how the resource should be accessed and what tools to use to do so
		Examples:
			`http:`, `htpps:`, `mailto:`, `ftp:`
	Protocol:
		Set of rules and standards on how data is transferred over a network
		There's Application Layer Protocols (`http`), Transport Layer Protocols (`TCP`) and Network Layer Protocols (`IP`)
	Hier-Part:
		Contains the authority/domain and optionally the path
		Examples:
			`//example.com/path/to/smth`
			`//user.password@host.com:8080/folder/file`
	Query:
		Contains a query to interact with the resource
		Examples:
			`?key1=val1&key2=val2`
			`?category=books&lang=en`
	Fragment:
		Used to access a subsection of a HTML document
		Examples:
			`#top`
			`#section3`
	Advantages:
		Global uniqueness, no resources are confused with each other
		Interoperability 
		Identify resources by location but also can be persistent identifiers ensuring longevity if the resource moves
		Very machine and human readable
		Very extendible for the future
	Disadvantages:
		If URIs are not careful link rot can occur where links are outdated or expired
		Dynamically generated URIs can be hard for humans to parse
		Sometimes ambiguous in usage (URI for Paris might refer to city or webpage about Paris)
		Server issues can make URIs inaccessible 
		Malicious actors can use phishing URIs to mislead people into harmful resources

Non-Information Resources (NIR)
	Opposite of Information Resources (IR)
	URI pointing to a IR returns representation of info e.g. HTML
	URI pointing to NIR returns redirect to IR that provides metadata

Data
	When a resource is accessed it returns data and metadata 
	Metadata can include information within the HTPP headers and HTTP response code 

Code 303 "See Other" indicates there is no representation for the accessed URI but associated info may be available at a different provided URI 

NIR URI Processing Styles
	303 Redirect
		Large dynamic data sets 
		Flexible as redirection can be configured for each resource 
	`#URIs` 
		Add fragments to URIs
		Small static data sets
		Reduced number of HTTP round trips thus less latency
		Single request retrieves entire document
		May transmit unnecessary data across web
		Used for vocabulary definitions

Resource Description Framework (RDF)
	Used to express information graphs
	Represents info using a triple structure (Subject, Predicate, Object)
	Information built up as a collection of these triples contained within an XML file 
	Graphs can be viewed as nodes and arcs where nodes store facts and arcs store relationships
	Or as triplets where object is related to subject by predicate 
	RDF can live inside XML docs
		`<rdf:RDF xmlns:rdf="URI"></rdf:RDF>`
		`<rdf:Description rdf:about="URI"><voc:title>Christ</voc:title> <voc:topic>Cats</voc:topic> </rdf:Description>`

RDF provides a way of building graphs from triples but doesn't have constraints. It is untyped mechanism 
This can cause issues as people may interpret the predicates differently 

RDF Schema (RDFS)
	Extends RDF with schema vocab
	Schema Terms
		Class, Property, type, subClassOf, range, domain
	These replace the predicate part of triples
	Too weak to describe resources in sufficient detail
		No localised range and domain constraints
		No existence/cardinality constraints 
		No transitive, inverse of symmetrical properties 

Ontology Web Language (OWL)
	Ontology = Formalized vocab of terms
	Standardised by W3C
	Covering a specific domain and shared by a community of users 
	OWL has a richer vocab and more expressive than RDFS
	Example:
		`<owl:Class rdf:ID='Room'/>`
		`<owl:Class rdf:ID='Restroom'> <rdfs:subClassOf rdf:resource='#Room'/> </owl:Class>`
	Has other mechanisms for defining classes
		`equivalentClass`
			Classes are synonymous
		`disjointWith`
			Instance of class cannot be an instance of other
		`unionOf`
			Class contains things from more than one class
		`intersectionOf`
			Class contains things in both in one and other
		`complementOf`
			Class contains things that are not other things (Children are not SeniorCitizens)
	`rdf:Property` is used to relate resources together or relate a resource to a `rdfs:Literal` or datatype 
	`owl:ObjectProperty` can relate resources together
	`owl:DataProperty` relates resources to `rdfs:Literal` or XML schema data type
	Properties
		Symmetric
			If (x, y) is an instance then (y, x) is an instance 
		Transitive 
			Is (x, y) and (y, z) are instances of P then (x, z) is an instance of P
		Functional
			Property has most one value for each individual 
		InverseOf
			If x is related to y by property2 then y is related to x by property1
		InverseFunctionalProperty
			The inverse property has most one value for each individual 

![[{A51A7BEA-08EB-4D90-A122-64E1C06F59B7}.png]]
