# Python Programming Portfolio
**Felix Boyne:**
**Bishop's Stortford College:**
**Python for STEM:** 
**Year 12:**

---

## About me

Hi, I am a year 12 student at BSC who has been doing python programming for 1 year. I study Design and Technology, Geography and Economics. I am also looking to go to university at Loughborough, Sheffield and Leeds after school to study something based around Geography and Economics because I find it interesting.

---

## Course Overview

This portfolio documents my progress through a Python programming course designed for students preparing for STEM pathways at university. The course covers:

- Python fundamentals (variables, input/output, data types)
- Control structures (loops and conditionals)
- Functions and modular code
- Data structures (lists, dictionaries, tuples, sets)
- Validation and error handling
- File handling
- Object-Oriented Programming (OOP)
- Version control with Git and GitHub
- Working with Jupyter Notebooks

--- 

## Portfolio Projects

| # | Project | Key Skills | Status |
|---|---|---|---|
| 1 | [Unit Converter](#) | Variables, functions, input/output | ✅ Complete |
| 2 | [Number Guessing Game](#) | Loops, conditionals, random | ✅Complete |
| 3 | [To-Do List](#) | List, functions, data structures | ✅complete |
| 4 | [Student Grade Calculator](#) | Dictionaries, validation, error handling | ✅ Complete |
| 5 | [OOP Bank Account](#) | Classes, OOP principles | ✅ Complete |
| 6 | [Data Analysis Notebook](#) | Jupyter Notebooks, data exploration | ✅ Complete |

---

## Skills I Have Developed 

**Programming Concepts**
- Writing clean, well-commented Python code
- Using functions to organise and reuse code
- Handling user input safely with validation

**Tools and Technologies**
- Python 3 (Thonny IDE)
- Jupyter Notebooks
- Git version control
- GitHub for code sharing and portfolio management
- Markdown for documentation

---

## Contact

- **GitHub:** felixthegit123
- **Email:** 26boynef@bscmail.org

## Unit converter
```python
def km_to_miles(km):
    """Convert kilometres to miles."""
    miles = km * 0.621371
    return miles

def miles_to_km(miles):
    """Convert miles to kilometres."""
    km = miles / 0.621371
    return km

def c_to_f(c):
    """Convert Celsius to Fahrenheit."""
    f = (c * 9/5) + 32
    return f

def f_to_c(f):
    """Convert Fahrenheit to Celsius."""
    c = (f - 32) * 5/9
    return c

def show_menu():
    print("=== Unit Converter ===")
    print("1. Kilometres to Miles")
    print("2. Miles to Kilometres")
    print("3. Celsius to Fahrenheit")
    print("4. Fahrenheit to Celsius")

def main():
    show_menu()
    choice = input("Enter your choice (1-4): ")

    if choice == "1":
        km = float(input("Enter kilometres: "))
        result = km_to_miles(km)
        print(f"{km} km = {result:.2f} miles")

    elif choice == "2":
        miles = float(input("Enter miles: "))
        result = miles_to_km(miles)
        print(f"{miles} miles = {result:.2f} km")

    elif choice == "3":
        c = float(input("Enter Celsius: "))
        result = c_to_f(c)
        print(f"{c}°C = {result:.2f}°F")

    elif choice == "4":
        f = float(input("Enter Fahrenheit: "))
        result = f_to_c(f)
        print(f"{f}°F = {result:.2f}°C")

    else:
        print("Invalid choice. Please enter a number from 1 to 4.")
main()
```