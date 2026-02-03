## $${\color{red}PHP}$$


**PHP (Hypertext Preprocessor)** - **server-side scripting language** designed mainly for **web development**. It runs on the server, generates HTML (or JSON/XML), and sends the result to the browser. The client never sees the PHP code itself—only the output.

---

### Core Characteristics

* **Server-side** (executes before response is sent)
* **Interpreted** (no compilation step needed)
* **Loosely typed** but supports **strict typing**
* **Embedded in HTML**
* Cross-platform (Linux, Windows, macOS)
* Works with most web servers (Apache, Nginx, IIS)

---

### Typical PHP Flow

1. Browser sends HTTP request
2. Web server passes request to PHP
3. PHP executes logic (DB queries, calculations, API calls)
4. PHP outputs HTML/JSON
5. Browser renders the result

---

### Syntax Basics

* PHP code is wrapped in `<?php ... ?>`
* Statements end with `;`
* Variables start with `$`
* Case-sensitive for variables, not for keywords

```php
<?php
$name = "John";
echo "Hello $name";
```

---

### Data Types

* **Scalar**: `int`, `float`, `string`, `bool`
* **Compound**: `array`, `object`, `callable`
* **Special**: `null`, `resource`

PHP supports **type declarations**:

```php
function sum(int $a, int $b): int {
    return $a + $b;
}
```

---

### Control Structures

* Conditionals: `if`, `else`, `elseif`, `switch`
* Loops: `for`, `foreach`, `while`, `do-while`
* Control keywords: `break`, `continue`, `return`

---

### Arrays (Very Important in PHP)

* Indexed arrays
* Associative arrays
* Multidimensional arrays

```php
$user = [
    'name' => 'Anna',
    'age' => 30
];
```

Powerful built-in functions:
`array_map`, `array_filter`, `array_reduce`, `in_array`, `array_merge`

---

### Functions

* User-defined functions
* Anonymous functions (closures)
* Arrow functions (short syntax)

```php
$add = fn($a, $b) => $a + $b;
```

Supports:

* Default parameters
* Type hints
* Return types

---

### Object-Oriented Programming (OOP)

PHP is fully **object-oriented**.

Key concepts:

* Classes & objects
* Constructors & destructors
* Visibility: `public`, `protected`, `private`
* Inheritance
* Interfaces
* Traits
* Abstract classes
* Namespaces

```php
class User {
    public function __construct(
        private string $name
    ) {}
}
```

---

### Error Handling

* Traditional: warnings, notices, fatal errors
* Modern: **Exceptions**

```php
try {
    throw new Exception("Error!");
} catch (Exception $e) {
    echo $e->getMessage();
}
```

---

### Working With Forms & HTTP

* Superglobals:

  * `$_GET`
  * `$_POST`
  * `$_REQUEST`
  * `$_SERVER`
  * `$_FILES`
  * `$_COOKIE`
  * `$_SESSION`

PHP is tightly integrated with HTTP and form handling.

---

### Sessions & Cookies

* **Sessions**: server-side user state
* **Cookies**: client-side storage

```php
session_start();
$_SESSION['user_id'] = 123;
```

---

### Database Integration

Supports many databases:

* MySQL / MariaDB
* PostgreSQL
* SQLite
* Oracle, MSSQL

Recommended approach:

* **PDO (PHP Data Objects)**

```php
$pdo = new PDO($dsn, $user, $pass);
$stmt = $pdo->prepare("SELECT * FROM users");
$stmt->execute();
```

---

### Security Features

PHP provides tools, but **security is the developer’s responsibility**:

* Password hashing: `password_hash()`
* SQL injection protection (prepared statements)
* XSS protection (`htmlspecialchars`)
* CSRF tokens
* Input validation & sanitization

---

### File System & I/O

* Read/write files
* Upload files
* Directory operations

```php
file_put_contents("test.txt", "Hello");
```

---

### Modern PHP (7.x – 8.x+)

Key improvements:

* Huge performance boost
* Strict typing
* Typed properties
* Enums
* Match expressions
* Nullsafe operator (`?->`)
* Attributes (annotations replacement)

---

### Ecosystem

* **Composer** – dependency manager
* **Frameworks**:

  * Laravel
  * Symfony
  * Slim
* **CMS**:

  * WordPress
  * Drupal
* **Testing**:

  * PHPUnit
* **Standards**:

  * PSR (PHP-FIG)

---

### Common Use Cases

* Dynamic websites
* REST APIs
* CMS & e-commerce platforms
* Backend for SPA apps
* CLI scripts & automation

---
