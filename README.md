# Python OOP and Encapsulation Practice

## About the Project

This repository contains beginner-level Python examples demonstrating object-oriented programming (OOP), private attributes, private methods, and basic getter and setter methods.

The examples are implemented using Jupyter Notebook to make the code easy to read, execute, and understand.

## Objectives

- Understand classes and objects in Python.
- Learn how double underscores are used in attribute and method names.
- Understand Python name mangling.
- Practice accessing private methods through public methods.
- Learn how to update and retrieve an object's attribute value.

## Technologies Used

- **Programming language:** Python
- **Development environment:** Jupyter Notebook
- **File format:** IPython Notebook (`.ipynb`)

## Project Structure

```text
python-oop-encapsulation-practice/
├── README.md
└── python_oop_encapsulation.ipynb
```

## Concepts Demonstrated

### 1. Classes and Objects

A class is a blueprint for creating objects. An object is an instance of a class.

The notebook defines classes named `Student`, `India`, and `Encap`, then creates objects from those classes.

Example:

```python
class Student:
    __a = 100

    def show(self):
        self.__num()

    def __num(self):
        print(self.__a)

ob = Student()
ob.show()
```

This example demonstrates how an object calls a public method, which then calls a double-underscore method within the class.

### 2. Private Attributes and Methods

Python allows developers to use double underscores at the beginning of attribute and method names.

Examples from this notebook include:

- `__a`: a double-underscore attribute.
- `__num()`: a double-underscore method.
- `__add()`: another double-underscore method.

Python applies a mechanism called **name mangling** to many identifiers that begin with two underscores and do not end with two underscores. This helps avoid accidental name conflicts in subclasses.

Note: Python's double-underscore naming convention does not provide absolute privacy or security.

### 3. Getter and Setter Methods

The `Encap` class demonstrates how a method can update an attribute and another method can return its value.

```python
class Encap:
    __a = 100

    def set(self, b):
        self.__a = self.__a + b

    def get(self):
        return self.__a

ob = Encap()
ob.set(30)
print(ob.get())
```

**Expected output:**

```text
130
```

The `set()` method adds 30 to the initial value of 100. The `get()` method returns the updated value.

These are simple getter/setter-style methods for learning purposes.

## How to Run the Notebook

1. Clone or download this repository.
2. Open `python_oop_encapsulation.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
3. Run the cells in order.
4. Observe the outputs and modify the examples to practise the concepts.

Python must be installed locally if you want to run the notebook on your own computer. Alternatively, you can use Google Colab in a browser.

## Learning Outcomes

After completing these examples, a beginner should be able to:

- Define simple Python classes.
- Create objects and call their methods.
- Recognize double-underscore attributes and methods.
- Explain the basic purpose of name mangling.
- Use simple methods to update and retrieve an attribute value.

## Future Improvements

Possible extensions include:

- Add examples of inheritance and polymorphism.
- Compare single-underscore and double-underscore naming.
- Add input validation to setter methods.
- Improve naming conventions and code documentation.
- Add more examples of encapsulation using real-world scenarios.

## Author

**Veera Bhadra N**

This project is part of my Python programming practice and ongoing learning in scientific computing and bioinformatics.

## Disclaimer

This is an educational practice project. The examples are intended to demonstrate fundamental Python concepts and are not a complete implementation of secure data encapsulation.
