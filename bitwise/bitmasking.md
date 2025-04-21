## 🧠 Bitmasking

### ✅ One-liner Concept:
Masking is nothing but marking(setting) the bits.
...

### 🧩 Function Signature:
```c
GENMASK(h,l) (((~UL(0)) - (UL(1) << (l)) + 1) & (~UL(0) >> (BITS_PER_LONG - 1 - (h)))) // from linux/bits.h

Generates a bitmask with all bits set from bit position `l` (low) to `h` (high), inclusive.
...

```

### 📌 Implementation:
```c
For GENMASK(7, 4), it returns:
0b11110000 → Bits 7,6,5,4 are set
...
```

### ⚠️ Notes:
To generate a mask from bit l to bit h, we do this:

1. Make all bits 1: ~0UL

2. Clear bits below l: (~0UL) << l

3. Clear bits above h: (~0UL) >> (BITS_PER_LONG - 1 - h)

4. AND both results → mask between l and h only
...

### 🎯 Common Mistakes:
GENMASK(h, l) is not h << l!

7 << 4 = 0x70 ≠ 0xF0

You’re setting a range of bits, not shifting a number
...

### 🔁 Related:
BIT(nr) – sets a single bit

BIT_MASK(nr) – like BIT(nr) but architecture-safe
...
