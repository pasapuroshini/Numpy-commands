
# NumPy Cheat Sheet

## Importing NumPy
```python
import numpy as np
```
# Creating an array from a list
```a = np.array([1, 2, 3]) ```

# Creating an array with zeros
```b = np.zeros((3, 3)) ```

# Creating an array with ones
```c = np.ones((2, 4))```

# Creating an array with a range of numbers
```d = np.arange(0, 10, 2)```

# Creating an array with evenly spaced numbers
```e = np.linspace(0, 1, 5)```

# Creating an identity matrix
```f = np.eye(3) ```

# Creating an array with random values
```g = np.random.random((2, 2))```

# Creating an array with random integers
```h = np.random.randint(0, 10, (3, 3)) ```

# Shape of the array
```shape = a.shape```

# Number of dimensions
```dims = a.ndim```

# Data type of elements
```dtype = a.dtype```

# Size of array (number of elements)
```size = a.size```
# The Difference Between Copy and View

The main difference between a copy and a view of an array is that the copy is a new array, and the view is just a view of the original array.

- **Copy**:
  - The copy owns the data.
  - Any changes made to the copy will not affect the original array.
  - Any changes made to the original array will not affect the copy.

- **View**:
  - The view does not own the data.
  - Any changes made to the view will affect the original array.
  - Any changes made to the original array will affect the view.

## COPY Example

Make a copy, change the original array, and display both arrays:

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
x = arr.copy()
arr[0] = 42

print(arr)
print(x)
```
View
----

*   **What is it?**: A new array object that views the data of the original array.
*   **Data Ownership**: The view does not own its data; it references the original array.
*   **Effect on Original**: Changes made to the view affect the original array, and vice versa.

### Example 1: Creating a View

python

  

```
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
x = arr.view()
arr[0] = 42

print("Original array:", arr)
print("View of the array:", x)`
```

**Output**:

  

`Original array: [42  2  3  4  5]
View of the array: [42  2  3  4  5]` 

### Example 2: Modifying the View

python

  
```import numpy as np

arr = np.array([1, 2, 3, 4, 5])
x = arr.view()
x[0] = 31

print("Original array:", arr)
print("View of the array:", x)
```

**Output**:

  

```
Original array: [31  2  3  4  5]
View of the array: [31  2  3  4  5]
```

Checking Data Ownership
-----------------------

*   **How to Check**: Use the `base` attribute.
    *   If `base` is `None`, the array owns its data.
    *   If `base` references another array, it is a view.

### Example: Checking Data Ownership

python

  

```import numpy as np

arr = np.array([1, 2, 3, 4, 5])

x = arr.copy()
y = arr.view()

print(x.base)  # Output: None
print(y.base)  # Output: Original array
```
**shape of an array(arr.shape)**
```
import numpy as np

arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])

print(arr.shape) #(2,4)

```
```
import numpy as np

arr = np.array([1, 2, 3, 4], ndmin=5)

print(arr)
print('shape of array :', arr.shape) #shape of array : (1, 1, 1, 1, 4)
```
**Reshaping a array**
```
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])

newarr = arr.reshape(4, 3)

print(newarr)
```
Output:
```

[[ 1  2  3]
 [ 4  5  6]
 [ 7  8  9]
 [10 11 12]]
```
**Sorting arrays**
```
np.sort(arr)
```
**List to Numpy Array**

```
np.asarray(list)
```
***aray of evenly spaced values --->specifying no of values required**
```
e=np.linspace(10,30,5)
print(e)
```


***aray of evenly spaced values --->specifying the step**
```
e=np.arange(10,30,5)
print(e)
```

***Transpose**

```
trans= np.transpose(array)
```
or
```
trans=array.T

```
**Searching in an array**
```
x=np.where(arrayname==item)
```

**Splitting arrays**
```
np.array_split(arr,NO_OF_PARTS)
```
**JOINING arrays**
```
np.concatenate(arr,arr2)
```

