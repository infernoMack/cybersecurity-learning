# Day 04 — TryHackMe Pre Security

**Path:** TryHackMe Pre Security  
**Module:** Software Basics  
**Day:** 04  
**Rooms Completed:** Data Representation, Data Encoding, Python: Demo, JavaScript: Demo, SQL Basics

---

## 1. Data Representation

Today I learned how computers represent and process different types of data.

### What Is Data Representation?

Data representation is the way computers store and process information using binary digits (bits).

Computers operate using electronic circuits that represent information through two binary states, commonly represented as `0` and `1`.

### Important Concepts

**1. Bit**

A bit is the smallest unit of digital data. It can have a value of `0` or `1`.

**2. Byte**

A byte consists of 8 bits.

For example:

`01000001`

This is an 8-bit binary sequence.

**3. Binary Number System**

The binary number system uses only two digits:

- `0`
- `1`

Unlike the decimal system, which uses digits from 0 to 9, binary uses base 2.

Example:

Binary `1010` = Decimal `10`.

Calculation:

\(1 \times 2^3 + 0 \times 2^2 + 1 \times 2^1 + 0 \times 2^0 = 10\)

**4. Decimal Number System**

The decimal number system uses digits from 0 to 9 and has a base of 10.

**5. Hexadecimal Number System**

The hexadecimal system uses 16 symbols:

`0–9` and `A–F`

It is commonly used in computing because it provides a compact way to represent binary data.

Example:

- Binary: `11111111`
- Decimal: `255`
- Hexadecimal: `FF`

### Why Data Representation Matters in Cybersecurity

Understanding binary and hexadecimal helps me interpret:

- Raw data and file contents.
- Memory addresses and values.
- Network packets.
- Hexadecimal values used in security tools.
- Encoded data encountered during security investigations.

### Important Terms

- Bit
- Byte
- Binary
- Decimal
- Hexadecimal
- Base 2
- Base 10
- Base 16

---

## 2. Data Encoding

Today I learned how computers represent text and other information in formats that systems can store, process, and exchange.

### What Is Data Encoding?

Data encoding is the process of representing information using a defined format or set of rules so that it can be stored, processed, or transmitted.

Different types of data require different representation methods.

### Important Encoding Concepts

**1. Character Encoding**

Character encoding defines how text characters are represented as numeric values and bytes.

Common examples include:

- ASCII
- Unicode
- UTF-8

**2. ASCII**

ASCII is a character encoding standard that represents English letters, digits, punctuation, and control characters.

For example, uppercase `A` has the decimal ASCII value `65`, which is hexadecimal `41`.

**3. Unicode**

Unicode assigns code points to characters from many writing systems, along with symbols and emoji.

**4. UTF-8**

UTF-8 is a widely used Unicode encoding. It represents Unicode characters using one to four bytes per code point.

**5. Base64**

Base64 converts binary data into a text-based representation using a defined set of 64 characters.

It is commonly used when binary data needs to be carried through systems designed to handle text.

Important: **Base64 is encoding, not encryption.** It does not protect sensitive information from someone who can decode it.

### Encoding vs Encryption vs Hashing

| Concept | Purpose | Reversible? |
|---|---|---|
| Encoding | Represent data in a different format | Generally yes |
| Encryption | Protect confidentiality using cryptographic keys | With the appropriate key or method |
| Hashing | Produce a fixed-length digest from input data | Designed to be one-way |

### Why Data Encoding Matters in Cybersecurity

Encoding knowledge helps me understand:

- How text is represented in files and network traffic.
- Why different systems may interpret data differently.
- How encoded values appear in web requests.
- How analysts inspect suspicious data.
- Why encoding should not be mistaken for security.

### Important Terms

- Character Encoding
- ASCII
- Unicode
- UTF-8
- Base64
- Encryption
- Hashing

---

## 3. Python: Demo

Today I was introduced to Python, a programming language widely used in automation, scripting, and cybersecurity.

### What Is Python?

Python is a high-level programming language known for its readable syntax and broad range of applications.

It can be used to automate repetitive tasks, process files, analyze data, and interact with systems and security tools.

### Basic Python Syntax

**1. Printing Output**

The `print()` function displays output.

```python
print("Hello, World!")
```

Output:

```text
Hello, World!
```

**2. Variables**

Variables store references to values that can be used in a program.

```python
name = "Cybersecurity"
age = 25

print(name)
print(age)
```

**3. Common Data Types**

```python
username = "analyst"  # String
age = 25              # Integer
price = 10.5          # Float
is_active = True      # Boolean
```

- `str`: Text
- `int`: Whole numbers
- `float`: Numbers with a fractional part
- `bool`: `True` or `False`

**4. Conditional Statements**

Conditional statements allow a program to make decisions.

```python
status_code = 200

if status_code == 200:
    print("Request successful")
else:
    print("Request unsuccessful")
```

**5. Loops**

Loops repeat a block of code.

```python
for number in range(1, 4):
    print(number)
```

Output:

```text
1
2
3
```

### Python in Cybersecurity

Python can help me:

- Automate repetitive tasks.
- Parse log files.
- Process text and data.
- Make HTTP requests in authorized testing environments.
- Build small utilities for security analysis.

### Important Terms

- Python
- Variable
- Data Type
- Function
- Conditional
- Loop
- Script
- Automation

---

## 4. JavaScript: Demo

Today I was introduced to JavaScript and its role in making websites interactive.

### What Is JavaScript?

JavaScript is a programming language commonly used to add behavior and interactivity to websites.

It can run in web browsers and, through environments such as Node.js, outside the browser as well.

### Where JavaScript Is Used

- Interactive website elements.
- Form validation.
- Dynamic page updates.
- Web applications.
- Server-side applications using Node.js.

### Basic JavaScript Syntax

**1. Printing Output**

```javascript
console.log("Hello, World!");
```

**2. Variables**

```javascript
let username = "analyst";
const language = "JavaScript";

console.log(username);
console.log(language);
```

- `let` declares a variable that can be reassigned.
- `const` declares a binding that cannot be reassigned.

**3. Conditional Statements**

```javascript
let statusCode = 200;

if (statusCode === 200) {
    console.log("Request successful");
} else {
    console.log("Request unsuccessful");
}
```

**4. Functions**

Functions are reusable blocks of code.

```javascript
function greet(name) {
    return "Hello, " + name;
}

console.log(greet("Analyst"));
```

### JavaScript and Web Security

JavaScript is important in web security because it runs in browser contexts and can interact with web page content.

Security concepts associated with JavaScript include:

- Cross-Site Scripting (XSS).
- Secure handling of user input.
- Browser security boundaries.
- Client-side versus server-side validation.
- Protecting sensitive data from exposure in browser code.

Client-side validation improves usability, but important security checks must also be enforced on the server.

### Important Terms

- JavaScript
- Variable
- Function
- Conditional
- Browser
- Node.js
- Client-Side
- Server-Side
- Cross-Site Scripting (XSS)

---

## 5. SQL Basics

Today I learned the fundamentals of SQL and how it is used to communicate with relational databases.

### What Is SQL?

SQL stands for Structured Query Language.

It is used to retrieve, insert, update, and delete data in relational database systems.

### What Is a Database?

A database is an organized collection of data.

A relational database stores data in tables containing rows and columns.

For example, a `users` table might contain:

| id | username | role |
|---:|---|---|
| 1 | rahul | user |
| 2 | priya | admin |
| 3 | amit | user |

- **Table:** Organizes related data.
- **Row:** Represents one record.
- **Column:** Represents an attribute.
- **Primary key:** Uniquely identifies a row in a table.

### Important SQL Commands

**1. SELECT — Retrieve Data**

```sql
SELECT * FROM users;
```

Retrieves all columns from the `users` table.

**2. WHERE — Filter Data**

```sql
SELECT * FROM users
WHERE username = 'rahul';
```

Retrieves rows matching the specified condition.

**3. INSERT — Add Data**

```sql
INSERT INTO users (id, username, role)
VALUES (4, 'neha', 'user');
```

Adds a new row, assuming the values satisfy the table's constraints.

**4. UPDATE — Modify Data**

```sql
UPDATE users
SET role = 'admin'
WHERE id = 3;
```

Changes the role for the row with ID `3`.

**5. DELETE — Remove Data**

```sql
DELETE FROM users
WHERE id = 4;
```

Deletes the matching row.

Always verify the condition before executing an `UPDATE` or `DELETE`. Without a `WHERE` clause, these operations may affect every row in the table.

### SQL and Cybersecurity

SQL is important in cybersecurity because web applications frequently use databases to store account details, application records, and other information.

A major security risk is **SQL Injection (SQLi)**.

SQL injection can occur when an application unsafely incorporates untrusted input into a SQL query, allowing the input to alter the intended query.

### How to Prevent SQL Injection

- Use parameterized queries or prepared statements.
- Avoid building SQL queries by concatenating untrusted input.
- Apply least-privilege permissions to database accounts.
- Validate input according to the application's requirements.
- Avoid exposing detailed database errors to users.

Input validation is useful, but it does not replace parameterized queries.

### Important Terms

- SQL
- Database
- Table
- Row
- Column
- Primary Key
- SELECT
- INSERT
- UPDATE
- DELETE
- WHERE
- SQL Injection
- Parameterized Query

---

## 6. What I Learned Today

Today I completed five rooms in the Software Basics module:

1. **Data Representation:** How computers represent information using bits, bytes, binary, decimal, and hexadecimal.
2. **Data Encoding:** How information is represented using standards such as ASCII, Unicode, UTF-8, and Base64.
3. **Python: Demo:** The basics of Python syntax, variables, conditions, and loops.
4. **JavaScript: Demo:** The basics of JavaScript and its role in web applications.
5. **SQL Basics:** How relational databases store information and how SQL retrieves and modifies data.

These topics provide a foundation for understanding programming, web technologies, databases, and common cybersecurity vulnerabilities.

---

## 7. Things I Need to Revise

- [ ] Bit vs Byte
- [ ] Binary vs Decimal vs Hexadecimal
- [ ] ASCII vs Unicode vs UTF-8
- [ ] Encoding vs Encryption vs Hashing
- [ ] Python variables and data types
- [ ] Python conditionals and loops
- [ ] JavaScript variables and functions
- [ ] Client-side vs Server-side code
- [ ] SQL SELECT and WHERE
- [ ] SQL INSERT, UPDATE, and DELETE
- [ ] SQL Injection and parameterized queries

---

## 8. Self-Assessment

1. How many bits are there in one byte?
2. What is the hexadecimal representation of decimal `255`?
3. How is encoding different from encryption?
4. What is the purpose of UTF-8?
5. What is the difference between a Python variable and a function?
6. What is the difference between `let` and `const` in JavaScript?
7. What are rows and columns in a relational database?
8. What does the SQL `WHERE` clause do?
9. Why can SQL injection occur?
10. How do parameterized queries help prevent SQL injection?

---

## TryHackMe Progress

**Pre Security — Software Basics**

- [x] Data Representation
- [x] Data Encoding
- [x] Python: Demo
- [x] JavaScript: Demo
- [x] SQL Basics

**Day 04 Status: Completed ✅**
