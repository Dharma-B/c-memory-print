## 🧠 Check Even Odd

### ✅ One-liner Concept:
- **Even number**: Last bit is `0`
- **Odd number**: Last bit is `1`
...

### 🧩 Function Signature:
```c
if (x & 1) {
    // Odd
} else {
    // Even
}
...
```

### 📌 Implementation:
```c
const char* check_even_odd(int x) {
    return (x & 1) ? "Odd" : "Even";
}
...
```

### ⚠️ Notes:
if (x % 2 == 0) → Even
else → Odd
Bitwise & 1 is faster and used in low-level code (like embedded or kernel logic).
...

### 🎯 Common Mistakes:
Using `%` for performance-critical code
```c
if (x % 2 == 0)  // Works but slower than bitwise AND
...

### 🔁 Related:
...
