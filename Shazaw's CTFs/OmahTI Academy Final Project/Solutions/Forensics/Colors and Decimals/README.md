# Solution: Colors and Decimals

**Category:** Forensics
**Points:** 750

---

### Analysis

The challenge is a tiny 13x1 pixel PNG image. The solution involves extracting information from the pixel color values.

1.  Inspecting the image with `exiftool` confirms its small dimensions and that it uses the `RGB with Alpha` color type.

2.  The next step is to extract the RGBA (Red, Green, Blue, Alpha) values for each of the 13 pixels. This can be done with an online tool or a simple script.

3.  The extracted numbers are decimal ASCII codes. For each pixel, the R, G, and B values represent a sequence of characters. The Alpha channel is ignored.

4.  By converting each decimal value to its corresponding ASCII character and concatenating them in order, the flag is reconstructed.

### Flag

OmahTIAcademy{RGBA_Is_Th3_N3xt_L3v3l!}
