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
			They show optional/extended functionality for edge cases 
			Example:
				`Purchase Product <<extends>> Apply Discount`
		`<<includes>>`
			Used to avoid repetition of use cases
			Represents common mandatory functionality 			
			Example:
				`Checkout <<includes>> Validate Payment`

Use Case Model
	The set of all use cases describing the functionality of the system

Naming Rules
	No abbreviations/acronyms
	No computer terms
	No spaces, use snake_case or PascalCase

Objects are Instances of Classes

Class Diagram
	Composed of class name, attributes, operations
	Only the name is mandatory 
	Attribute
		`+Name`
	Attribute with Signature
		`-Length : int`
	Operation with Signature
		`+getLength(n : int) : void`
	Signature Syntax:
		`boolean`
		`String`
		`int`
		`void`
		`MyClass*`
		`float`
	Visibility
		`+` Public
		`-` Private
		`#` Protected
	Directionality
		`Foo(in arg : type) : type`
		`Foo(out arg : type) : type`
		`Foo(inout arg : type) : type`
	Relationships
		![[{21B9D4C1-9005-49E5-B798-1777F8A9D00A}.png]]
			Association:
				Shows a general connection
			Inheritance/Generalisation 
				Same as in CS
				Arrow points towards superclass
			Realization
				Same as an interface
				Arrow points towards interface
			Dependency
				Shows that one requires/uses the other for some operation
				Arrow points to the "used" 
			Aggregation
				Shows that items of one form the other but can also exist by themselves
				Diamond points to the "whole"
			Composition
				Shows that items of one form the other and cannot exist by themselves
				Diamond points to the "whole"
		Multiplicity
			Placed on relationships to show how many instances of one relate to the other
			`1`, `0`, `0..1`, `*`, `0..*`

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