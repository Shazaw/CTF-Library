# Solution: Corrupt3d

**Category:** Forensics
**Points:** 500

---

### Analysis

The task is to repair the `Corrupt3d.png` file so it can be viewed.

1.  Attempting to open the file fails. A preliminary check using the `file` command reveals that the operating system does not recognize it as a PNG image.

2.  Inspecting the file's hexdump using `xxd` shows that the first eight bytes (the file signature or "magic numbers") are incorrect for a PNG file. The standard PNG signature is `89 50 4E 47 0D 0A 1A 0A`.

    <img width="774" height="213" alt="image" src="https://github.com/user-attachments/assets/5b6d51be-518d-4d63-b3a2-2938d095e54f" />


3.  The solution is to use a hex editor to manually replace the incorrect header with the correct 8-byte PNG signature.

4.  After saving the corrected file, it can be opened with any image viewer, which now displays the flag.

### Flag

OmahTIAcademy{Quick_Hexdata_Fix_For_Png}
