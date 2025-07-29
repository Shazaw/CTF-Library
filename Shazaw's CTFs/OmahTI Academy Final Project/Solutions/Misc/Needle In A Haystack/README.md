# Solution: Needle in a Haystack

**Category:** Misc
**Points:** 500

---

### Analysis

The challenge provides a `haystack.tar.gz` archive which, when extracted, contains thousands of files.

1.  First, the archive must be fully extracted using `tar -xzvf haystack.tar.gz`.

2.  This creates a `haystack` directory filled with a large number of files, making manual inspection impossible.

3.  The `grep` command with the recursive (`-r`) flag is used to search the contents of all files within the `haystack` directory for the flag format.

    ```bash
    grep -r "OmahTIAcademy" haystack/
    ```

4.  The command returns a list of files containing fake flags and one file containing the real flag.

### Flag

OmahTIAcademy{F1nd1ng_A_N33dl3_In_A_Hayst4ck!}
