
![[Pasted image 20240716170012.png]]
![[Pasted image 20240716170025.png]]

Ok so the goal is to go through each section of the buffer, get its type, pass it into a function and place the decoded message into an output buffer

while (pCur):
	msgStart = pCur;
	msgEnd = msg_part_end();
	if (!msgEnd)
		return 400;
	type = msg_part_type();
	if (!type)
		return 401;
	fn = mapping.get(type);
	if (fn)
		decode = fn(msgStart, msgEnd);
		decodeBuffer += decode;
	pCur = msg_part_next();

Keep in mind:
	Msg_Decode can be max 75 lines
	Memory leaks are not allowed

I also need to figure out how to allocate and place data into the decode buffer. Should probably make it more dimensional

(a)
```c
struct decoded_msg {
	struct decoded_msg** NestedMsgs;
	size_t NestedAmount;
	
	unsigned char** Msgs;
	size_t* MsgLengths;
	size_t MsgAmount;
}
```
Is it better to use void*? I don't know what other things return...

Ok this is insane I'll come back to it