# EX.NO.6 – AI-ASSISTED PROGRAMMING AND DEBUGGING

# **Name:** Bakkiyalakshmi E
# **Register Number:** 212223220012

## AIM

To develop programs using AI-assisted programming, identify and debug errors, optimize code, generate unit tests, and compare the outputs of multiple AI tools.

---

## AI TOOLS USED

* ChatGPT
* Google Gemini
* Microsoft Copilot

**Languages:** Python, C, Java

---

## 1. APPLICATION

### Student Management System

A simple Student Management System was selected.

### Functions

* Add Student
* Display Students
* Search Student by ID
* Exit

### Student Details

* Student ID
* Name
* Department
* Marks

---

## 2. PERSONA PROMPT

```text
Act as an experienced software developer and debugging expert.

Develop a simple Student Management System using Python.

The program should allow the user to:
1. Add student details
2. Display student details
3. Search for a student by ID
4. Exit

Student details include ID, Name, Department and Marks.

After generating the program:
- Identify possible bugs
- Debug the code
- Optimize the code
- Explain time and space complexity
- Generate unit test cases

Keep the code simple and readable.
```

---

## 3. PYTHON CODE GENERATED

```python
students = []

def add_student():
    student_id = int(input("Enter ID: "))
    name = input("Enter Name: ")
    department = input("Enter Department: ")
    marks = float(input("Enter Marks: "))

    students.append({
        "id": student_id,
        "name": name,
        "department": department,
        "marks": marks
    })

    print("Student added successfully.")


def display_students():
    for student in students:
        print(student)


def search_student():
    student_id = int(input("Enter ID to search: "))

    for student in students:
        if student["id"] == student_id:
            print(student)
            return

    print("Student not found.")


while True:
    print("\n1. Add Student")
    print("2. Display Students")
    print("3. Search Student")
    print("4. Exit")

    choice = int(input("Enter choice: "))

    if choice == 1:
        add_student()
    elif choice == 2:
        display_students()
    elif choice == 3:
        search_student()
    elif choice == 4:
        break
    else:
        print("Invalid choice.")
```

---

## 4. BUG IDENTIFICATION

The AI tools identified the following issues:

1. Invalid ID input can cause `ValueError`.
2. Invalid marks such as `150` are accepted.
3. Duplicate Student IDs are allowed.
4. Invalid menu input can terminate the program.
5. Searching an empty list needs proper handling.

---

## 5. DEBUGGING

The code was improved using:

```python
try:
    student_id = int(input("Enter ID: "))
except ValueError:
    print("Invalid ID")
```

Additional improvements:

* Added input validation.
* Checked marks between 0 and 100.
* Prevented duplicate Student IDs.
* Handled invalid menu choices.
* Added clear error messages.

---

## 6. OPTIMIZATION

The original program uses a list and linear search.

```text
Search Time Complexity = O(n)
Space Complexity = O(n)
```

For faster Student ID searching, a dictionary can be used:

```python
students = {}

students[101] = {
    "name": "Arun",
    "department": "IT",
    "marks": 85
}
```

Average dictionary lookup:

```text
O(1)
```

---

## 7. MULTIPLE AI TOOL COMPARISON

The **same prompt** was provided to ChatGPT, Gemini, and Copilot.

### ChatGPT

* Generated complete Python code.
* Identified input and logical errors.
* Suggested debugging and validation.
* Explained complexity.
* Generated unit tests.
* Provided detailed explanations.

### Google Gemini

* Generated a working Student Management System.
* Identified common input and logical errors.
* Suggested optimization techniques.
* Explained complexity.
* Generated test cases.
* Provided alternative approaches.

### Microsoft Copilot

* Generated a concise implementation.
* Identified major programming errors.
* Suggested debugging and validation.
* Explained linear search complexity.
* Generated basic test cases.

### Overall Observation

```text
ChatGPT  → Detailed explanation and debugging
Gemini   → Alternative approaches and optimization
Copilot  → Quick and concise coding assistance
```

All three AI tools successfully generated solutions and assisted with debugging and testing. However, the output from each tool was different in terms of **code structure, explanation, and level of detail**.

---

## 8. UNIT TEST CASES

### Test Case 1 – Valid Student

```text
Input: ID = 101, Marks = 85
Expected: Student added successfully
```

### Test Case 2 – Duplicate ID

```text
Input: ID = 101
Expected: Student ID already exists
```

### Test Case 3 – Invalid Marks

```text
Input: Marks = 150
Expected: Invalid marks
```

### Test Case 4 – Student Search

```text
Input: Search ID = 101
Expected: Student details displayed
```

### Test Case 5 – Student Not Found

```text
Input: Search ID = 999
Expected: Student not found
```

---

## 9. MANUAL CODING VS AI-ASSISTED CODING

### Manual Coding

**Advantages:**

* Improves programming logic.
* Builds independent problem-solving skills.
* Gives better understanding of the code.

**Disadvantages:**

* Takes more time.
* Debugging and testing require more effort.

### AI-Assisted Coding

**Advantages:**

* Faster code generation.
* Helps identify bugs.
* Provides optimization suggestions.
* Generates test cases quickly.

**Disadvantages:**

* Generated code may contain errors.
* Code must be verified and tested.
* Overdependence on AI should be avoided.

---

## 10. WORKFLOW

```text
Problem Definition
       ↓
Common Prompt
       ↓
ChatGPT / Gemini / Copilot
       ↓
Code Generation
       ↓
Bug Identification
       ↓
Debugging
       ↓
Optimization
       ↓
Unit Testing
       ↓
Compare Outputs
       ↓
Final Verified Code
```

---

## CONCLUSION

The experiment demonstrated the use of **multiple AI tools for programming and debugging**. ChatGPT, Gemini, and Copilot were used with the same programming requirement, and their outputs were compared.

AI tools helped in **code generation, bug identification, debugging, optimization, complexity analysis, and unit-test generation**. The experiment also showed that AI-generated code must be verified and tested by the programmer.

---

## RESULT

The **AI-Assisted Programming and Debugging** experiment was successfully completed. Multiple AI tools were used and their programming, debugging, optimization, and testing capabilities were compared successfully.
