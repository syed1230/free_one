DSA code reporisitary 
<!--Queues_linkedlist-->
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class QueueLinkedList:
    def __init__(self):
        self.front = None
        self.rear = None
    def enqueue(self, data):
        new_node = Node(data)
        if self.rear is None:
            self.front = self.rear = new_node
            return
        self.rear.next = new_node
        self.rear = new_node
    def dequeue(self):
        if self.front is None:
            print("Queue Underflow")
            return None
        dequeued_data = self.front.data
        self.front = self.front.next
        if self.front is None:
            self.rear = None
        return dequeued_data
    def display(self):
        temp = self.front
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")
q = QueueLinkedList()
q.enqueue(10)
q.enqueue(20)
q.enqueue(10)
q.enqueue(20)
q.display()      # 10 -> 20 -> None
print(q.dequeue())  # 10
q.display()      # 20 -> None
<!--stack_circulararray-->
class StackCircularArray:
    def __init__(self, size):
        self.size = size
        self.stack = [None] * size
        self.top = -1
    def is_full(self):
        return (self.top + 1) % self.size == 0 and self.stack[self.top] is not None
    def is_empty(self):
        return self.top == -1
    def push(self, data):
        if self.is_full():
            print("Stack Overflow")
            return
        self.top = (self.top + 1) % self.size
        self.stack[self.top] = data
    def pop(self):
        if self.is_empty():
            print("Stack Underflow")
            return None
        popped_data = self.stack[self.top]
        self.stack[self.top] = None
        self.top = self.top - 1 if self.top != 0 else self.size - 1
        return popped_data
    def display(self):
        print("Stack:", self.stack)
stack = StackCircularArray(5)
stack = StackCircularArray(6)  # smaller size for quick testing
#pushing the 1 in to the array
print("Pushing 1")
stack.push(1)
stack.display()
#oshing the 2 into the aray
print("Pushing 2")
stack.push(2)
stack.display()
#oushing the 34 into the array
print("Pushing 34")
stack.push(34)
stack.display()
#the array is o fthe limit 3 but here trying to push the 99 into the rray which shopws the overflow
print("\n\nTrying to push 99 (should cause overflow)")
stack.push(99)  # This should print "Stack Overflow"
stack.display()
#noe poping the elemnts in the aray
print("\n\nPopping:", stack.pop())
stack.display()
#popoing
print("Popping:", stack.pop())
stack.display()
#poping
print("Popping:", stack.pop())
stack.display()
#completly removed the elemnts noe trying to take elemen in the null array
print("\n\nTrying to pop from empty stack (should cause underflow)")
print("Popped:", stack.pop())  # Should print "Stack Underflow"
stack.display()
#trring to insert 100 after removbing and also after the completetion of the check function 
print("\n\nPushing 100 after underflow")
stack.push(100)
stack.display()
<!-- stack _linkled list-->
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class StackLinkedList:
    def __init__(self):
        self.top = None
    def push(self, data):
        new_node = Node(data)
        new_node.next = self.top
        self.top = new_node
    def pop(self):
        if self.top is None:
            print("Stack Underflow")
            return None
        popped_data = self.top.data
        self.top = self.top.next
        return popped_data
    def display(self):
        temp = self.top
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")
#implementation here using the function call 
stack = StackLinkedList()
stack.push(123)
stack.push(45)
stack.push(23)
stack.display()  # 20 -> 10 -> None
print(stack.pop())  # 20
stack.display()     # 10 -> None

print("Popping element:", stack.pop())
stack.display()

print("Popping element:", stack.pop())
stack.display()

print("Popping element:", stack.pop())
stack.display()
print("------------------------------------------------------\n---------------------------------------------------")
print("Trying to pop from empty stack (should show underflow):")
print("Popped:", stack.pop())  # Underflow case

print("Pushing 99 after underflow")
stack.push(99)
stack.display()
<!--simple stack program-->
# Python program to
# demonstrate stack implementation
# using list
stack = []
# append() function to push
# element in the stack
stack.append('a')
stack.append('b')
stack.append('c')

print('Initial stack')
print(stack)

# pop() function to pop
# element from stack in
# LIFO order
print('\nElements popped from stack:')
print(stack.pop())
print(stack.pop())
print(stack.pop())

print('\nStack after elements are popped:')
print(stack)

<!--enques_and _dequesua-->
class ArrayQueue:
    def __init__(self, capacity):
        self.queue = [None] * capacity  # fixed size array
        self.front = 0
        self.rear = -1
        self.size = 0
        self.capacity = capacity
    def is_empty(self):
        return self.size == 0
    def is_full(self):
        return self.size == self.capacity
    def enqueue(self, item):
        if self.is_full():
            print("Queue is full! Cannot enqueue", item)
            return
        self.rear = (self.rear + 1) % self.capacity
        self.queue[self.rear] = item
        self.size += 1
        print(f"Enqueued: {item}")
    def dequeue(self):
        if self.is_empty():
            print("Queue is empty! Cannot dequeue")
            return None
        item = self.queue[self.front]
        self.queue[self.front] = None  # Optional: clear the slot
        self.front = (self.front + 1) % self.capacity
        self.size -= 1
        print(f"Dequeued: {item}")
        return item
    def display(self):
        if self.is_empty():
            print("Queue is empty")
            return
        print("Queue elements:", end=" ")
        for i in range(self.size):
            print(self.queue[(self.front + i) % self.capacity], end=" ")
        print()


# Example usage:
q = ArrayQueue(5)

q.enqueue(10)
q.enqueue(20)
q.enqueue(30)
q.display()

q.dequeue()
q.display()

q.enqueue(40)
q.enqueue(50)
q.enqueue(60)  # should be full now
q.display()

q.enqueue(70)  # should print full message

q.dequeue()
q.dequeue()
q.display()

<!--enqueing-->
class CircularQueue:
    def __init__(self, size):
        # Initialize the queue with a fixed size
        self.size = size
        # Create a list to store queue elements, initially all None
        self.queue = [None] * size
        # front points to the index of the first element
        self.front = -1
        # rear points to the index of the last element
        self.rear = -1
    def is_full(self):
        # Queue is full if next position of rear is front
        return (self.rear + 1) % self.size == self.front
    def is_empty(self):
        # Queue is empty if front is -1
        return self.front == -1
    def enqueue(self, data):
        # Add an element to the rear of the queue
        if self.is_full():
            # If the queue is full, we cannot add new element
            print("Queue is full! Cannot enqueue", data)
            return
               if self.is_empty():
            # If queue is empty, reset front and rear to 0
            self.front = 0
            self.rear = 0
            self.queue[self.rear] = data  # Insert data at rear
        else:
            # Move rear forward circularly
            self.rear = (self.rear + 1) % self.size
            self.queue[self.rear] = data  # Insert data at new rear
                print(f"Enqueued: {data}")
    def dequeue(self):
        # Remove an element from the front of the queue
        if self.is_empty():
            # Cannot dequeue if queue is empty
            print("Queue is empty! Cannot dequeue")
            return None
               data = self.queue[self.front]  # Get the front element to return
                if self.front == self.rear:
            # If only one element was present, queue becomes empty after removal
            self.front = -1
            self.rear = -1
        else:
            # Move front forward circularly
            self.front = (self.front + 1) % self.size
                print(f"Dequeued: {data}")
        return data
    def display(self):
        # Display all elements in the queue from front to rear
        if self.is_empty():
            print("Queue is empty")
            return
                print("Queue elements:", end=" ")
        i = self.front
        while True:
            print(self.queue[i], end=" ")
            if i == self.rear:
                # Stop once we have printed the rear element
                break
            i = (i + 1) % self.size  # Move circularly to next element
        print()


# Testing the circular queue
cq = CircularQueue(5)  # Create a queue of size 5

# Enqueue 10, 20, 30
cq.enqueue(10)  # Inserts 10 at rear (index 0)
cq.enqueue(20)  # Inserts 20 at rear (index 1)
cq.enqueue(30)  # Inserts 30 at rear (index 2)
cq.display()    # Prints: 10 20 30

# Dequeue twice (should remove 10 and then 20)
cq.dequeue()    # Removes 10 from front (index 0), front moves to index 1
cq.dequeue()    # Removes 20 from front (index 1), front moves to index 2
cq.display()    # Prints: 30

# Enqueue 5 (goes to next rear position circularly)
cq.enqueue(5)   # Inserts 5 at rear (index 3)
cq.display()    # Prints: 30 5


<!--50 _integrs manipulation-->
import random
import time

# Insertion Sort implementation
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        # Move elements of arr[0..i-1], that are greater than key,
        # to one position ahead of their current position
        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key

# Merge Sort implementation
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2  # Finding the mid of the array
        left_half = arr[:mid]  # Dividing the array elements
        right_half = arr[mid:]  # into two halves
        merge_sort(left_half)  # Sorting the first half
        merge_sort(right_half)  # Sorting the second half
        i = j = k = 0
        # Copy data to temp arrays left_half[] and right_half[]
        while i < len(left_half) and j < len(right_half):
            if left_half[i] < right_half[j]:
                arr[k] = left_half[i]
                i += 1
            else:
                arr[k] = right_half[j]
                j += 1
            k += 1
        # Checking if any element was left
        while i < len(left_half):
            arr[k] = left_half[i]
            i += 1
           k += 1
       while j < len(right_half):
            arr[k] = right_half[j]
            j += 1
            k += 1

# Generate a random list of 50 integers between 1 and 100
random_list = [random.randint(1, 100) for _ in range(50)]
print("Original list:")
print(random_list)

# Copy lists for sorting (to keep the original list unchanged)
list_for_insertion = random_list.copy()
list_for_merge = random_list.copy()

# Time insertion sort
start_time = time.time()
insertion_sort(list_for_insertion)
end_time = time.time()
insertion_sort_time = end_time - start_time
print("\nSorted list by Insertion Sort:")
print(list_for_insertion)
print(f"Insertion Sort took {insertion_sort_time:.6f} seconds")

# Time merge sort
start_time = time.time()
merge_sort(list_for_merge)
end_time = time.time()
merge_sort_time = end_time - start_time
print("\nSorted list by Merge Sort:")
print(list_for_merge)
print(f"Merge Sort took {merge_sort_time:.6f} seconds")

# Compare performance
print("\nPerformance Comparison:")
if insertion_sort_time < merge_sort_time:
    print("Insertion Sort is faster.")
elif merge_sort_time < insertion_sort_time:
    print("Merge Sort is faster.")
else:
    print("Both algorithms took the same time.")
    <!--circular_queue_inserion and deletion-->
    class CircularQueue:
    def __init__(self, size):
        self.size = size                # Maximum size of the queue
        self.queue = [None] * size      # Initialize the queue with None
        self.front = -1                 # Front pointer
        self.rear = -1                  # Rear pointer
    def is_full(self):
        # Queue is full if next position of rear is front
        return (self.rear + 1) % self.size == self.front
   def is_empty(self):
        # Queue is empty if front is -1
        return self.front == -1
    def enqueue(self, data):
        if self.is_full():
            print("Queue is full! Cannot insert", data)
            return
        if self.is_empty():
            # If queue is empty, initialize front and rear to 0
            self.front = 0
            self.rear = 0
        else:
            # Move rear forward circularly
            self.rear = (self.rear + 1) % self.size    
        self.queue[self.rear] = data
        print(f"Inserted {data} into queue.")
    def dequeue(self):
        if self.is_empty():
            print("Queue is empty! Cannot delete element.")
            return None
               data = self.queue[self.front]
        if self.front == self.rear:
            # Queue has only one element, reset queue after deletion
            self.front = -1
            self.rear = -1
        else:
            # Move front forward circularly
            self.front = (self.front + 1) % self.size
                print(f"Deleted {data} from queue.")
        return data
    def display(self):
        if self.is_empty():
            print("Queue is empty.")
            return
        print("Queue elements:", end=" ")
        i = self.front
        while True:
            print(self.queue[i], end=" ")
            if i == self.rear:
                break
            i = (i + 1) % self.size
        print()


# Example usage
cq = CircularQueue(5)  # Queue of size 5

cq.enqueue(10)
cq.enqueue(20)
cq.enqueue(30)
cq.display()

cq.dequeue()
cq.dequeue()
cq.display()

cq.enqueue(40)
cq.enqueue(50)
cq.enqueue(60)
cq.display()

cq.enqueue(70)  # Should show queue is full

<!--binary tree in array and the linked list-->
class ArrayBinaryTree:
    def __init__(self, capacity):
        # Initialize the tree with a fixed capacity and fill it with None
        self.tree = [None] * capacity
        self.capacity = capacity
    def set_root(self, data):
        # Set the root node at index 0 if it's currently empty
        if self.tree[0] is None:
            self.tree[0] = data
        else:
            print("Root already exists.")
    def set_left_child(self, parent_index, data):
        # Calculate the left child index based on the parent index
        left_child_index = 2 * parent_index + 1
        # Check if the parent exists and is within bounds
        if 0 <= parent_index < self.capacity and self.tree[parent_index] is not None:
            # Ensure the left child index is within the array bounds
            if 0 <= left_child_index < self.capacity:
                self.tree[left_child_index] = data
            else:
                print("Left child index out of bounds.")
        else:
           print(f"Parent at index {parent_index} does not exist or is out of bounds.")
    def set_right_child(self, parent_index, data):
        # Calculate the right child index based on the parent index
        right_child_index = 2 * parent_index + 2
        # Check if the parent exists and is within bounds
        if 0 <= parent_index < self.capacity and self.tree[parent_index] is not None:
            # Ensure the right child index is within the array bounds
            if 0 <= right_child_index < self.capacity:
                self.tree[right_child_index] = data
            else:
                print("Right child index out of bounds.")
        else:
            print(f"Parent at index {parent_index} does not exist or is out of bounds.")
    def get_node(self, index):
        # Return the value at the given index if it's within bounds
        if 0 <= index < self.capacity:
            return self.tree[index]
        return None  # Return None if index is invalid
    def print_tree(self):
        # Print the tree with index and value in a user-friendly format
        print("Array Representation:")
        for i, node in enumerate(self.tree):
            if node is not None:
                print(f"Index {i}: {node}", end=" | ")
            else:
                print(f"Index {i}: None", end=" | ")
        print("\n")

    <!--******* linked list implementation-->
    # Node class represents each individual element (node) of the binary tree
class Node:
    def __init__(self, data):
        self.data = data      # The value/data stored in the node
        self.left = None      # Pointer to the left child
        self.right = None     # Pointer to the right child

# Binary tree implementation using linked list (nodes and pointers)
class LinkedListBinaryTree:
    def __init__(self):
        self.root = None  # Initially, the tree is empty (no root)
    def insert(self, data):
        # Insert a new node into the tree
        if self.root is None:
            # If the tree is empty, set the new node as root
            self.root = Node(data)
        else:
            # Otherwise, use level-order (BFS) insertion
            self._insert_recursive(self.root, data)
    def _insert_recursive(self, current_node, data):
        # This function performs level-order insertion (breadth-first)
        # It ensures that nodes are filled from top to bottom, left to right
        from collections import deque  # Import deque for queue functionality
        queue = deque([current_node])  # Initialize queue with the root node
        while queue:
            node = queue.popleft()  # Get the front node from the queue
            # Check if the left child is empty
            if node.left is None:
                node.left = Node(data)  # Insert as left child
                return
            else:
                queue.append(node.left)  # If not, add to queue to check its children
            # Check if the right child is empty
            if node.right is None:
                node.right = Node(data)  # Insert as right child
                return
            else:
                queue.append(node.right)  # If not, add to queue to check its children
    def inorder_traversal(self, node):
        # Inorder traversal: left subtree → root → right subtree
        if node:
            self.inorder_traversal(node.left)
            print(node.data, end=" ")  # Print node data
            self.inorder_traversal(node.right)
    def print_tree(self):
        # Helper function to print the tree using inorder traversal
        print("Linked List Representation (Inorder Traversal):")
        self.inorder_traversal(self.root)
        print("\n")  # Newline after traversal output
# Array Implementation
array_tree = ArrayBinaryTree(10)
array_tree.set_root('A')
array_tree.set_left_child(0, 'B')
array_tree.set_right_child(0, 'C')
array_tree.set_left_child(1, 'D')
array_tree.set_right_child(1, 'E')
array_tree.print_tree()

# Linked List Implementation
linked_list_tree = LinkedListBinaryTree()
linked_list_tree.insert('A')
linked_list_tree.insert('B')
linked_list_tree.insert('C')
linked_list_tree.insert('D')
linked_list_tree.insert('E')
linked_list_tree.print_tree()
