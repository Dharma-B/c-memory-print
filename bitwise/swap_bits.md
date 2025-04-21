## 🧠 Swap Bits

### ✅ One-liner Concept:
Swap two variables without using a temporary variable, using XOR.
...

### 🧩 Function Signature:
```c
void swap(int* a, int* b)
...
```

### 📌 Implementation:
```c
void swap(int* a, int* b) {
    if (a == b) return; // Important: avoid undefined behavior when pointers alias
    *a ^= *b;
    *b ^= *a;
    *a ^= *b;
}
...
```

### ⚠️ Notes:
❌ Never use XOR swap when a == b or they alias the same memory — it zeroes out!
...

### 🎯 Common Mistakes:
x ^ x = 0	Identity property
x ^ 0 = x	Zero identity
x ^ y ^ x = y	Useful in undoing XOR
...

### 🔁 Related:
Toggle
...
