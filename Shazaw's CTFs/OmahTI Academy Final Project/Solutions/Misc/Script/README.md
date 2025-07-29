# Solution: Script

**Category:** Misc
**Points:** 500

---

### Analysis

The challenge is a very large text file (`script.txt`) containing a movie script. The flag is hidden somewhere within it.

1.  The file is too large to read manually. The most efficient method is to search for the known flag format.

2.  Using the `grep` command-line utility to search for the string "OmahTIAcademy" instantly locates and prints the line containing the flag.

### Command

```bash
grep "OmahTIAcademy" script.txt
```

### Flag

OmahTIAcademy{What_a_FUn_Scr1pt!}
