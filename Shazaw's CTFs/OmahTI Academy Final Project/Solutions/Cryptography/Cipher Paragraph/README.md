# Solution: Cipher Paragraph

**Category:** Cryptography
**Points:** 750

---

### Analysis

This is a complex, multi-layered cipher challenge where each step reveals the clue for the next.

1.  **Layer 1 (Substitution):** The first line of the text is a 26-letter substitution alphabet (`qazwsx...`). This is used to decrypt the entire paragraph. The result reveals the first plaintext clue: `...le chiffre INDECHIFFRABLE`.

2.  **Layer 2 (Vigenère):** The word `INDECHIFFRABLE` is the key for a Vigenère cipher. This is used to decrypt the new ciphertext, revealing the next clue: `...what MONOALPHABETIC means?`.

3.  **Layer 3 (Keyword):** The word `MONOALPHABETIC` is used as the key for a keyword cipher (after removing duplicate letters). Decrypting the next layer reveals the final clue: `...roman generals and the number twenty`.

4.  **Layer 4 (Caesar/ROT):** The final clue points to a ROT20 cipher. Applying a shift of 20 to the final ciphertext reveals the flag's content.

### Flag

OmahTIAcademy{throughthejourneyofciphers}
