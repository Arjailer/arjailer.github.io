## Grind

Grind is a visual grep tool for Windows.

I started writing it in early 2012 as a simple, fast search tool for my own use. It's become quite popular amongst the developers where I work, and I still work on it from time to time.

![Grind screenshot](Grind1.png)

---

<strong>Grind v1.55</strong><br />
<sup>31 July 2024</sup>

[Download installer](https://github.com/Arjailer/arjailer.github.io/releases/download/Grind/Grind.Setup.exe)<br />
<sup>11.4 MB</sup>
<br />
[Download zip](https://github.com/Arjailer/arjailer.github.io/releases/download/Grind/Grind.zip)<br />
<sup>15.2 MB</sup>
<br />

_Grind needs [.NET Desktop Runtime 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0#runtime-desktop-8.0.2) on Windows 10 version 1809 or later_

<br /><br />

<strong>Windows SmartScreen</strong><br />
<sub>Note that due to the costs involved the Grind installer is unsigned, and therefore running the installer will probably trigger <strong>Windows SmartScreen</strong>.</sub><br />
<sub>Depending how your Windows is configured this may have to click <strong>More Info</strong> then <strong>Run Anyway</strong> to get the installer to start, or it may block the installer from running entirely.</sub><br />
<sub>If this happens you can either try the zip version, or you can unblock the installer by running the following commands in PowerShell:</sub><br />
<code>cd $Env:HOMEPATH\Downloads</code><br />
<code>Unblock-File Grind.Setup.exe</code>
<sub></sub>

<strong>Updating with older versions</strong><br />
<sub>Note that Grind versions prior to 1.54 will no longer automatically find updates. This is because Microsoft changed the link format for OneDrive meaning the link that older versions of Grind used to check for updates no longer works. Version 1.54 onward uses a new link hosted here at arjailer.uk</sub>

<strong>.NET Framework 4.8</strong><br />
<sub>[Grind v1.41](https://github.com/Arjailer/arjailer.github.io/releases/download/Grind-dotnet-4/Grind.Setup.v1.41.exe) was the last version that used [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework) and runs on Windows 7 service pack 1 or later</sub>

<sup>_Note that to downgrade from a later version you should uninstall the later version before installing the earlier version_</sup>
