# Solution: A beginner's first website

**Category:** OSINT
**Points:** 500

---

### Analysis

This challenge involves finding a security vulnerability related to a developer named `RandomGuyChilling`.

1.  The primary lead is the username. A search on GitHub for this username leads to the profile `https://github.com/RandomGuyChilling`.

2.  The profile has one repository named `FirstProject`. Inspecting the code reveals a login page. A comment in the code indicates that the password was recently deleted for security reasons.

3.  The key to solving this is to investigate the **commit history** of the repository. The history shows a previous version of the code where the password was hardcoded. This commit reveals the flag.

    <img width="783" height="76" alt="image" src="https://github.com/user-attachments/assets/ec9c02ef-f04c-4204-888e-37fa6824f1a0" />


### Flag

OmahTIAcademy{You_sh0u1d_n3vEr_puT_Cr3d5_1n_pUBL1c_G1thUb}
