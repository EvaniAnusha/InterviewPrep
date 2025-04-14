## Two Sum (Brute force)
```python
nums = [2, 7, 11, 15]
tar = 26
```

```python
for i in range(nums):
  # linear_search(0, i, nums)
  for j in range(0, i):
    if(nums[i] + nums[j] == tar):
      return [nums[i], nums[j]]
```

## Two Sum (BinarySearch)
```python
for i in range(nums):
  # binary_search(0, i, nums)
```

## Two Sum (Optimal)
```python
mp = dict()
for i in range(nums):
  comp = tar - nums[i]
  if (comp in mp):
    return [mp[comp], i]
  else:
    mp[comp] = i
```
