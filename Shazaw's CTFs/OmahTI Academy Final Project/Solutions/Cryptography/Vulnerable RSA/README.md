# Solution: Vulnerable RSA

**Category:** Cryptography
**Points:** 500

---

### Analysis

The challenge provides the public components of an RSA encryption: the public exponent `e`, the modulus `n`, and the ciphertext `c`.

1.  The most significant clue is that the public exponent `e` is very small (`e = 3`). This immediately suggests a **Low Public Exponent Attack**.

2.  This attack is viable if the original message `m` was small enough that `m^e < n`. In this scenario, the encryption simplifies from `c = m^e mod n` to just `c = m^e`.

3.  The solution is to calculate the integer `e`-th root of `c`. This can be done with a Python script, which directly recovers the integer representation of the message. Converting this integer back to bytes reveals the flag.

### Solver Script

```python
import gmpy2
from Crypto.Util.number import long_to_bytes

# Values from the challenge file
e = 3
n = # Paste n from challenge.txt
c = # Paste c from challenge.txt

# Calculate the integer cube root of the ciphertext
message_int, is_exact_root = gmpy2.iroot(c, e)

if is_exact_root:
    # Convert the integer back to a readable string
    flag = long_to_bytes(message_int)
    print(flag.decode())
else:
    print("Attack failed. No exact integer root found.")

```

### Flag

OmahTIAcademy{L0w_Exp0n3nt_4tt4ck_RSA!}
