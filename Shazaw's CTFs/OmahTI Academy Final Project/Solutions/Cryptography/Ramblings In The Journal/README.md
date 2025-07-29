# Solution: Ramblings in the Journal

**Category:** Cryptography
**Points:** 500

---

### Analysis

The challenge provides a text file containing a paragraph where every word begins with a capital letter.

1.  The first step is to extract the first letter of every word from the text.

2.  The resulting string is then processed with a ROT13 cipher.

3.  This result appears to be gibberish. The final insight is to **reverse** this string, which reveals the meaningful text `TITLECASECRYPTO`.

### Flag

OmahTIAcademy{TITLECASECRYPTO}
