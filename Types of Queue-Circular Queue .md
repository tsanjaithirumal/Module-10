# 🔄 Types of Queue-Circular Queue in Python

This project demonstrates the implementation of a **Circular Queue** in Python. The queue accepts 3 user values, performs enqueue and dequeue operations, and displays the removed values.

---

## 🎯 Aim

To develop a Python program that implements a Circular Queue:
- Accepts 3 values from the user
- Removes the 3 values from the queue
- Displays the removed values

---

## 🧠 Algorithm

1. **Initialize** a circular queue of fixed size (e.g., 5).
2. **Define the following functions**:
   - `enqueue()`: Inserts an element into the queue.
   - `dequeue()`: Removes an element from the queue.
   - `display()`: Shows the queue contents.
3. Accept 3 values from the user using the `enqueue()` method.
4. Remove 3 values using the `dequeue()` method.
5. Print the removed values.

---

## 💻 Program:
```
class CircularQueue:
    def __init__(self, size=5):
        self.size = size
        self.queue = [None] * size
        self.front = -1
        self.rear = -1
    
    def enqueue(self, value):
        if (self.rear + 1) % self.size == self.front:
            return False  
        
        if self.front == -1:  
            self.front = 0
        
        self.rear = (self.rear + 1) % self.size
        self.queue[self.rear] = value
        return True
    
    def dequeue(self):
        if self.front == -1:
            return None
        
        value = self.queue[self.front]
        self.queue[self.front] = None
        
        if self.front == self.rear:
            self.front = -1
            self.rear = -1
        else:
            self.front = (self.front + 1) % self.size
        
        return value
    
    def display(self):
        if self.front == -1:
            return []
        elements = []
        i = self.front
        while True:
            elements.append(self.queue[i])
            if i == self.rear:
                break
            i = (i + 1) % self.size
        return elements

cq = CircularQueue()

for _ in range(3):
    val = int(input())
    cq.enqueue(val)

removed = []
for _ in range(3):
    removed.append(cq.dequeue())

print(*removed)
```

### Output:
<img width="499" height="457" alt="446248445-0f087c24-97de-4ba3-bbcb-765204d73be3" src="https://github.com/user-attachments/assets/4dfbd57b-ff96-4018-914e-53f00e00bd68" />

## Result:
Thus, the program is verified successfully.
