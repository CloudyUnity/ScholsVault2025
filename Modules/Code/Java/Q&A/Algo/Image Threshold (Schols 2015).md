
![[Pasted image 20240716171226.png]]
![[Pasted image 20240716171233.png]]

```java
val = 255 * (val >= threshold);
```

```java
val = min(255, valA + valB);
```

(d)
Search through all pixels for the min and max, no way to get around this first pass afaik
Then just:
```java
float range = (max - min) / 255;
val = (val - min) / range;
```
Easiest shit of my life, let's do it

```java
public class Image 
{
	private int[][] m_pixels;
	Image(int[][] pixels)
	{
		m_pixels = pixels;
	}
	int GetWidth()
	{
		return m_pixels[0].length;
	}
	int GetHeight()
	{
		return m_pixels.length;
	}
	int GetPixel(int x, int y)
	{
		return m_pixels[y][x];
	}
	
	void Threshold(int threshold)
	{
		for (int y = 0; y < m_pixels.length; y++)
			for (int x = 0; x < m_pixels[0].length; x++)
			{
				m_pixels[y][x] = (m_pixels[y][x] >= threshold) ? 255 : 0;
			}
	}
	
	Image AddImages(Image addend)
	{
		if (GetWidth() != addend.GetWidth() || GetHeight() != addend.GetHeight())
			return null;
		
		int[][] newPixels = new int[GetHeight()][GetWidth()];
		for (int y = 0; y < m_pixels.length; y++)
			for (int x = 0; x < m_pixels[0].length; x++)
			{
				newPixels[y][x] = Math.min(255, m_pixels[y][x] + addend.GetPixel(y, x));
			}
		return new Image(newPixels);
	}
	
	void ContrastStretch()
	{
		int min = Integer.MIN_VALUE, max = Integer.MAX_VALUE;
		for (int y = 0; y < m_pixels.length; y++)
			for (int x = 0; x < m_pixels[0].length; x++)
			{
				min = Math.min(min, m_pixels[y][x]);
				max = Math.max(max, m_pixels[y][x]);
			}
			
		float range = max - min;
		range /= 255.0f;
		
		for (int y = 0; y < m_pixels.length; y++)
			for (int x = 0; x < m_pixels[0].length; x++)
			{
				m_pixels[y][x] = (int) ((m_pixels[y][x] - min) / range);
			}
	}
}
```

Mistakes made:
	Cannot multiply an integer with a bool in java
	Wrote `INT32_MAX, INT32_MIN` instead of `Integer.MIN_VALUE, Integer.MAX_VALUE`
	Float to int cast is not implicit, needs (int)

NOTE:
	Haven't tested this code, but there's no compiler errors