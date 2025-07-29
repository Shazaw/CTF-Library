# Solution: Vacation Spot

**Category:** OSINT
**Points:** 750

---

### Analysis

The goal is to find the precise geographic coordinates for the location shown in `VacationSpot.jpeg`.

1.  A reverse image search using Google Lens on the provided picture suggests the location is **Ilulissat, Greenland**, specifically the Ilulissat Icefjord.

    <img width="649" height="243" alt="image" src="https://github.com/user-attachments/assets/5b930e87-4702-4076-8a25-76d1a1fb9208" />


2.  With this information, the next step is to explore the Ilulissat Icefjord area on Google Maps, looking for a Photo Sphere or Street View that matches the challenge image.

3.  A matching Photo Sphere is found, taken by photographer Jannik Kappel. The URL for this specific view contains the high-precision coordinates: `69.2005715,-51.1253647`.

    <img width="787" height="400" alt="image" src="https://github.com/user-attachments/assets/4adcaf25-d60b-4c02-b635-e4bd40c7f242" />


4.  The challenge requires the coordinates to be formatted to two decimal points.

### Flag

OmahTIAcademy{69.20,-51.12}
