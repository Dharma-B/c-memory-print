## 🧠 Count Set Bits (Hamming Weight)

### ✅ One-liner Concept:
Count the number of 1s in the binary representation.
...

### 🧩 Function Signature:
```c
int countSetBits(int n) {
...
```

### 📌 Implementation:
```c
int countSetBits(int n) {
    int count = 0;
    while (n) {
        count += n & 1;
        n >>= 1;
    }
    return count;
}
...
```

### 🎯 Common Mistakes:
you don't essentially need to convert the given number to binary
representation and start counting the bits, do it alltogether.
...

