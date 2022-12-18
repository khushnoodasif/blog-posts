# Stack Implementation Using List In Python

A stack is a linear data structure that follows a particular order in which the operations are performed. The order may be LIFO (Last In First Out) or FILO (First In Last Out).

In this tutorial, we will be implementing a stack that follows the LIFO order using Python's list data structure.

Let's start by defining a function `isempty()` which checks whether the stack is empty or not.

```python
def isempty(stk):          # checks whether the stack is empty or not
   if stk==[]:
      return True
   else:
      return False
```

The `isempty()` function takes in a stack as an argument and checks if it is equal to an empty list. If it is, it returns `True`, else it returns `False`.

Next, let's define a function `push()` which allows additions to the stack.

```python
def push(stk,item):        # Allow additions to the stack
   stk.append(item)
   top=len(stk)-1
```

The `push()` function takes in a stack and an item as arguments. It adds the item to the stack using the `append()` method and updates the value of the `top` variable to the index of the item added.

Now, let's define a function `popu()` which allows deletions from the stack.

```python

def popu(stk):
   if isempty(stk):        # verifies whether the stack is empty or not
      print("Stack Underflow")
   else:    # Allow deletions from the stack
      item=stk.pop()
      if len(stk)==0:
         top=-1
      else:
         top=len(stk)
      return item
```

The `popu()` function first checks if the stack is empty using the `isempty()` function we defined earlier. If it is empty, it prints "Stack Underflow". If not, it removes the top element from the stack using the `pop()` method and updates the value of `top` accordingly.

Next, let's define a function `display()` which displays the elements in the stack.

```python
def display(stk):
   if isempty(stk):
      print("Stack is empty")
   else:
      top=len(stk)-1
      print("Elements in the stack are: ")
      for i in range(top,-1,-1):
         print (stk[i])
```

The `display()` function first checks if the stack is empty using the `isempty()` function. If it is, it prints "Stack is empty". If not, it traverses the stack from the top to the bottom and prints the elements.

Now, let's define the main driver code that allows us to perform various stack operations.

```python
#------------------Driver code-------------------------
stk=[]     # Emptry list as empty stack
top=-1
while True:
    print("Enter your choice:\n1.PUSH\n2.POP\n3.Display\n4.Exit")
    ch=int(input())  # <-user coice
    if ch==1:   #PUSH in stack
        k=input("Enter element to insert: ")
        push(stk,k)
```

Here, we are prompting the user to enter an element to insert into the stack and then calling the `push()` function with the stack and the element as arguments.

Next, let's handle the case where the user wants to remove an element from the stack.

```python
elif ch==2:  #POP in stack
    k=popu(stk)
    print(k," is popped")
```

Here, we are calling the `popu()` function with the stack as an argument and storing the returned value in the variable `k`. We then print the value of `k` along with the message " is popped".

Now, let's handle the case where the user wants to display the elements in the stack.

```python
elif ch==3:   # Display Stack
    display(stk)
```

Here, we are simply calling the `display()` function with the stack as an argument.

Finally, let's handle the case where the user wants to exit the loop.

```python
elif ch==4:   #Exiting from loop
    break
```

Here, we are simply breaking out of the loop.

And that's it! We have successfully implemented a stack in Python.

I hope this tutorial was helpful in understanding the concepts of stack and how to implement it in Python. If you have any questions, feel free to ask.