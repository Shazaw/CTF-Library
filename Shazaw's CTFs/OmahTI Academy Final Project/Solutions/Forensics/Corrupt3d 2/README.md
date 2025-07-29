# Solution: Corrupt3d 2

**Category:** Forensics
**Points:** 750

---

### Analysis

This is another corrupted PNG challenge, but the hint "it has something to do with a 'check'" points towards a CRC (Cyclic Redundancy Check) error.

1.  Similar to the first `Corrupt3d` challenge, the file signature is incorrect and must be fixed first using a hex editor.

2.  Even after fixing the header, the file still won't open. Using the `pngcheck -v` command provides a verbose analysis of the PNG structure.

3.  The tool reports a **CRC error in the IHDR chunk**. It shows the `computed` (correct) CRC and the `expected` (incorrect) CRC that is currently in the file.

    <img width="726" height="245" alt="image" src="https://github.com/user-attachments/assets/5a36c7b5-541c-4522-a4d9-281a0fc258e0" />


4.  The next step is to find the incorrect CRC value (`f011a9d9` in the write-up) in the file's hexdump and replace it with the correct, computed value (`e5af27e8`).

5.  After patching the CRC value and saving, the PNG is fully repaired and can be opened to view the flag.

### Flag

OmahTIAcademy{Hexdata_But_This_Time_CRC!}
