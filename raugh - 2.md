Absolutely — here is a clean, professional **Overview + Topics Table + Example** for **Conditional Logic**, written in **Mentor Mode**, similar structure to your Control Flow & Iteration contents page.

---

Perfect — here is the **same structure** with **exactly 5 doubts**.

---

###### **Q1. When should I use `match` instead of `switch` in PHP?**

**Answer** -- Use **`match`** when you need a **returned value**, **strict comparison**, and **clean, safe branching**.  
Use **`switch`** only for **legacy** or **very simple procedural CLI code**.

### **Example**

```php
// Preferred modern approach — match
$statusCode = 404;

$message = match ($statusCode) {
    200 => 'OK',
    201 => 'Created',
    400 => 'Bad Request',
    401 => 'Unauthorized',
    403 => 'Forbidden',
    404 => 'Not Found',
    500 => 'Server Error',
    default => 'Unknown Status',
};

// Old approach — switch (avoid in modern code)
switch ($statusCode) {
    case 200: $message = 'OK'; break;
    // ... more cases
}
```

###### **Doubt Table (Yes / No)** — _Top 5 Confusions_

|Doubt|Yes|No|
|---|:-:|:-:|
|Does `match` always require a `default` case?||✔️|
|Does `match` return a value directly?|✔️||
|Can `match` fall through multiple cases like `switch`?||✔️|
|Is `match` faster or at least equal in performance to `switch`?|✔️||
|Should I prefer `match` in new modern PHP codebases (2025+)?|✔️||

---
