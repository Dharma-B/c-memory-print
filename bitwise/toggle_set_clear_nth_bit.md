## 🧠 Toggle/Set/Clear nth bit

### ✅ One-liner Concept:
Set -> 1 at given pos.
Clear -> 0 at given pos.
Toggle -> set if 0 and clear if 1
...

### 🧩 Function Signature:
```c
int set_bit(int n, int pos)
int clear_bit(int n, int pos)
int toggle_bit(int n, int pos)
...
```

### 📌 Implementation:
```c
int set_bit(int n, int pos) {
    return n | (1 << pos);
}
int clear_bit(int n, int pos) {
    return n & ~(1 << pos);
}
int toggle_bit(int n, int pos) {
    return n ^ (1 << pos);
}
bool is_bit_set(int n, int pos) {
    return n & (1 << pos);
}
...
```

### ⚠️ Notes:
Another application of XOR
...

### 🎯 Common Mistakes:
x ^ x = 0	Identity property
x ^ 0 = x	Zero identity
x ^ y ^ x = y	Useful in undoing XOR
...

### 🔁 Related:
swap
...
