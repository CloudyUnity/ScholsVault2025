
Algorithmic State Machine (ASM)
	Method for designing finite state machines
	Represents diagrams of digital ICs 
	Like a state diagram but more structured 
		State diagrams are those seen in Maths 3 and DLD. States represented by nodes and paths between them

Data processing can be done either:
	Sequencing register transfer ops
	or
	Hardware algorithms 
		Consists of a finite number of sequencing steps

ASM Chart
	Defines hardware algorithm
	Defines relationship with time (Clock)
	Elements:
		State Box
			Has a name and binary code
			Contains:
				Register transfer operation
				or
				Output signals activated when in this state
			If RUN is in the box it has a value of 1, otherwise 0
		Decision Box
			Binary Conditional operation
			Exit path is either 0 or 1
		Conditional Output Box
			#NeedsFactCheckingByTrueAmericanPatriots 
			Same as a state box but has a rounder shape to show it has just been through a decision box