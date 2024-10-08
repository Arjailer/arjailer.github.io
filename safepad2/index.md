## SafePad 2

SafePad 2 is an encrypted text editor for 64-bit Windows.

It uses [AES256](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) encryption with [Argon2](https://en.wikipedia.org/wiki/Argon2) password hashing.

![SafePad 2 screenshot](SafePad2.png)

<br /><br />

---

<strong>SafePad v2.06</strong><br />
<sup>8 July 2024</sup>

[Download](https://github.com/Arjailer/arjailer.github.io/releases/download/SafePad-2/SafePad.2.Setup.exe)<br />
<sup>5.6 MB</sup>

_SafePad 2 needs [.NET Desktop Runtime 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0#runtime-desktop-8.0.2) on Windows 10 version 1809 or later_

<br /><br />

<strong>Windows SmartScreen</strong><br />
<sub>Note that due to the costs involved the SafePad 2 installer is unsigned, and therefore running the installer will probably trigger <strong>Windows SmartScreen</strong>.</sub><br />
<sub>Depending how Windows is configured you may have to click <strong>More Info</strong> then <strong>Run Anyway</strong> to start the installer, or it may block the installer entirely.</sub><br />
<sub>If this happens you can unblock the installer by running the following command in PowerShell:</sub><br />
<code>Unblock-File "$((New-Object -ComObject Shell.Application).NameSpace('shell:Downloads').Self.Path)\SafePad.2.Setup.exe"</code>

<strong>Updating with older versions</strong><br />
<sub>Note that SafePad versions prior to 2.06 will no longer automatically find updates. This is because Microsoft changed the link format for OneDrive meaning the link that older versions of SafePad 2 used to check for updates no longer works. Version 2.06 onward use a new link hosted here at arjailer.uk</sub>

<strong>.NET Framework 4.7.2</strong><br />
<sub>[SafePad v2.05](https://github.com/Arjailer/arjailer.github.io/releases/download/SafePad-2-dotnet-4/SafePad.2.Setup.v2.05.exe) was the last version that used [.NET Framework 4.7.2](https://dotnet.microsoft.com/download/dotnet-framework) and runs on 64-bit Windows 7 service pack 1 or later</sub>

<sup>_Note that to downgrade from a later version you should uninstall the later version before installing the earlier version_</sup>
