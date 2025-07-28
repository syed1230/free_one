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
