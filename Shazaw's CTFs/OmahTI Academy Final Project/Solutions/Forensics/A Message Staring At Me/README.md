# Solution: A Message Staring At Me

**Category:** Forensics
**Points:** 500

---

### Analysis

This challenge requires finding a hidden message within the `cat.png` image file.

1.  The first step is to analyze the image's metadata using `exiftool`. This reveals an unusual Base64 string in the `License` metadata field.

    <img width="771" height="284" alt="image" src="https://github.com/user-attachments/assets/394e98bf-684c-40f8-a525-33c6e93d026d" />


2.  Decoding this Base64 string using a tool like CyberChef reveals a clear hint: `Do you remember what LSB is?`

    <img width="784" height="136" alt="image" src="https://github.com/user-attachments/assets/9ec680aa-c2f4-4290-aeca-d61d12a40d5c" />


3.  The hint points to Least Significant Bit (LSB) steganography. Using an LSB analysis tool like `zsteg` on the `cat.png` file will extract the hidden flag from the image's data planes.

### Flag

OmahTIAcademy{F1ndi1ng_H1dd3n_Mean1NG5_Beh1nd_Imag3s}
