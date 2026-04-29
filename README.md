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
This is the first project I did which converts units. It can convert Kilometers to Miles as well as Celsius to Farehnheit and the other way round. It is very useful when travelling countries if the road signs or temperature reading are in a different measurement.
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
This image shows the result of the code.
<img width="156" height="78" alt="{3A142E52-17AE-4E0A-A2EE-118503C571A8}" src="https://github.com/user-attachments/assets/5a8083e5-1ea9-4917-969f-fd209ffe91c3" />

## Number guessing game
This is a game where you can guess a random number between 1 and 100 which can be used to have some fun with you friends to see who guesses first.
```python 
import random

def play_game():
    """Play one round of the guessing game."""
    secret = random.randint(1, 100)
    attempts = 0
    
    print("I'm thinking of a number between 1 and 100.")
    
    while True:
        guess = int(input("Your guess: "))
        attempts += 1
        
        if guess < secret:
            print("Too low! Try again.")
        elif guess > secret:
            print("Too high! Try again.")
        else:
            print(f"Correct! You got it in {attempts} attempts.")
            break  # Exit the loop

play_game()
```
This is a picture from the result of the guessing game which took me 5 tries.
<img width="164" height="88" alt="{68B067E3-FA08-4542-A03D-6FAA10E7BABC}" src="https://github.com/user-attachments/assets/8034dfbc-7600-46b5-83c2-6a996af18fef" />

## To-do list manager
I created a to-do list because it was useful for me to remember what I have to do and it is very quick and easy to add and remove tasks to the list.
```python 
def show_tasks(tasks):
    """Display all tasks with their numbers."""
    if len(tasks) == 0:
        print("No tasks yet!")
        return
    
    print("\n=== Your Tasks ===")
    for i, task in enumerate(tasks, start=1):
        print(f"{i}. {task}")
    print()

def add_task(tasks):
    """Add a new task to the list."""
    new_task = input("Enter task: ")
    tasks.append(new_task)
    print(f"Added: '{new_task}'")

def remove_task(tasks):
    """Remove a task by number."""
    show_tasks(tasks)
    number = int(input("Enter task number to remove: "))
    if 1 <= number <= len(tasks):
        removed = tasks.pop(number - 1)
        print(f"Removed: '{removed}'")
    else:
        print("Invalid number.")

def main():
    tasks = []
    
    while True:
        print("=== To-Do List ===")
        print("1. View tasks")
        print("2. Add task")
        print("3. Remove task")
        print("4. Quit")
        
        choice = input("Choose: ")
        
        if choice == "1":
            show_tasks(tasks)
        elif choice == "2":
            add_task(tasks)
        elif choice == "3":
            remove_task(tasks)
        elif choice == "4":
            print("Goodbye!")
            break

main()
```
This is an example of me noting down my maths homework as a task and then recalling it to help me remember.
<img width="111" height="97" alt="{4B0DDB43-31BF-4DBF-9F04-C600A585F8DD}" src="https://github.com/user-attachments/assets/b9199a68-b9d9-4fc7-963d-4a41cb5d4f5e" />

## Grade calculator
This is a grade calculator which let me put all of my results into the system which then gave me my average grade so I can see what I am working to across multiple subjects.
def get_grade(average):
    """Return a letter grade based on average percentage."""
    if average >= 70:
        return "A"
    elif average >= 60:
        return "B"
    elif average >= 50:
        return "C"
    elif average >= 40:
        return "D"
    else:
        return "U"

def get_valid_score(subject):
    """Ask for a score and keep asking until a valid number is entered."""
    while True:
        try:
            score = float(input(f"Enter score for {subject} (0-100): "))
            if 0 <= score <= 100:
                return score
            else:
                print("Score must be between 0 and 100.")
        except ValueError:
            print("Please enter a number.")

def calculate_results():
     """Collect scores and display results."""
     name = input("Student name: ")
     subjects = ["Maths", "English", "Science"]
     scores = {}
    
     for subject in subjects:
        scores[subject] = get_valid_score(subject)
    
     average = sum(scores.values()) / len(scores)
     grade = get_grade(average)
    
     print(f"\n=== Results for {name} ===")
     for subject, score in scores.items():
        print(f"  {subject}: {score:.1f}")
     print(f"Average: {average:.1f}%")
     print(f"Grade: {grade}")

calculate_results()
Here is an example of me putting 3 grades in which are all different and the system giving me a B grade overall.
<img width="137" height="85" alt="{447BA7F4-B2FB-49F6-B742-B8F5435E8672}" src="https://github.com/user-attachments/assets/4a7678fa-2936-4494-84ff-a48299c61a01" />

