
![[Pasted image 20241027194308.png]]

Removing involves searching through all elements to find outdated ones and deleting them

Linked List:
	Sorted by speed
	Record = O(N)
	Median = O(N)
	Remove = O(N)

List:
	Sorted by speed
	Record = O(N)
	Median = O(1)
	Remove = O(N^2)

Dequeue:
	Sorted by timestamp
	Record = O(1)
	Median = O(N log N)
		Copy -> Sort -> Maths = N + NlogN + 1
	Remove = O(1)

Dequeue + Heaps:
	Sorted by timestamp
	We keep track of two heaps, a min heap and max heap for fast median calculation
	Involves slower recording/removing so I won't bother going into further detail

Dequeue is the fastest method for recording so let's pick that one

```java
public class MotorwaySensor
{
	class DataPoint implements Comparable<DataPoint>
	{
		public int Speed = 0;
		public int TimeStamp = 0;
		
		@Override
		public int compareTo(DataPoint o) {
			return Speed - o.Speed;
		}
	}
	
	private Deque<DataPoint> m_dataQueue = new ArrayDeque<DataPoint>();
	MotorwaySensor()
	{
		//...
	}
	
	void removeOutdated(int timestamp)
	{
		while (m_dataQueue.size() > 0 && timestamp - m_dataQueue.getLast().TimeStamp > 60)
			m_dataQueue.removeLast();
	}
	
	void recordDataPoint(int speed, int timestamp)
	{
		DataPoint point = new DataPoint();
		point.Speed = speed;
		point.TimeStamp = timestamp;
		
		m_dataQueue.push(point);				
	}
	
	int currentMedianSpeed() // O(N) + O(N) + O(N log N) + O(1) = O(N log N)
	{
		removeOutdated(m_dataQueue.getFirst().TimeStamp); // O(N)
		
		DataPoint[] arr = m_dataQueue.toArray(new DataPoint[m_dataQueue.size()]); // O(N)
		Arrays.sort(arr); // O(N log N)
		if ((m_dataQueue.size() & 1) == 0)
		{
			int i1 = m_dataQueue.size() / 2;
			int i2 = i1 + 1;
			return (arr[i1].Speed + arr[i2].Speed) / 2;
		}
		
		int i = (int)Math.ceil((float)m_dataQueue.size() / 2.0f);
		return arr[i].Speed;
	}
}
```

WC Time Complexity of record is O(1)
WC Time Complexity of median is O(N log N)
WC Memory Complexity of record is O(1) 
WC Memory Complexity of median is O(N)

Mistakes Made:
	Used wrong Deque function names
	Forgot to pass timestamp into removeOutdated
	Wrote `T` instead of `DataPoint`, idk I'm not paying attention I guess
	Bit stuff needs brackets
		`x & 1 == 0` // Error
		`(x & 1) == 0` // Happy
	Tried to add datapoints together instead of their speeds
	Forgot to implement Comparable interface for DataPoint to allow it to be sorted...oops

NOTE:
	Untested code, no compiler errors