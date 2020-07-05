One of the many ways to filter a list is using list comprehension:

```python
numbers = [0, 15, -2, -9, 3]
positive_numbers = [n for n in numbers if n > 0]
print(positive_numbers) # => [15, 3]
```
