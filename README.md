# Golang Basics — Day 1 (05/02/2025)

## 🧱 Basic Go Program Structure

```go
package main  // Required for all standalone Go programs

import "fmt"  // "fmt" is the package for formatted I/O (like print statements)

func main() {
    // This is a comment
    fmt.Println("Hello, Go!")  // Prints text followed by a new line
}
```

| Part               | What It Means                                                                                 |
| ------------------ | --------------------------------------------------------------------------------------------- |
| `package main`     | Every Go file starts by declaring a package. `main` is special — it’s where execution starts. |
| `import "fmt"`     | You're telling Go: “Hey, I want to use print stuff!”                                          |
| `func main()`      | Like Python's `if __name__ == "__main__"` — this is your entry point.                         |
| `fmt.Println(...)` | Just like Python’s `print()`, this prints text to the screen with a newline.                  |

---

## 📏 Style: Space Between `main()` and `{`

### ✅ Does this work?

```go
func main(){
    fmt.Println("sid")
}
```

✔️ Yes, it works.

### ✅ Is this better?

```go
func main() {
    fmt.Println("sid")
}
```

✔️ Yes, this is **idiomatic Go**.

### 📌 Why?

* Go has a tool called `gofmt` that formats code.
* It prefers and enforces the space for readability.

---

## 🧠 Variables in Go — 3 Ways

### 1. Short Declaration (Most Common)

```go
name := "Sid"
age := 25
```

* `:=` means "create and assign"
* Only valid **inside functions**

### 2. Explicit Type Declaration

```go
var name string = "Sid"
var age int = 25
```

* Use this when you want to **be clear** about the type

### 3. Zero-value Declaration

```go
var score int
```

* Declares `score` as `int`, assigns default value `0`
* Similarly declares `""` for strings and `false` for booleans

---

## 🧪 Practice Example

```go
package main

import "fmt"

func main() {
    name := "Sid"           // Go figures out it's a string
    var age int = 25        // Explicitly tell Go it's an int
    var city string         // Will be "" (empty string) by default

    fmt.Println("Name:", name)
    fmt.Println("Age:", age)
    fmt.Println("City:", city)  // Prints empty string
}
```
---

## 🛠 Key Rules Summary

| Syntax         | Meaning                                       |
| -------------- | --------------------------------------------- |
| `:=`           | Use for declare+assign inside functions       |
| `var`          | Use when assigning later or outside functions |
| `const`        | Use for values that never change              |
| Type Inference | Go will auto-detect the type with `:=`        |

---
