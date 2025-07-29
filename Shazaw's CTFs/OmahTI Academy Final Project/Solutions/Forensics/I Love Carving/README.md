# Solution: I Love Carving

**Category:** Forensics
**Points:** 750

---

### Analysis

This challenge requires finding a flag that has been split into three separate pieces within the `Carving.jpeg` file.

1.  **Part 1:** The first part of the flag is written directly on the image itself and is visible when the file is opened.

2.  **Part 2:** The second part is hidden in the metadata. Running `exiftool` on the image reveals a Base64 string in the `License` field. Decoding this string provides the middle part of the flag.

3.  **Part 3:** The final part is appended to the end of the file. By opening the image in a hex editor and scrolling to the very bottom, the remaining text of the flag can be found after the standard JPEG End of Image marker.

4.  Combining these three parts in order reveals the complete flag.

### Flag
OmahTIAcademy{Y0_good_JOB_G3tting_This_Flag_98275}
