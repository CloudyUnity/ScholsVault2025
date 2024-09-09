Object Management Group (OMG)
	A computer industry standards consortium

Views
	Structural
		Static
		Design
		Use Case
	Dynamic
		State Machine
		Activity 
		Interaction
	Physical
		Deployment
	Model Management
		Profile

Use Case Diagrams
	Used to communicate the scope of the tasks your IM supports and for whom
	Actors represent roles/users/external systems
		Composed of a name and optional description
	Lines/Arrows show involvement 
	Use Cases represent functionality
		Composed of name, actors, entry/exit conditions, event flow, requirements
		Named with verbs
	Boxes show scope/boundaries

Involvement Modifiers	
	Factored out of main event flow
	`<<extends>>`
		These go on lines for seldom invoked use case 
		#todo 
	`<<includes>>`
		Used to avoid repetition of use cases
		Represents common functionality 
		#todo 

Use Case Model
	The set of all use cases describing the functionality of the system

Naming Rules
	No abbreviations/acronyms
	No computer terms
	No spaces, use snake_case or PascalCase

Objects are Instances of Classes

Class Diagram
	Composed of class name, attributes, operations

Attribute
	A named property of a class describing a range of values a property may have
	Type
		Either UML predefined types, model types or programming types
	`[visibility] [name] [multiplicity] [:type] [= initial-value] [{property-string}]`
	+ Public
	- Private
	Multiplicity is the range of possible values
		`[0..1]`, `[n..*]`#

Operation
	A service that you can request on an object
	Aka functions