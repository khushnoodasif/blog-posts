# Using User Input and a Menu to Calculate Shape Volumes in Python

In this tutorial, we will learn how to find the volume of different shapes in Python using user input and a menu to select the shape. We will cover the following shapes:

1.  Cube
    
2.  Sphere
    
3.  Cylinder
    
4.  Cone
    

Before we begin, let's first import the necessary libraries. We will be using the `math` library to perform some calculations, so make sure to import it as well.

```python
import math
```

Next, we will create a menu for the user to select the shape they want to find the volume of. We will use a `while` loop and a `switch` statement to handle the different shape options.

```python
while True:
    print("Please select a shape:")
    print("1. Cube")
    print("2. Sphere")
    print("3. Cylinder")
    print("4. Cone")
    print("5. Quit")

    choice = int(input())

    if choice == 5:
        break

    if choice == 1:
        # Calculate the volume of a cube
        pass
    elif choice == 2:
        # Calculate the volume of a sphere
        pass
    elif choice == 3:
        # Calculate the volume of a cylinder
        pass
    elif choice == 4:
        # Calculate the volume of a cone
        pass
    else:
        print("Invalid choice. Please try again.")
```

Now let's define the functions to calculate the volume of each shape.

## **Cube**

To find the volume of a cube, we need to ask the user for the length of one side of the cube. We can then use the following formula to calculate the volume:

```python
volume = side^3
```

Here is the code to implement this in Python:

```python
def find_cube_volume():
    side = float(input("Enter the length of one side of the cube: "))
    volume = side**3
    print(f"The volume of the cube is {volume}.")
```

## **Sphere**

To find the volume of a sphere, we need to ask the user for the radius of the sphere. We can then use the following formula to calculate the volume:

```python
volume = (4/3) * pi * radius^3
```

Here is the code to implement this in Python:

```python
def find_sphere_volume():
    radius = float(input("Enter the radius of the sphere: "))
    volume = (4/3) * math.pi * radius**3
    print(f"The volume of the sphere is {volume}.")
```

## **Cylinder**

To find the volume of a cylinder, we need to ask the user for the radius of the base and the height of the cylinder. We can then use the following formula to calculate the volume:

```python
volume = pi * radius^2 * height
```

Here is the code to implement this in Python:

```python
def find_cylinder_volume():
    radius = float(input("Enter the radius of the base of the cylinder: "))
    height = float(input("Enter the height of the cylinder: "))
    volume = math.pi * radius**2 * height
    print(f"The volume of the cylinder is {volume}.")
```

## **Cone**

To find the volume of a cone, we need to ask the user for the radius of the base and the height of the cone. We can then use the following formula to calculate the volume:

```python
volume = (1/3) * pi * radius^2 * height
```

Here is the code to implement this in Python:

```python
def find_cone_volume():
    radius = float(input("Enter the radius of the base of the cone: "))
    height = float(input("Enter the height of the cone: "))
    volume = (1/3) * math.pi * radius**2 * height
    print(f"The volume of the cone is {volume}.")
```

Here is the complete code that includes all the functions within the `while` loop:

```python
import math

def find_cube_volume():
    side = float(input("Enter the length of one side of the cube: "))
    volume = side**3
    print(f"The volume of the cube is {volume}.")

def find_sphere_volume():
    radius = float(input("Enter the radius of the sphere: "))
    volume = (4/3) * math.pi * radius**3
    print(f"The volume of the sphere is {volume}.")

def find_cylinder_volume():
    radius = float(input("Enter the radius of the base of the cylinder: "))
    height = float(input("Enter the height of the cylinder: "))
    volume = math.pi * radius**2 * height
    print(f"The volume of the cylinder is {volume}.")

def find_cone_volume():
    radius = float(input("Enter the radius of the base of the cone: "))
    height = float(input("Enter the height of the cone: "))
    volume = (1/3) * math.pi * radius**2 * height
    print(f"The volume of the cone is {volume}.")

while True:
    print("Please select a shape:")
    print("1. Cube")
    print("2. Sphere")
    print("3. Cylinder")
    print("4. Cone")
    print("5. Quit")

    choice = int(input())

    if choice == 5:
        break

    if choice == 1:
        find_cube_volume()
    elif choice == 2:
        find_sphere_volume()
    elif choice == 3:
        find_cylinder_volume()
    elif choice == 4:
        find_cone_volume()
    else:
        print("Invalid choice. Please try again.")
```

This code will present the user with a menu to select a shape, and then ask for the necessary input to calculate the volume of the selected shape. The program will continue to loop until the user selects the option to quit.