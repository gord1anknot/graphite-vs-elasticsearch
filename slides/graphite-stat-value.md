## Stats - Values

```python
	float('nan')
	float('-inf')
	float('+inf')
```

These python types represent floating point numbers, ultimately platform 
specific implementations of IEEE 754 numbers. Although they can be stored in 
whisper archives, tools (graphite-web in particular) will coerce them to None.

```python
	None
```

None, the python null, represents the absence
of a measurement at a given timestamp.
