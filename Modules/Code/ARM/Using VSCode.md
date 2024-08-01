Setup:
	Go to gitlab link
	Clone repo
	Open repo in VSCode
	Ctrl+Shift+B to compile
	F5 to Run

Common Problems:
	Watch window disappeared:
		Ctrl+Shift+P
		"workbench.views.service.panel"
	 '.devcontainer/devcontainer.json' file already exists:
		 Update VSCode and Dev Containers extension
		 Pull changes from gitlab/reclone repo

Watch Statements:
	`$rn` Register Value
	`$rn, h` Register Value (Hex)
	`*$rn` Word load
	`*(unsigned int*)$rn` Unsigned word load
	`*(short*)$rn` Halfword load
	`*(char*)$rn` Byte load
	`(int)varLabel` Memory in variable
	`(char*)&varStrLabel` Null-terminated ascii string 
	`(char*)$rn` Null-terminated ascii string
	`(int[x])*$rn` Array of x words
	`(int[x])varLabel` Array of x words
	`(int[p][q])varLabel` Matrix of size pxq

Viewing Memory:
	Ctrl+Shift+P
	"Cortex-Debug: View Memory"
	Write in start address
	Clear memory view whenever you rebuild

Allocating Memory:
	At the end of a file (Before `.end`) write this:
		`.section  .data.FILENAME`
	Create a variable with a label, then allocate memory for it using:
		`.space n`
		`.word n n n ...`
		`.halfword n n n ...`
		`.byte n n n ...`
		`.asciz "..."`

