# C++ Programs using Constructors, Copy Constructors & Destructors

This repository contains several **Object-Oriented Programming (OOP)** examples in **C++**, demonstrating the concepts of:

* **Default constructors**
* **Parameterized constructors**
* **Copy constructors**
* **Destructors**
* **Class and object implementation**

---

## Theory

In **C++**, classes and objects are the foundation of Object-Oriented Programming.

* **Constructor**: A special member function that is automatically invoked when an object is created. It is used to initialize data members.

  * **Default Constructor** → No arguments, initializes objects with default values.
  * **Parameterized Constructor** → Takes arguments to initialize objects with specific values.
  * **Copy Constructor** → Initializes a new object as a copy of an existing object.

* **Destructor**: A special member function invoked automatically when an object goes out of scope or is explicitly deleted. It is used to free resources.

---

## Algorithm (General Steps)

1. Define a **class** with data members (attributes like `name`, `age`, `price`, etc.).
2. Implement **constructors** to initialize objects:

   * Default constructor → takes no arguments.
   * Parameterized constructor → initializes with given arguments.
   * Copy constructor → copies values from another object.
3. Implement a **display() function** to show object details.
4. In `main()`, create objects of the class.
5. Observe constructor calls, copy constructor calls, and destructor calls when objects go out of scope.

---

## Programs Included

### 1. Book Class with Copy Constructor

* Demonstrates **parameterized constructor** and **copy constructor**.

```cpp
Book s("Manga", "Mangaka", 200);
Book copyS(s);
```

**Algorithm**:

1. Create a book object with name, author, and price.
2. Use copy constructor to create another object.
3. Display both objects.

---

### 2. Student Class with Copy Constructor

* Shows **copy constructor usage** in a student class.

```cpp
student s("Prateek", 20);
student copyS(s);
```

**Algorithm**:

1. Initialize student using parameterized constructor.
2. Copy student object using copy constructor.
3. Display student details.

---

### 3. Car Class with Default Constructor & User Input

* Demonstrates **default constructor** with **input from user**.

```cpp
Car sedan;
sedan.display();
```

**Algorithm**:

1. Constructor asks user to enter price, car name, and mileage.
2. Display function prints entered details.

---

### 4. Student Class with Default Constructor & Input

* Shows **default constructor** initializing attributes via user input.

```cpp
student s1;
s1.display();
```

**Algorithm**:

1. Default constructor asks for `name`, `roll number`, and `grade`.
2. Display function prints values.

---

### 5. Date Class with Parameterized Constructor

* Simple example with **parameterized constructor**.

```cpp
Date d1(28, 8, 2025);
d1.showDate();
```

**Algorithm**:

1. Constructor initializes `day`, `month`, and `year`.
2. Display function prints date in DD/MM/YY format.

---

### 6. Destructor Example with Object Count

* Demonstrates how **destructors are invoked automatically**.

```cpp
destruct d1, d2, d3;
{
    destruct d4;  // destroyed at end of block
}
```

**Algorithm**:

1. Every time an object is created, increment count.
2. When an object is destroyed, decrement count.
3. Destructor messages show destruction order.

---

### 7. Destructor Call in Loop

* Shows **multiple destructor calls** when temporary objects are created in a loop.

```cpp
for(int i=0; i<4; i++) {
    date temp;  // destroyed after each iteration
}
```

**Algorithm**:

1. Create 4 objects initially.
2. Inside loop, create temporary objects.
3. Destructor called each time object goes out of scope.

---

## Example Outputs

* **Book Example:**

```
Book Name: Manga
Author Name: Mangaka
Price: 200
copy constructor called!!
Book Name: Manga
Author Name: Mangaka
Price: 200
```

* **Car Example:**

```
Enter the price : 1200000
Enter the Car Name : toyota
Enter the mileage : 23
Car Details are :
1200000
toyota
23
```

* **Destructor Example:**

```
Number of objects created: 1
Number of objects created: 2
Number of objects created: 3
Number of objects created: 4
Number of objects destroyed: 3
Number of objects destroyed: 2
Number of objects destroyed: 1
Number of objects destroyed: 0
```

---

## Conclusion

* Constructors simplify object initialization.
* Copy constructors help in object duplication.
* Destructors manage memory and resources.
* C++ automatically calls constructors and destructors at object creation and destruction.
