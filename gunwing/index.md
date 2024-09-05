## Gun Wing

Gun Wing is a simple little shoot-em-up for Windows that I wrote in [Blitz3D](https://blitzresearch.itch.io/blitz3d) in my spare time back in 2007.

It didn't turn out to be as much fun as I'd hoped but I learned a lot writing it.

![Gun Wing screenshot](GunWing1.jpg)

<br /><br />

---

<strong>Gun Wing v1.1</strong><br />
<sup>February 2007</sup>

[Download](https://github.com/Arjailer/arjailer.github.io/releases/download/GunWing/GunWing.Setup.exe)<br />
<sup>6 MB</sup>

_Gun Wing itself should run on anything from Windows 95 onward, but the installer only supports Windows XP or later_

<br /><br />

<strong>Windows SmartScreen</strong><br />
<sub>Note that due to the costs involved the Gun Wing installer is unsigned, and therefore running the installer will probably trigger <strong>Windows SmartScreen</strong>.</sub><br />
<sub>Depending how Windows is configured you may have to click <strong>More Info</strong> then <strong>Run Anyway</strong> to start the installer, or it may block the installer entirely.</sub><br />
<sub>If this happens you can unblock the installer by running the following command in PowerShell:</sub><br />
<code>Unblock-File "$((New-Object -ComObject Shell.Application).NameSpace('shell:Downloads').Self.Path)\GunWing.Setup.exe"</code>
