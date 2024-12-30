Summary:
	Cancer treatment machine (Therac-25) was the first to use software in 1985
	They employed a hobbyist programmer to do the software stuff
	The hardware side had no proper limits in place to prevent accidents
	The machine often printed out error codes with no manual to decode them, as such users became desensitised to them
	One warning, Warning 53 was caused by trying to change the ray type while the magnetic disks were rearranging. This software error caused tens of thousands of rads to be sent into the patient 
	The company failed to notice, address and solve this issue, leading to many many deaths

This wasn't a one-off incident. Many more radiation overdose accidents have occurred since

The Issues:
	Overconfidence in software:
		There's a widespread belief that software doesn't fail
		In safety critical systems today some hardware backups/interlocks are being replaced or controlled by software 
		Systems need more protection against software errors
		Hardware doesn't have single-point-failures where if one thing goes wrong it can have serious consequences. Software needs to be the same
	No hardware limits:
		Many of the same software issues in the Therac-25 were also in the Therac-20 but it wasn't as dangerous then because of hardware limits 
	Company stuff...

There's a misunderstanding that software problems come from implementation errors rather than requirement flaws. Nearly all modern safety measures are built upon ensuring implementation but not for requirements. Safety needs to be considered from the beginning 

Often in post-incident/accident reports the blame is put on operators and a quick patch is made rather than trying to understand the underlying issues. 

Some software has inadequate practices. What might be ok for a website is not always ok for safety-critical software. It should be considered malpractice for software to be created without safety requirements. Software designs are often unnecessarily complex. OOP is not ideal for control-oriented systems, the code is more difficult to test for safety, trace from requirements to code, maintain without affecting safety and assure the correctness of changes.

Defensive design is not always emphasized. Ways to detect or prevent software errors should be designed from the beginning. Programming languages that provide error checking like strong type checking aren't always as popular in safety-critical systems. This is why C/C++ are trying to be replaced with Zig/Rust in certain fields.

Software designers don't work with human factors engineers enough. Software can often be very confusing, yet operators get the blame for accidents

A lot of the software from Therac-25 was reused from the Therac-20, there's a misconception that because the code was tested extensively you can reuse it without risk which is misguided. 

Sometimes making UIs more friendly conflicts with making them more safe. For example removing multiple data entry or confirmation windows to improve workflow but increase risk