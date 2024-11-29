
MB - ? Load IR_IN into FU(B) : Load RegFile(B) into FU(B)
	Also outputs as Datapath(DataOut)
	Mux B
MD - ? Load DataIn into RegFile(D) : Load FU(Out) into RegFile(D)
	Mux D

Datapath(ADD) = RegFile(A)

MW - WriteEnable for RAM
	Memory Write
MM - ? Load InstAddress into RAM : Load RegFile(A) into RAM for address
	Mux Memory 

RW - Enables writing into RegFile
DR - Dest Register (Normal)
SA - Source into A (Normal)
SB - Source into B (Normal)
TD - Dest Register (Temp)
TA - Source into A (Temp)
TB - Source into B (Temp)

IR_IN -

FS - FU Micro-op codes