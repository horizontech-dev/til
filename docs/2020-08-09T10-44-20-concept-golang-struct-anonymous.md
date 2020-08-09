---
date: 2020-08-09T10:44:20-07:00
title: Concept-Golang-Struct-Anonymous
tags: Go
---

# Concept-Golang-Struct-Anonymous

struct fields can be **anonymous**. Meaning they can be declared without a name

```go
type Employee {
Name string
Salary int
int
}
```

Using nested structs one can do a ***field promotion***. A simple example

```go
type Person {
Age int
Employee
}

var p Person
p.Name = "Horizon Technologies"
```

Here *Employee* is a nested struct (since its declared inside *Person* struct). While accessing *Employee* fields one can access it as if its from the field declared in Person.



