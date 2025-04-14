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


## Matrix multiplication
```python
A = [
[1 2 3]
[4 5 6]
]

B = [
[1 4]
[2 5]
[3 6]
]

if (len(A[0]) != len(B))
  print('Matrix multiplication not possible')
else:
  m = len(A)
  n = len(A[0])
  l = len(B[0])
```

###### calculate `C00` here `val`
```python
val = 0
for k in range(n):
  val += A[0][k]*B[k][0]
```


###### calculate `C0j` here `[C00 ... C0l-1]`
```python
arr = []
for j in range(l):
  val = 0
  for k in range(n):
    val += A[0][k]*B[k][j]
  arr.append(val)
```

###### calculate `Cij` here `[[C00 .. C0l-1], ... [Cm-10 .. Cm-1l-1]]`
```python
mat = []
for i in range(m):

  arr = []
  for j in range(l):
    val = 0
    for k in range(n):
      val += A[0][k]*B[k][j]
    arr.append(val)

  mat.append(arr)
```


## Transpose
```python
mat = [
[1 2 3]
[4 5 6]
[7 8 9]
]

def transpose(mat):
  m, n = len(mat), len(mat[0])
  
  if(m == n):
    for i in range(n):
      for j in range(i, n):
        mat[i][j], mat[j][i] = mat[j][i], mat[i][j]
  else:
    print('Not a square matrix transpose wont work')
```

## Reverse an Array
```python
arr = [1 2 3 4 5]

def reverse(arr):
  low = 0, high = len(arr) - 1
  while(low < high):
    arr[low], arr[high] = arr[high], arr[low]
    low++
    high--
```
## Rotate image by 90 degrees
```python
mat = [
[1 2 3]
[4 5 6]
[7 8 9]
]

output = [
[1 4 7]
[2 5 8]
[3 6 9]
]

def rotate_image(mat):
  transpose(mat)

  # reversing each col
  for i in range(len(mat)):
    reverse(mat[i])
```
## Set matrix to zeros
