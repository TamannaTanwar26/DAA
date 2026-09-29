# DAA
Design and Analysis of Algorithms Program

## Program 1: Graphs using Matplotlib
# Aim: To plot single-line and multiple-line graphs using Matplotlib.
```
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y1 = [2, 4, 6, 8, 10]
y2 = [1, 3, 5, 7, 9]

plt.plot(x, y1, marker='o', label='Line 1')

plt.plot(x, y2, marker='s', label='Line 2')

plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Single and Multiple Line Graph")

plt.legend()

plt.grid(True)

plt.show()
```
<img width="1863" height="919" alt="Screenshot 2026-09-29 173826" src="https://github.com/user-attachments/assets/6e240f80-f685-4e60-8189-82cb91c05137" />


## Program 2: Time Execution
# Aim: To calculate and display the execution time of a program
# using the time and timeit modules.
```
import time
import timeit

# Using time module
start_time = time.time()

total = 0
for i in range(1, 1000001):
    total += i

end_time = time.time()

execution_time = end_time - start_time

print("Sum:", total)
print("Execution time using time module:", execution_time, "seconds")


# Using timeit module
def calculate_sum():
    total = 0
    for i in range(1, 1000001):
        total += i
    return total

time_taken = timeit.timeit(calculate_sum, number=1)

print("Execution time using timeit module:", time_taken, "seconds")
```
<img width="1107" height="940" alt="Screenshot 2026-09-29 175624" src="https://github.com/user-attachments/assets/c3477f54-1e02-4ed7-a21a-c0eacbadba51" />

## Program 3: Memory Used
# Aim: To measure and display the memory used during program execution
# using sys and tracemalloc modules.
```
import sys
import tracemalloc

# Using sys module
numbers = [1, 2, 3, 4, 5]

memory_size = sys.getsizeof(numbers)

print("Memory used by the list using sys module:", memory_size, "bytes")


# Using tracemalloc module
tracemalloc.start()

data = [i for i in range(10000)]

current, peak = tracemalloc.get_traced_memory()

print("Current memory usage:", current, "bytes")
print("Peak memory usage:", peak, "bytes")

tracemalloc.stop()
```

<img width="1912" height="940" alt="image" src="https://github.com/user-attachments/assets/b9070993-be58-4c78-9acc-16fa55a97df2" />

## Program 4: Time Complexity
# Aim: To plot and compare different time complexities using Matplotlib.
```
import matplotlib.pyplot as plt
import math

n = list(range(1, 11))

# Different time complexities
o1 = [1 for x in n]
ologn = [math.log2(x) for x in n]
on = n
onlogn = [x * math.log2(x) for x in n]
on2 = [x ** 2 for x in n]
on3 = [x ** 3 for x in n]
o2n = [2 ** x for x in n]
on_factorial = [math.factorial(x) for x in n]

# Plot all complexities
plt.plot(n, o1, label="O(1)")
plt.plot(n, ologn, label="O(log n)")
plt.plot(n, on, label="O(n)")
plt.plot(n, onlogn, label="O(n log n)")
plt.plot(n, on2, label="O(n²)")
plt.plot(n, on3, label="O(n³)")
plt.plot(n, o2n, label="O(2ⁿ)")
plt.plot(n, on_factorial, label="O(n!)")

# Labels and title
plt.xlabel("Input Size (n)")
plt.ylabel("Operations")
plt.title("Comparison of Time Complexities")

# Legend and grid
plt.legend()
plt.grid(True)

# Display graph
plt.show()
```
<img width="1886" height="994" alt="image" src="https://github.com/user-attachments/assets/ce40c099-6e29-4e9d-a1a1-37432aa2f5ed" />

## Program 5: Linear Search
# Aim: To search for a given element in an array using Linear Search.
```
# Input array
arr = [10, 20, 30, 40, 50]

# Element to search
key = int(input("Enter the element to search: "))

# Linear Search
found = False

for i in range(len(arr)):
    if arr[i] == key:
        print("Element found at index:", i)
        found = True
        break

if not found:
    print("Element not found in the array.")
```
<img width="1854" height="896" alt="image" src="https://github.com/user-attachments/assets/11a75c48-c5b0-4344-a88c-e94fb9d1b393" />

## Program 6: Largest Element
# Aim: To find the largest element in an array.
```
arr = [10, 25, 7, 45, 18, 32]

largest = arr[0]

for i in range(1, len(arr)):
    if arr[i] > largest:
        largest = arr[i]

print("Array:", arr)
print("Largest element:", largest)
```
<img width="1311" height="915" alt="image" src="https://github.com/user-attachments/assets/0f1121e8-e6e6-4d9a-9b05-30b2560c828d" />

## Program 7: Smallest Element
# Aim: To find the smallest element in an array.
```
arr = [10, 25, 7, 45, 18, 32]

smallest = arr[0]

for i in range(1, len(arr)):
    if arr[i] < smallest:
        smallest = arr[i]

print("Array:", arr)
print("Smallest element:", smallest)
```
<img width="1333" height="909" alt="image" src="https://github.com/user-attachments/assets/71b3c3b0-52d0-4f99-ad5f-bc571f444f4d" />

## Program 8: Bubble Sort – Ascending Order
# Aim: To sort an array in ascending order using Bubble Sort.
```
arr = [64, 34, 25, 12, 22, 11, 90]

n = len(arr)

for i in range(n - 1):
    for j in range(n - i - 1):
        if arr[j] > arr[j + 1]:
            arr[j], arr[j + 1] = arr[j + 1], arr[j]

print("Sorted array in ascending order:", arr)
```
<img width="1296" height="914" alt="image" src="https://github.com/user-attachments/assets/588ef727-f1b0-4c45-93b6-1c03526fbb1a" />

## Program 9: Bubble Sort – Descending Order
# Aim: To sort an array in descending order using Bubble Sort.
```
arr = [64, 34, 25, 12, 22, 11, 90]

n = len(arr)

for i in range(n - 1):
    for j in range(n - i - 1):
        if arr[j] < arr[j + 1]:
            arr[j], arr[j + 1] = arr[j + 1], arr[j]

print("Sorted array in descending order:", arr)
```
<img width="1549" height="900" alt="image" src="https://github.com/user-attachments/assets/a8756b6a-04a6-48e5-a94d-d095e4b644e9" />

## Program 10: Insert Element at the End
# Aim: To insert a new element at the end of an array.
```
arr = [10, 20, 30, 40, 50]

print("Original array:", arr)

element = int(input("Enter the element to insert: "))

arr.append(element)

print("Array after insertion:", arr)
```
<img width="1747" height="963" alt="image" src="https://github.com/user-attachments/assets/160c7d35-53b9-42d5-b39f-16697eafc162" />

## Program 11: Insert Element at a Specified Position
# Aim: To insert a new element at a specified position in an array.
```
arr = [10, 20, 30, 40, 50]

print("Original array:", arr)

element = int(input("Enter the element to insert: "))
position = int(input("Enter the position: "))

if 0 <= position <= len(arr):
    arr.insert(position, element)
    print("Array after insertion:", arr)
else:
    print("Invalid position.")
```
<img width="1781" height="947" alt="image" src="https://github.com/user-attachments/assets/2a1bfdb7-1e78-4474-8998-5b1b3aabda4b" />

## Program 12: Delete Element from a Specified Position
# Aim: To delete an element from a specified position in an array.
```
arr = [10, 20, 30, 40, 50]

print("Original array:", arr)

position = int(input("Enter the position to delete: "))

if 0 <= position < len(arr):
    deleted = arr.pop(position)
    print("Deleted element:", deleted)
    print("Array after deletion:", arr)
else:
    print("Invalid position.")
```
<img width="1851" height="940" alt="image" src="https://github.com/user-attachments/assets/c8481f97-3d0f-434d-a4fd-fbfb3acec57e" />

## Program 13: Delete Element by Value
# Aim: To delete a given value from an array by first searching for it.
```
arr = [10, 20, 30, 40, 50]

print("Original array:", arr)

value = int(input("Enter the value to delete: "))

if value in arr:
    arr.remove(value)
    print("Element deleted:", value)
    print("Array after deletion:", arr)
else:
    print("Element not found in the array.")
```
<img width="1401" height="918" alt="image" src="https://github.com/user-attachments/assets/943e3870-490a-449e-aa6a-2a767c244ad5" />

## Program 14: Factorial using Recursion
# Aim: To find the factorial of a given number using recursion.
```
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)


num = int(input("Enter a number: "))

if num < 0:
    print("Factorial is not defined for negative numbers.")
else:
    result = factorial(num)
    print("Factorial of", num, "is:", result)
```
<img width="1846" height="897" alt="image" src="https://github.com/user-attachments/assets/ca25bffc-cf5f-48d7-801b-4a598bf649aa" />

## Program 15: Sum of Numbers using Recursion
# Aim: To find the sum of natural numbers up to a given number using recursion.
```
def sum_natural(n):
    if n == 0:
        return 0
    else:
        return n + sum_natural(n - 1)


num = int(input("Enter a number: "))

if num < 0:
    print("Please enter a positive number.")
else:
    result = sum_natural(num)
    print("Sum of natural numbers up to", num, "is:", result)
```
<img width="1843" height="971" alt="image" src="https://github.com/user-attachments/assets/ce2fd41a-af93-407e-a17d-622eeea44955" />

## Program 16: Fibonacci Series using Recursion
# Aim: To generate the Fibonacci series using recursion.
```
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)


terms = int(input("Enter the number of terms: "))

if terms <= 0:
    print("Please enter a positive number.")
else:
    print("Fibonacci Series:")

    for i in range(terms):
        print(fibonacci(i), end=" ")
```
<img width="1885" height="963" alt="image" src="https://github.com/user-attachments/assets/50eea036-6f65-4cab-b875-45fb83d8aceb" />

## Program 17: Graph Representation using Classes and Objects
# Aim: To represent a graph using Node and Graph classes
# and display it using an adjacency list.
```
class Node:
    def __init__(self, data):
        self.data = data


class Graph:
    def __init__(self):
        self.adjacency_list = {}

    def add_vertex(self, vertex):
        if vertex not in self.adjacency_list:
            self.adjacency_list[vertex] = []

    def add_edge(self, vertex1, vertex2):
        self.add_vertex(vertex1)
        self.add_vertex(vertex2)

        self.adjacency_list[vertex1].append(vertex2)
        self.adjacency_list[vertex2].append(vertex1)

    def display(self):
        print("Adjacency List:")
        for vertex in self.adjacency_list:
            print(vertex, "->", self.adjacency_list[vertex])


# Create graph
graph = Graph()

# Add vertices
vertices = ["A", "B", "C", "D", "E"]

for vertex in vertices:
    node = Node(vertex)
    graph.add_vertex(node.data)

# Add edges
graph.add_edge("A", "B")
graph.add_edge("A", "C")
graph.add_edge("B", "D")
graph.add_edge("C", "D")
graph.add_edge("D", "E")

# Display graph
graph.display()
```
<img width="1858" height="976" alt="image" src="https://github.com/user-attachments/assets/0cb4e458-bcb6-411f-b43d-650e1608cb6d" />

## Program 18: Represent the Given Directed Graph
# Aim: To represent a directed graph using classes and objects
# and display it using an adjacency list.
```
class Node:
    def __init__(self, data):
        self.data = data


class Graph:
    def __init__(self):
        self.adjacency_list = {}

    def add_vertex(self, vertex):
        if vertex not in self.adjacency_list:
            self.adjacency_list[vertex] = []

    def add_edge(self, source, destination):
        self.add_vertex(source)
        self.add_vertex(destination)

        # Directed edge
        self.adjacency_list[source].append(destination)

    def display(self):
        print("Adjacency List:")
        for vertex in self.adjacency_list:
            print(vertex, "->", self.adjacency_list[vertex])


graph = Graph()

# Add vertices here according to the given graph
vertices = ["A", "B", "C", "D", "E"]

for vertex in vertices:
    node = Node(vertex)
    graph.add_vertex(node.data)

# Add directed edges according to the given graph
# Example:
# graph.add_edge("A", "B")
# graph.add_edge("A", "C")

graph.display()
```
<img width="1428" height="997" alt="image" src="https://github.com/user-attachments/assets/89452a74-5a3a-4a9c-92b0-3fa5d6e5b690" />

## Program 19: Represent the Given Directed Graph
# Aim: To represent a directed graph using classes and objects
# and display it using an adjacency list.
```
class Node:
    def __init__(self, data):
        self.data = data


class Graph:
    def __init__(self):
        self.adjacency_list = {}

    def add_vertex(self, vertex):
        if vertex not in self.adjacency_list:
            self.adjacency_list[vertex] = []

    def add_edge(self, source, destination):
        self.add_vertex(source)
        self.add_vertex(destination)

        # Directed edge
        self.adjacency_list[source].append(destination)

    def display(self):
        print("Adjacency List:")
        for vertex in self.adjacency_list:
            print(vertex, "->", self.adjacency_list[vertex])


# Create graph
graph = Graph()

# Create nodes
vertices = ["A", "B", "C", "D", "E"]

for vertex in vertices:
    node = Node(vertex)
    graph.add_vertex(node.data)

# Add directed edges
graph.add_edge("A", "B")
graph.add_edge("A", "C")
graph.add_edge("B", "D")
graph.add_edge("C", "D")
graph.add_edge("D", "E")

# Display graph
graph.display()
```
<img width="1728" height="963" alt="image" src="https://github.com/user-attachments/assets/23c3aab7-3eba-4eba-a877-80eb1be4aa33" />

## Program 20: Graph Creation Using User Input
# Aim: To create a graph by taking vertices and edges from the user
# and display it using an adjacency list.
```
class Graph:
    def __init__(self, vertices):
        self.adjacency_list = {}

        for vertex in vertices:
            self.adjacency_list[vertex] = []

    def add_edge(self, vertex1, vertex2):
        self.adjacency_list[vertex1].append(vertex2)
        self.adjacency_list[vertex2].append(vertex1)

    def display(self):
        print("\nAdjacency List:")
        for vertex in self.adjacency_list:
            print(vertex, "->", self.adjacency_list[vertex])


# Take number of vertices
n = int(input("Enter number of vertices: "))

vertices = []

print("Enter the vertices:")

for i in range(n):
    vertex = input(f"Vertex {i + 1}: ")
    vertices.append(vertex)

# Create graph
graph = Graph(vertices)

# Take number of edges
e = int(input("Enter number of edges: "))

print("Enter the edges:")

for i in range(e):
    print(f"Edge {i + 1}:")
    vertex1 = input("Enter first vertex: ")
    vertex2 = input("Enter second vertex: ")

    if vertex1 in graph.adjacency_list and vertex2 in graph.adjacency_list:
        graph.add_edge(vertex1, vertex2)
    else:
        print("Invalid vertex!")

# Display graph
graph.display()
```
<img width="1658" height="920" alt="image" src="https://github.com/user-attachments/assets/9dd8b834-f957-4518-b1b6-a8584531ddd7" />

