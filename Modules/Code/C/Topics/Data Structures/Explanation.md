
Sneaky Queue
	Create an array longer than the queue will ever reach. This is not a renewable queue! 
	Assign two index pointers to 0 for the front and rear of the queue
	When you add something to the queue put it on the rear and increment rear
	When you take something off the queue take it from the front and increment front
	If `front >= rear` then the queue is empty