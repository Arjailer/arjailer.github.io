## SafePad 2

[Download SafePad v2.04](https://github.com/Arjailer/arjailer.github.io/releases/download/SafePad-2/SafePad.2.Setup.exe)
<br />
(30 August 2019, ~2MB)

[What's new in this version?](#history)

_SafePad 2 needs [.NET Framework 4.7.2](https://dotnet.microsoft.com/download) or later, on 64-bit Windows 7 or later_

---

<br />

SafePad 2 is an encrypted text editor for 64-bit Windows.

It uses [AES256](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) encryption with [Argon2](https://en.wikipedia.org/wiki/Argon2) password hashing.

![SafePad 2 screenshot](SafePad2.png)

<br />

---

<a name="history"></a>

### SafePad 2 version history

_**From v2.04 onwards SafePad 2 will be 64-bit only**_

**v2.04**  (30 August 2019) 
- **(changed)**  Replaced PBKDF2 password hashing with Argon2.

**v2.03**  (22 July 2019) 
- **(changed)**  Minor changes to icons and the installer. 

**v2.02**  (24 May 2019) 
- **(fixed)**  Added clickable links option. 

**v2.01**  (22 May 2019) 
- **(new)**  Added opening files from the command line. 
- **(new)**  Added message about upgrading v1 files to v2. 
- **(fixed)**  Reduced flickering at startup. 
- **(fixed)**  v1 files were upgrading with 1 password round. Now uses the default number of rounds. 
- **(fixed)**  Some icons were blurry. 

**v2.00**  (19 May 2019) 
- **(new)**  Initial release 
