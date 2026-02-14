Got it — here’s a **super-small**, **paper-friendly**, **static** portal that still satisfies:

✅ HTML5 **semantic elements** (`header nav main section article footer`)
✅ **Bootstrap** used (CDN + basic classes)
✅ Pages: **Home**, **Books Catalogue**, **User Profile**

Just write these 3 minimal files.

---

## 1) `index.html` (Home)

```html
<!doctype html><html lang="en"><head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>BookStore</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head><body class="container">
<header class="py-3 border-bottom"><nav class="d-flex gap-3">
<a href="index.html" class="fw-bold text-decoration-none">BookStore</a>
<a href="catalogue.html">Catalogue</a><a href="profile.html">Profile</a>
</nav></header>

<main class="py-4">
<section class="p-3 bg-light rounded">
<h1 class="h4">Online Book Store</h1>
<p class="mb-2">Buy books, view catalogue, manage profile.</p>
<a class="btn btn-primary btn-sm" href="catalogue.html">Browse</a>
</section>
</main>

<footer class="py-3 border-top small text-muted">© 2026 BookStore</footer>
</body></html>
```

---

## 2) `catalogue.html` (Books Catalogue)

```html
<!doctype html><html lang="en"><head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Catalogue</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head><body class="container">
<header class="py-3 border-bottom"><nav class="d-flex gap-3">
<a href="index.html">Home</a><a href="catalogue.html" class="fw-bold">Catalogue</a><a href="profile.html">Profile</a>
</nav></header>

<main class="py-4">
<section>
<h1 class="h5 mb-3">Books Catalogue</h1>
<div class="row g-2">
<article class="col-6"><div class="card p-2"><b>Clean Code</b><small class="text-muted d-block">₹499</small></div></article>
<article class="col-6"><div class="card p-2"><b>The Alchemist</b><small class="text-muted d-block">₹299</small></div></article>
<article class="col-6"><div class="card p-2"><b>DBMS</b><small class="text-muted d-block">₹399</small></div></article>
<article class="col-6"><div class="card p-2"><b>Java Basics</b><small class="text-muted d-block">₹349</small></div></article>
</div>
</section>
</main>

<footer class="py-3 border-top small text-muted">© 2026 BookStore</footer>
</body></html>
```

---

## 3) `profile.html` (User Profile)

```html
<!doctype html><html lang="en"><head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Profile</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head><body class="container">
<header class="py-3 border-bottom"><nav class="d-flex gap-3">
<a href="index.html">Home</a><a href="catalogue.html">Catalogue</a><a href="profile.html" class="fw-bold">Profile</a>
</nav></header>

<main class="py-4">
<section class="card p-3">
<h1 class="h5">User Profile</h1>
<article class="small">
<b>Name:</b> Student<br><b>Email:</b> student@mail.com<br><b>Membership:</b> Basic
</article>
</section>
</main>

<footer class="py-3 border-top small text-muted">© 2026 BookStore</footer>
</body></html>
```

---
Here is a **small, clean, exam-friendly** Inventory Management System.

It includes:

* Add Item
* Quantity
* Price
* Delete Item
* Shows Total Items
* Uses HTML5 semantic elements
* Uses JavaScript DOM

---

## Inventory Management (HTML5 + JavaScript DOM)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Inventory System</title>
</head>
<body>

<header>
    <h1>Inventory Management</h1>
</header>

<main>

<section>
    <input type="text" id="name" placeholder="Item Name">
    <input type="number" id="qty" placeholder="Qty">
    <input type="number" id="price" placeholder="Price">
    <button onclick="addItem()">Add</button>
    <p>Total Items: <span id="total">0</span></p>
</section>

<section id="list"></section>

</main>

<footer>
    <p>Simple Inventory Page</p>
</footer>

<script>
var count = 0;

function addItem() {
    var n = document.getElementById("name").value;
    var q = document.getElementById("qty").value;
    var p = document.getElementById("price").value;

    if(n=="" || q=="" || p=="") return;

    var item = document.createElement("p");
    item.innerHTML = n + " | Qty: " + q + " | Price: " + p +
        " <button onclick='removeItem(this)'>Delete</button>";

    document.getElementById("list").appendChild(item);

    count++;
    document.getElementById("total").innerHTML = count;

    document.getElementById("name").value="";
    document.getElementById("qty").value="";
    document.getElementById("price").value="";
}

function removeItem(btn) {
    btn.parentElement.remove();
    count--;
    document.getElementById("total").innerHTML = count;
}
</script>

</body>
</html>
```

---

### Why this is perfect for exam:

* Very small code
* Clearly shows DOM manipulation
* Easy functions
* Clean semantic structure

Below is a **small, exam-friendly Registration Form** using **HTML5 + Bootstrap (customized a little)** and **RegEx validation in JavaScript**.

✅ Uses Bootstrap CDN
✅ Custom Bootstrap look (small styling)
✅ Validates with RegEx: **Name, Email, Phone, Password**
✅ Easy daily-life fields, simple code

---

## Registration Form (HTML5 + Customized Bootstrap + RegEx)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Registration</title>

  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">

  <style>
    .box{max-width:420px;margin:40px auto;padding:20px;border:1px solid #ddd;border-radius:12px}
    .btn-custom{background:#0d6efd;color:#fff}
  </style>
</head>
<body class="bg-light">

<header class="text-center py-3">
  <h2 class="m-0">User Registration</h2>
</header>

<main class="box bg-white">
  <form onsubmit="return check()">
    <label class="form-label">Full Name</label>
    <input class="form-control mb-2" id="name" placeholder="Rahul Kumar">

    <label class="form-label">Email</label>
    <input class="form-control mb-2" id="email" placeholder="rahul@gmail.com">

    <label class="form-label">Phone</label>
    <input class="form-control mb-2" id="phone" placeholder="10 digit number">

    <label class="form-label">Password</label>
    <input class="form-control mb-2" id="pass" type="password" placeholder="Min 6 chars">

    <p class="text-danger small" id="msg"></p>

    <button class="btn btn-custom w-100">Register</button>
  </form>
</main>

<script>
function check(){
  var n=document.getElementById("name").value.trim();
  var e=document.getElementById("email").value.trim();
  var ph=document.getElementById("phone").value.trim();
  var p=document.getElementById("pass").value;

  var rn=/^[A-Za-z ]{3,}$/;                 // name: letters + space, min 3
  var re=/^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$/; // email
  var rph=/^[0-9]{10}$/;                    // phone: 10 digits
  var rp=/^(?=.*[A-Za-z])(?=.*\d).{6,}$/;   // pass: 6+, letter+number

  var m="";
  if(!rn.test(n)) m="Enter valid name (min 3 letters).";
  else if(!re.test(e)) m="Enter valid email.";
  else if(!rph.test(ph)) m="Phone must be 10 digits.";
  else if(!rp.test(p)) m="Password: 6+ chars with 1 letter & 1 number.";

  document.getElementById("msg").innerHTML=m;
  return m=="";  // true = submit, false = stop
}
</script>

</body>
</html>
```

---
### 1) HRM scenario: Entities, attributes, relationships, constraints (ER)

#### Entities + key attributes

* **DEPARTMENT**(**dept_id**, dept_name)
* **EMPLOYEE**(**emp_id**, f_name, l_name, salary, dept_id, supervisor_id)
* **PROJECT**(**proj_id**, proj_name, status, budget, dept_id)
* **WORKS_ON**(**emp_id**, **proj_id**)  *(bridge table for M:N)*
* **DEPENDENT**(**dep_id**, dep_name, relation, emp_id)
* **PROJECT_CITY**(**proj_id**, **city**) *(project can be in multiple cities)*

#### Relationships + cardinality + participation

1. **DEPARTMENT — employs — EMPLOYEE**

   * Cardinality: **1 : N** (one dept has many employees)
   * Participation: **EMPLOYEE total** (every employee must belong to a dept), **DEPARTMENT partial**
2. **EMPLOYEE — supervises — EMPLOYEE** (recursive)

   * Cardinality: **1 : N** (one supervisor can supervise many employees)
   * Participation: **partial** (top manager may have NULL supervisor_id)
3. **DEPARTMENT — controls — PROJECT**

   * Cardinality: **1 : N**
   * Participation: **PROJECT total** (every project must be controlled by a dept)
4. **EMPLOYEE — works_on — PROJECT** (via WORKS_ON)

   * Cardinality: **M : N**
   * Participation: **partial** (employee may work on 0 projects; project may have 0 employees in simple model)
5. **EMPLOYEE — has — DEPENDENT**

   * Cardinality: **1 : N**
   * Participation: **DEPENDENT total**, **EMPLOYEE partial**
6. **PROJECT — located_in — CITY** (via PROJECT_CITY)

   * Cardinality: **1 : N** (one project can be in many cities)

---

## 2) ER → Relational schema (mapping)

* DEPARTMENT(**dept_id**, dept_name)
* EMPLOYEE(**emp_id**, f_name, l_name, salary, dept_id → DEPARTMENT.dept_id, supervisor_id → EMPLOYEE.emp_id)
* PROJECT(**proj_id**, proj_name, status, budget, dept_id → DEPARTMENT.dept_id)
* WORKS_ON(**emp_id** → EMPLOYEE.emp_id, **proj_id** → PROJECT.proj_id, PK(emp_id, proj_id))
* DEPENDENT(**dep_id**, dep_name, relation, emp_id → EMPLOYEE.emp_id)
* PROJECT_CITY(**proj_id** → PROJECT.proj_id, **city**, PK(proj_id, city))

---

# 3) Create tables + insert small sample data (easy, exam-friendly)

```sql
CREATE TABLE Department(
  dept_id INT PRIMARY KEY,
  dept_name VARCHAR(20) UNIQUE
);

CREATE TABLE Employee(
  emp_id INT PRIMARY KEY,
  f_name VARCHAR(20),
  l_name VARCHAR(20),
  salary INT,
  dept_id INT NOT NULL,
  supervisor_id INT,
  FOREIGN KEY(dept_id) REFERENCES Department(dept_id),
  FOREIGN KEY(supervisor_id) REFERENCES Employee(emp_id)
);

CREATE TABLE Project(
  proj_id INT PRIMARY KEY,
  proj_name VARCHAR(30),
  status VARCHAR(12),     -- 'Ongoing' / 'Completed'
  budget INT,             -- use rupees
  dept_id INT NOT NULL,
  FOREIGN KEY(dept_id) REFERENCES Department(dept_id)
);

CREATE TABLE Works_On(
  emp_id INT,
  proj_id INT,
  PRIMARY KEY(emp_id, proj_id),
  FOREIGN KEY(emp_id) REFERENCES Employee(emp_id),
  FOREIGN KEY(proj_id) REFERENCES Project(proj_id)
);

CREATE TABLE Dependent(
  dep_id INT PRIMARY KEY,
  dep_name VARCHAR(20),
  relation VARCHAR(12),
  emp_id INT NOT NULL,
  FOREIGN KEY(emp_id) REFERENCES Employee(emp_id)
);

CREATE TABLE Project_City(
  proj_id INT,
  city VARCHAR(20),
  PRIMARY KEY(proj_id, city),
  FOREIGN KEY(proj_id) REFERENCES Project(proj_id)
);

-- DATA
INSERT INTO Department VALUES
(1,'Finance'),(2,'R&D'),(3,'HR');

INSERT INTO Employee VALUES
(101,'Amit','Shah',90000,1,105),
(102,'Neha','Singh',70000,1,105),
(103,'Ravi','Kumar',120000,2,106),
(104,'Pooja','Nair',95000,2,106),
(105,'Sita','Rao',150000,3,NULL),
(106,'Arun','Das',140000,2,105),
(107,'Kiran','Patel',80000,3,105),
(108,'Vijay','Mehta',110000,2,106);

INSERT INTO Project VALUES
(201,'Payroll App','Ongoing',400000,1),
(202,'Budget Tool','Completed',600000,1),
(203,'AI HR','Ongoing',800000,2),
(204,'Lab System','Completed',500000,2),
(205,'Recruit Portal','Ongoing',300000,3);

INSERT INTO Works_On VALUES
(101,201),(101,202),
(102,201),
(103,203),(103,204),(103,201),
(104,203),(104,204),(104,201),
(108,203),(108,204),(108,201);

INSERT INTO Dependent VALUES
(1,'Anu','Spouse',103),
(2,'Ria','Child',103),
(3,'Dev','Child',101);

INSERT INTO Project_City VALUES
(201,'Mumbai'),
(203,'Bengaluru'),(203,'Hyderabad'),
(204,'Chennai'),
(205,'Delhi'),(205,'Mumbai');
```

---

# 4) SQL for the given problems

### 1) f_Name, l_Name, dept_Name of employees whose salary > average salary of Finance dept

```sql
SELECT e.f_name, e.l_name, d.dept_name
FROM Employee e JOIN Department d ON e.dept_id=d.dept_id
WHERE e.salary > (
  SELECT AVG(e2.salary)
  FROM Employee e2 JOIN Department d2 ON e2.dept_id=d2.dept_id
  WHERE d2.dept_name='Finance'
);
```

### 2) employee name + department who works on > 2 projects controlled by R&D

```sql
SELECT e.f_name, e.l_name, d.dept_name
FROM Employee e
JOIN Department d ON e.dept_id=d.dept_id
JOIN Works_On w ON e.emp_id=w.emp_id
JOIN Project p ON w.proj_id=p.proj_id
JOIN Department rd ON p.dept_id=rd.dept_id
WHERE rd.dept_name='R&D'
GROUP BY e.emp_id, e.f_name, e.l_name, d.dept_name
HAVING COUNT(*) > 2;
```

### 3) all ongoing projects controlled by all departments (dept + project)

```sql
SELECT d.dept_name, p.proj_name
FROM Department d JOIN Project p ON d.dept_id=p.dept_id
WHERE p.status='Ongoing'
ORDER BY d.dept_name;
```

### 4) supervisor details supervising >3 employees who completed at least one project

```sql
SELECT s.emp_id, s.f_name, s.l_name, s.salary
FROM Employee s
JOIN Employee e ON e.supervisor_id = s.emp_id
WHERE EXISTS (
  SELECT 1
  FROM Works_On w JOIN Project p ON w.proj_id=p.proj_id
  WHERE w.emp_id=e.emp_id AND p.status='Completed'
)
GROUP BY s.emp_id, s.f_name, s.l_name, s.salary
HAVING COUNT(*) > 3;
```

### 5) names of dependents of employees whose completed projects total budget = 10L (10,00,000)

```sql
SELECT dep.dep_name
FROM Dependent dep
JOIN (
  SELECT w.emp_id
  FROM Works_On w JOIN Project p ON w.proj_id=p.proj_id
  WHERE p.status='Completed'
  GROUP BY w.emp_id
  HAVING SUM(p.budget) = 1000000
) x ON dep.emp_id = x.emp_id;
```

### 6) department + employee details whose project is in more than one city

```sql
SELECT DISTINCT d.dept_name, e.emp_id, e.f_name, e.l_name
FROM Employee e
JOIN Department d ON e.dept_id=d.dept_id
JOIN Works_On w ON e.emp_id=w.emp_id
JOIN (
  SELECT proj_id
  FROM Project_City
  GROUP BY proj_id
  HAVING COUNT(*) > 1
) pc ON w.proj_id = pc.proj_id;
```

---
### 1) HRM scenario: Entities, attributes, relationships, constraints (ER)

#### Entities + key attributes

* **DEPARTMENT**(**dept_id**, dept_name)
* **EMPLOYEE**(**emp_id**, f_name, l_name, salary, dept_id, supervisor_id)
* **PROJECT**(**proj_id**, proj_name, status, budget, dept_id)
* **WORKS_ON**(**emp_id**, **proj_id**)  *(bridge table for M:N)*
* **DEPENDENT**(**dep_id**, dep_name, relation, emp_id)
* **PROJECT_CITY**(**proj_id**, **city**) *(project can be in multiple cities)*

#### Relationships + cardinality + participation

1. **DEPARTMENT — employs — EMPLOYEE**

   * Cardinality: **1 : N** (one dept has many employees)
   * Participation: **EMPLOYEE total** (every employee must belong to a dept), **DEPARTMENT partial**
2. **EMPLOYEE — supervises — EMPLOYEE** (recursive)

   * Cardinality: **1 : N** (one supervisor can supervise many employees)
   * Participation: **partial** (top manager may have NULL supervisor_id)
3. **DEPARTMENT — controls — PROJECT**

   * Cardinality: **1 : N**
   * Participation: **PROJECT total** (every project must be controlled by a dept)
4. **EMPLOYEE — works_on — PROJECT** (via WORKS_ON)

   * Cardinality: **M : N**
   * Participation: **partial** (employee may work on 0 projects; project may have 0 employees in simple model)
5. **EMPLOYEE — has — DEPENDENT**

   * Cardinality: **1 : N**
   * Participation: **DEPENDENT total**, **EMPLOYEE partial**
6. **PROJECT — located_in — CITY** (via PROJECT_CITY)

   * Cardinality: **1 : N** (one project can be in many cities)

---

## 2) ER → Relational schema (mapping)

* DEPARTMENT(**dept_id**, dept_name)
* EMPLOYEE(**emp_id**, f_name, l_name, salary, dept_id → DEPARTMENT.dept_id, supervisor_id → EMPLOYEE.emp_id)
* PROJECT(**proj_id**, proj_name, status, budget, dept_id → DEPARTMENT.dept_id)
* WORKS_ON(**emp_id** → EMPLOYEE.emp_id, **proj_id** → PROJECT.proj_id, PK(emp_id, proj_id))
* DEPENDENT(**dep_id**, dep_name, relation, emp_id → EMPLOYEE.emp_id)
* PROJECT_CITY(**proj_id** → PROJECT.proj_id, **city**, PK(proj_id, city))

---

# 3) Create tables + insert small sample data (easy, exam-friendly)

```sql
CREATE TABLE Department(
  dept_id INT PRIMARY KEY,
  dept_name VARCHAR(20) UNIQUE
);

CREATE TABLE Employee(
  emp_id INT PRIMARY KEY,
  f_name VARCHAR(20),
  l_name VARCHAR(20),
  salary INT,
  dept_id INT NOT NULL,
  supervisor_id INT,
  FOREIGN KEY(dept_id) REFERENCES Department(dept_id),
  FOREIGN KEY(supervisor_id) REFERENCES Employee(emp_id)
);

CREATE TABLE Project(
  proj_id INT PRIMARY KEY,
  proj_name VARCHAR(30),
  status VARCHAR(12),     -- 'Ongoing' / 'Completed'
  budget INT,             -- use rupees
  dept_id INT NOT NULL,
  FOREIGN KEY(dept_id) REFERENCES Department(dept_id)
);

CREATE TABLE Works_On(
  emp_id INT,
  proj_id INT,
  PRIMARY KEY(emp_id, proj_id),
  FOREIGN KEY(emp_id) REFERENCES Employee(emp_id),
  FOREIGN KEY(proj_id) REFERENCES Project(proj_id)
);

CREATE TABLE Dependent(
  dep_id INT PRIMARY KEY,
  dep_name VARCHAR(20),
  relation VARCHAR(12),
  emp_id INT NOT NULL,
  FOREIGN KEY(emp_id) REFERENCES Employee(emp_id)
);

CREATE TABLE Project_City(
  proj_id INT,
  city VARCHAR(20),
  PRIMARY KEY(proj_id, city),
  FOREIGN KEY(proj_id) REFERENCES Project(proj_id)
);

-- DATA
INSERT INTO Department VALUES
(1,'Finance'),(2,'R&D'),(3,'HR');

INSERT INTO Employee VALUES
(101,'Amit','Shah',90000,1,105),
(102,'Neha','Singh',70000,1,105),
(103,'Ravi','Kumar',120000,2,106),
(104,'Pooja','Nair',95000,2,106),
(105,'Sita','Rao',150000,3,NULL),
(106,'Arun','Das',140000,2,105),
(107,'Kiran','Patel',80000,3,105),
(108,'Vijay','Mehta',110000,2,106);

INSERT INTO Project VALUES
(201,'Payroll App','Ongoing',400000,1),
(202,'Budget Tool','Completed',600000,1),
(203,'AI HR','Ongoing',800000,2),
(204,'Lab System','Completed',500000,2),
(205,'Recruit Portal','Ongoing',300000,3);

INSERT INTO Works_On VALUES
(101,201),(101,202),
(102,201),
(103,203),(103,204),(103,201),
(104,203),(104,204),(104,201),
(108,203),(108,204),(108,201);

INSERT INTO Dependent VALUES
(1,'Anu','Spouse',103),
(2,'Ria','Child',103),
(3,'Dev','Child',101);

INSERT INTO Project_City VALUES
(201,'Mumbai'),
(203,'Bengaluru'),(203,'Hyderabad'),
(204,'Chennai'),
(205,'Delhi'),(205,'Mumbai');
```

---

# 4) SQL for the given problems

### 1) f_Name, l_Name, dept_Name of employees whose salary > average salary of Finance dept

```sql
SELECT e.f_name, e.l_name, d.dept_name
FROM Employee e JOIN Department d ON e.dept_id=d.dept_id
WHERE e.salary > (
  SELECT AVG(e2.salary)
  FROM Employee e2 JOIN Department d2 ON e2.dept_id=d2.dept_id
  WHERE d2.dept_name='Finance'
);
```

### 2) employee name + department who works on > 2 projects controlled by R&D

```sql
SELECT e.f_name, e.l_name, d.dept_name
FROM Employee e
JOIN Department d ON e.dept_id=d.dept_id
JOIN Works_On w ON e.emp_id=w.emp_id
JOIN Project p ON w.proj_id=p.proj_id
JOIN Department rd ON p.dept_id=rd.dept_id
WHERE rd.dept_name='R&D'
GROUP BY e.emp_id, e.f_name, e.l_name, d.dept_name
HAVING COUNT(*) > 2;
```

### 3) all ongoing projects controlled by all departments (dept + project)

```sql
SELECT d.dept_name, p.proj_name
FROM Department d JOIN Project p ON d.dept_id=p.dept_id
WHERE p.status='Ongoing'
ORDER BY d.dept_name;
```

### 4) supervisor details supervising >3 employees who completed at least one project

```sql
SELECT s.emp_id, s.f_name, s.l_name, s.salary
FROM Employee s
JOIN Employee e ON e.supervisor_id = s.emp_id
WHERE EXISTS (
  SELECT 1
  FROM Works_On w JOIN Project p ON w.proj_id=p.proj_id
  WHERE w.emp_id=e.emp_id AND p.status='Completed'
)
GROUP BY s.emp_id, s.f_name, s.l_name, s.salary
HAVING COUNT(*) > 3;
```

### 5) names of dependents of employees whose completed projects total budget = 10L (10,00,000)

```sql
SELECT dep.dep_name
FROM Dependent dep
JOIN (
  SELECT w.emp_id
  FROM Works_On w JOIN Project p ON w.proj_id=p.proj_id
  WHERE p.status='Completed'
  GROUP BY w.emp_id
  HAVING SUM(p.budget) = 1000000
) x ON dep.emp_id = x.emp_id;
```

### 6) department + employee details whose project is in more than one city

```sql
SELECT DISTINCT d.dept_name, e.emp_id, e.f_name, e.l_name
FROM Employee e
JOIN Department d ON e.dept_id=d.dept_id
JOIN Works_On w ON e.emp_id=w.emp_id
JOIN (
  SELECT proj_id
  FROM Project_City
  GROUP BY proj_id
  HAVING COUNT(*) > 1
) pc ON w.proj_id = pc.proj_id;
```

---

