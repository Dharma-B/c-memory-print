## 🧠 Is power of 2

### ✅ One-liner Concept:
2 power anything is always even.
...

### 🧩 Function Signature:
```c
bool ispowerof2(int x)
...
```

### 📌 Implementation:
```c
bool ispowerof2(int x) {
    return x > 0 && (x & (x - 1)) == 0;
}
...
```
