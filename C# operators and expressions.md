# 

🧮 C# Operators & Expressions
=============================

### (Arithmetic • Comparison • Logical • Bitwise • Null-coalescing • Null-conditional • String interpolation)

* * *

1️⃣ **Arithmetic Operators**
============================

| Operator | Meaning        | Example  | Result               |
| -------- | -------------- | -------- | -------------------- |
| `+`      | Addition       | `5 + 3`  | 8                    |
| `-`      | Subtraction    | `5 - 3`  | 2                    |
| `*`      | Multiplication | `5 * 3`  | 15                   |
| `/`      | Division       | `10 / 3` | 3 (integer division) |
| `%`      | Modulus        | `10 % 3` | 1                    |
| `++`     | Increment      | `x++`    | increases x by 1     |
| `--`     | Decrement      | `x--`    | decreases x by 1     |

✔️ Example:

    int a = 10;
    int b = 3;
    Console.WriteLine(a / b);  // 3
    Console.WriteLine(a % b);  // 1

* * *

2️⃣ **Comparison Operators**
============================

Used for Boolean results (`true`/`false`):

| Operator | Meaning          |
| -------- | ---------------- |
| `==`     | Equal            |
| `!=`     | Not equal        |
| `>`      | Greater than     |
| `<`      | Less than        |
| `>=`     | Greater or equal |
| `<=`     | Less or equal    |

✔️ Example:

    int x = 10;
    int y = 5;
    
    Console.WriteLine(x > y);   // True
    Console.WriteLine(x == y);  // False

* * *

3️⃣ **Logical Operators**
=========================

Used with Boolean expressions:

| Operator | Meaning | Example                 |
| -------- | ------- | ----------------------- |
| `&&`     | AND     | `true && false` → false |
| \`       |         | \`                      |
| `!`      | NOT     | `!true` → false         |

✔️ Example:

    bool isLogged = true;
    bool isAdmin = false;
    
    if (isLogged && !isAdmin)
    {
        Console.WriteLine("Normal user");
    }

* * *

4️⃣ **Bitwise Operators**
=========================

Operate on binary values.

| Operator | Meaning     | Example  |
| -------- | ----------- | -------- |
| `&`      | AND         | `5 & 3`  |
| \`       | \`          | OR       |
| `^`      | XOR         | `5 ^ 3`  |
| `~`      | NOT         | `~5`     |
| `<<`     | Left shift  | `5 << 1` |
| `>>`     | Right shift | `5 >> 1` |

✔️ Quick example:  
5 → `0101`  
3 → `0011`

    Console.WriteLine(5 & 3);  // 1
    Console.WriteLine(5 | 3);  // 7
    Console.WriteLine(5 ^ 3);  // 6

* * *

5️⃣ **Null-Coalescing Operator (`??`)**
=======================================

Returns **left value** if not null, otherwise **right value**.

    string name = null;
    string result = name ?? "Unknown";
    Console.WriteLine(result);  // Unknown

More examples:

    int? age = null;
    int realAge = age ?? 18;   // Default to 18

* * *

6️⃣ **Null-Conditional Operator (`?.`)**
========================================

Safely access a property/method **only if not null**.

Without null-conditional:

    if (user != null)
        Console.WriteLine(user.Name);

With `?.` (cleaner):

    Console.WriteLine(user?.Name);

✔️ If `user` is null → returns `null` instead of throwing exception.

Chaining:

    var city = person?.Address?.City;

* * *

7️⃣ **String Interpolation & Concatenation**
============================================

7.1 String Concatenation
------------------------

Old way:

    string name = "John";
    string msg = "Hello " + name + "!";

7.2 String Interpolation (best method)
--------------------------------------

    string name = "John";
    string msg = $"Hello {name}!";

✔️ Supports expressions:

    int a = 5, b = 3;
    Console.WriteLine($"Sum = {a + b}");

✔️ Format values:

    double price = 12.5;
    Console.WriteLine($"{price:C}"); // $12.50 (currency)

* * *

8️⃣ Complete Example (All Operators Used)
=========================================

    int? number = null;
    int value = number ?? 100;       // null-coalescing
    
    string name = null;
    string result = name?.ToUpper(); // null-conditional
    
    int a = 10, b = 3;
    
    Console.WriteLine($"Add: {a + b}");
    Console.WriteLine($"Compare: {a > b}");
    Console.WriteLine($"Logical: {true && false}");
    Console.WriteLine($"Bitwise AND: {a & b}");
    Console.WriteLine($"Hi {name ?? "Guest"}");

* * *


