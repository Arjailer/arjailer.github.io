## Grind

[Download Grind v1.17](https://github.com/Arjailer/arjailer.github.io/releases/download/Grind-1.17/Grind.Setup.exe) (22 July 2019, ~4.5MB)

[What's new in this version?](#history)

_Grind needs .NET Framework 4.5.2 on Windows 7 or later_

---

<br />

Grind is a grep _(global / regular expression / print)_ tool for Windows.

I started writing it in early 2012 from a desire for a simple, fast, effective grep tool, primarily for my own use. I also wanted to put some of the technologies I'd been learning into practice _(things like WPF MVVM, the Managed Extensibility Framework, the Task Parallel Library, and Async / Await)_.

I have vague plans to make Grind open source one day ... but no promises ...

![Grind screenshot](Grind1.png)

<br />

---

<a name="history"></a>

### Grind version history

**v1.17**  (22 July 2019) 
- **(changed)**  Increased text file maximum line length from 5000 to 9600 to match AvalonEdit's maximum line length. Above this files are displayed with the binary file viewer instead. 
- **(changed)**  Binary files no longer try to display Line or Character counts in those columns. 
- **(changed)**  Selection highlighting size limit options are now also applied to word highlighting. 
- **(changed)**  Now uses a more memory efficient method for loading text files into the text viewer. 
- **(changed)**  Updated all third party components to the latest versions. 
- **(fixed)**  Unexpected errors while gathering files would crash the application. They are now reported in the Search Errors tab. 

**v1.16**  (3 July 2019) 
- **(fixed)**  Incorrect detection of newline characters during replace. Introduced in v1.15 encoding detection changes. 

**v1.15**  (1 July 2019) 
- **(new)**  Results list columns can now be re-ordered or hidden, either by right-clicking on the column headers, or by dragging the column headers in the list. 
- **(new)**  Showing the whole file path in the results list can now be toggled on and off, either in Options > Results, or by right-clicking on the column headers. 
- **(new)**  New hotkey for overriding the "allow multiple instances" option while starting Grind. Hotkeys can be customised by right-clicking on the tray icon and selecting Options. 
- **(changed)**  Roughly 30% improvement in Normal and Extended search speeds due to more efficient string comparisons. 
- **(fixed)**  Text files with extremely long lines (over 5000 characters) would display extremely slowly, often seeming to never finish. This was due to limitations in the AvalonEdit text control, so these files are now displayed with the binary file viewer instead. 
- **(fixed)**  Crash if the detected file encoding was not supported by the Windows installation (e.g. Big-5 traditional Chinese character encoding on English installations). Now uses UTF-8 as a fallback. 
- **(fixed)**  Minor bug fixes and stability improvements. 

**v1.14**  (28 May 2019) 
- **(fixed)**  Crash loading old settings files. 

**v1.13**  (23 May 2019) 
- **(new)**  Added Ctrl+W shortcut to close the main window. 
- **(changed)**  Improved restoring of window positions. 
- **(changed)**  Improved appearance of disabled buttons. 
- **(changed)**  Improved formatting of file and match counts. 
- **(fixed)**  File encoding would sometimes be detected incorrectly. 
- **(fixed)**  Files that were deleted between finding and searching would crash the search due to missing file size. 
- **(fixed)**  Hardened the drag/drop code to cope with COMExceptions. 

**v1.12**  (4 December 2018) 
- **(new)**  Use system proxy settings when checking for updates. 
- **(fixed)**  Improved detection of clean vs update installs. 
- **(fixed)**  Improved closing of running tray app when installing or uninstalling. 
- **(fixed)**  On Windows 10 the taskbar button would always appear on the primary monitor regardless of which monitor the main window was restored to. 

**v1.11**  (7 September 2018) 
- **(new)**  Can search for words in the current file with Alt+click, or right-click > "search for selected text in the current file". To accommodate this the Google shortcut has changed to Ctrl+Alt+click. 
- **(new)**  Added Notepad++ 64-bit and the new Visual Studio Code user installation as predefined text editors in Options > Results > Change text editor > Predefined 
- **(changed)**  Tidied up the way blank lines are handled in the Matches Only view. 
- **(changed)**  Positions in binary files are now reported in hex in the status bar, to match the viewer. 
- **(fixed)**  Moving the caret off the end of a very small binary file caused a crash. 

**v1.10**  (2 July 2018) 
- **(changed)**  Reduced the maximum number of threads used for searching. Has very little impact on search speed, but avoids locking the system when searching multiple large files. 
- **(changed)**  Added large file handling to the command line options. 
- **(fixed)**  Command line crashed due to bad implementation of large file size option. 
- **(fixed)**  Double-clicking an item before it was ready could cause a crash. 

**v1.09**  (10 January 2018) 
- **(fixed)**  Fixed layout of ribbon on high-dpi Windows 10. 

**v1.08**  (9 November 2017) 
- **(fixed)**  Crashed on startup from a clean install. 

**v1.07**  (10 October 2017) 
- **(changed)**  Added high dpi icons for tray app. 

**v1.06**  (5 October 2017) 
- **(changed)**  Changed icons to a more modern "flat" style. 
- **(fixed)**  Improved restoring maximized windows in multi-monitor setups. E.g. a window maximized on monitor 2 would often jump to monitor 1 when minimized or un-maximized. 

**v1.05**  (20 September 2017) 
- **(new)**  Added warning when search includes large files. Can chose to search the large files, exclude them, or stop the search. Default size is 250MB, which can be changed in Options > Search > Large files. 
- **(changed)**  Improved the handling of large files.
The text viewer now reports when files are too large to display instead of just crashing. The text viewer has to load the entire file before it can be displayed, which restricts the size of files it can display. The largest text file successfully searched and displayed on 64-bit Windows was 900MB (which took 15 seconds to search for a three character match, and another 30 seconds to load and display the contents). Larger files will be searched, but not displayed in Grind.
The binary viewer pages the file into memory as you scroll, so it can display much larger files. The largest binary file successfully searched and displayed on 64-bit Windows was 34GB (which took 1 hour 20 minutes to search for a three character match, and then displayed the contents almost instantly). 
- **(fixed)**  Crashed when displaying a file identified as text which contained mixed line-breaks (CR/LF/CRLF). 

**v1.04**  (6 September 2017) 
- **(new)**  Can now invert search matches, so that only files which do NOT match the specified criteria are listed. 
- **(new)**  Can change the text font and size for displaying file contents in Options > View. 
- **(new)**  Shows the current line in the scrollbar. Can be disabled in Options > Scrollbar. 
- **(new)**  Can copy filenames and locations of all ticked files to the clipboard. 
- **(fixed)**  Sometimes double-clicking on a file would open the wrong file. 
- **(fixed)**  Crashed occasionally if moving through matches too quickly (e.g. with Ctrl+Left or Ctrl+Right). 
- **(fixed)**  Would go into an infinite loop if a regex search returned zero-length matches. 

**v1.03**  (15 August 2017) 
- **(new)**  Can now optionally search and view binary files. See the help for limitations. 
- **(new)**  Added filter tab allowing searched files to be filtered by size and modified date. Tab is coloured when a filter is set. 
- **(changed)**  Replaced the ribbon control with a more modern version. 
- **(changed)**  Simplified scrollbar styling to make match highlights easier to see. 
- **(changed)**  Can now control the shell extension from the tray app options. 
- **(changed)**  Added extended search mode and the new file size and modified date filters to the command line options. 
- **(changed)**  Updated all third party components to the latest versions. 
- **(fixed)**  Positioning of scrollbar match highlights is now more accurate. 
- **(fixed)**  Multi-line scrollbar match highlights are now sized correctly. 
- **(fixed)**  Multiple find in file matches on the same line would sometimes not highlight correctly. 
- **(fixed)**  Grind would hang if large text selections were made with the selected text highlighting option enabled. Avoided by adding a maximum selection size option. 
- **(fixed)**  Installer now checks for .NET 4.5.2 

**v1.02**  (10 May 2017) 
- **(fixed)**  Fixed build issue that was causing incorrect plugin versions to be distributed. 

**v1.01**  (10 May 2017) 
- **(new)**  Can now search within the displayed file's contents by using the "find in file" box (Ctrl+F). Results are highlighted in green. Navigate with Ctrl+up and Ctrl+down. See the help for more details. 
- **(new)**  Can search Google for words by holding the Alt key and clicking on the word to search for, or by selecting some text, right-clicking and selecting "search Google for selected text". 
- **(new)**  Locations of highlighted words and selections are now shown in the scrollbar. 
- **(new)**  Notification tray app now checks for updates and has a proper About box. 
- **(new)**  Added update notification pop-ups. Click the pop-up to download the update. 
- **(fixed)**  Improved handling and reporting of registry writing errors. Particularly useful if your anti-virus program has started blocking writes to the registry keys required for running Grind in the notification tray at startup. 
- **(changed)**  Updated all third party components to the latest versions. 
- **(changed)**  Grind now requires .NET 4.5.2 

**v1.00**  (17 March 2017) 
- **(new)**  Added extended search and replace engine which can handle new lines at the end of lines (e.g. "end\r\n") and tabs within a line (e.g. "\t\tstart"). Extended replace can remove new lines (e.g. replacing "end\r\n" with just "end") or insert new lines (e.g. replacing "end" with "end\r\n"). Note that searches are still confined to a single line, so new lines in the middle of a search term (e.g. "end\r\nstart") will not be found. 
- **(new)**  Regex search and replace can now handle new lines and tabs too. 
- **(new)**  Can drag all found files into other applications, such as Visual Studio or Explorer, by dragging the Matches tab header. 
- **(new)**  Can drag all ticked files by dragging the tick column header. 
- **(fixed)**  Word highlighting didn't work if the word was the entire line. 
- **(fixed)**  Searching files less than 2 bytes long would crash trying to determine if the file ended with a new line. 
- **(changed)**  Now only checks for updates on startup once an hour. 
- **(changed)**  Updated the help file. 

**v0.27**  (3 February 2017) 
- **(new)**  Can limit search to tick files only by selecting "search ticked files" on ribbon. 
- **(new)**  Can search for selected text by selecting some text, right-clicking and selecting "search for selected text" or "search for selected text in ticked files". 
- **(new)**  Can search for words by holding the Ctrl key and clicking on the word to search for. Hold Shift+Ctrl to search in tick files only. 
- **(new)**  Word highlighting. Click on a word to highlight all occurrences throughout the document. Can be disabled in Options > View 
- **(new)**  Selection highlighting. Select some text to highlight all occurrences throughout the document. Can be disabled in Options > View 
- **(new)**  Added Sublime Text 3 and Visual Studio Code as predefined text editors in Options > Results > Change text editor > Predefined 
- **(fixed)**  Added missing third party acknowledgements in About > Third Party Components 
- **(changed)**  Updated all third party components to the latest versions. 

**v0.26**  (30 January 2017) 
- **(fixed)**  Forgot to add ShellLib to the installer - fixed now. 

**v0.25**  (30 January 2017) 
- **(fixed)**  Matches at the very beginning of lines weren't being highlighted. 
- **(fixed)**  Removed the line number highlighter as it is no longer required. 

**v0.24**  (27 January 2017) 
- **(new)**  Shell extension menu options are now available when right-clicking on a file (e.g. source control, virus scanner etc) 
- **(new)**  Line numbers are now shown in their own area to the left of the file contents. Removes the need for hacks to deal with the cursor being in the line number area and looks neater. 
- **(new)**  Cursor position is now shown at the bottom-right of the screen. 

**v0.23**  (11 January 2017) 
- **(fixed)**  Navigating forwards caused crash if no file selected. 
- **(fixed)**  Alt+tab would show an icon for the notification tray icon. 

**v0.22**  (22 June 2016) 
- **(new)**  Search history. Added back and forward buttons to navigate through history. Right-click the buttons to see the history. Pre-requisite for starting searches based on selected text, which was added in 0.27 
- **(new)**  Single instance option. Allowing multiple instances can be disabled in the Grind and tray options. 
- **(fixed)**  Replaces being one character out on the first line of a UTF encoded file. 
- **(fixed)**  ArgumentOutOfRangeException when switching between Whole File and Matches Only after a Replace. 

**v0.21**  (19 May 2016) 
- **(fixed)**  In-application updating now gives more control to the user during the installation. Was previously overly aggressive in automatically closing applications during the installation. The first update to 0.21+ is still aggressive, but it should be better from then on. 

**v0.20**  (5 May 2016) 
- **(new)**  Added command line interface, which exports results to a tab separated file. Get help with Grind.CommandLine.exe /? 

**v0.19**  (15 April 2016) 
- **(changed)**  Overhauled the update system. Checks for updates at startup. Update release notes can be viewed prior to downloading. Updates can be downloaded and installed with a single click. 
- **(changed)**  Overhauled the error reporting system. Error reports are now logged directly in the bug tracking system, rather than by email. 

**v0.18**  (28 March 2016) 
- **(fixed)**  Crash at startup if PATH environment variable included quoted entries. 
- **(fixed)**  Reinstated support for UNC search paths. Was inadvertently broken when Pri.LongPath was introduced in v0.16 

**v0.17**  (23 March 2016) 
- **(new)**  Notification tray icon that enables global hotkeys for running Grind (Windows+G), running with the current selected text (Windows+S), or running with the current clipboard text (Windows+K). The tray icon is enabled during installation or in Options > General > Integration. Hotkeys can be customised by right-clicking on the tray icon and selecting Options. 
- **(new)**  Customise syntax highlighting file extensions in Options > File Contents. 
- **(changed)**  Simplified how the Match Case and Match Whole Word options are handled. Makes no difference to the user, but makes the code easier to maintain. 

**v0.16**  (29 October 2015) 
- **(new)**  Syntax highlighting of SQL files. 
- **(fixed)**  Error when searching long directory paths. Now uses Pri.LongPath for all path operations. 
- **(changed)**  Attachments are now zipped when emailing error reports. 

**v0.15**  (6 September 2015) 
- **(fixed)**  Crash when retrieving file icons in Windows 10. 

**v0.14**  (30 August 2015) 
- **(new)**  Switching between "whole file" and "matches only" now retains the current cursor position as closely as possible. 
- **(fixed)**  Error when trying to search UNC paths. 
- **(changed)**  Updated installer .NET check to accommodate .NET 4.6 

**v0.13**  (10 July 2015) 
- **(new)**  Can now use Ctrl+Left and Ctrl+Right to navigate to previous and next matches. 
- **(fixed)**  Now retains existing newlines at the end of files during replace. Previously these were removed. 

**v0.12**  (4 September 2014) 
- **(new)**  Added regular expression builder buttons with quick links to common regular expression elements. 
- **(new)**  Changed "exclude extension" to a more general "exclusions" option, which allows file and folder masks using ? and * wildcards. Set in Options > Search > Exclusions 
- **(fixed)**  Interface update routines could sometimes be called from the wrong thread. 

**v0.11**  (6 June 2014) 
- **(new)**  Replace now supports regular expression replacing. 
- **(new)**  Files for replacing can be selected or un-selected using the tick boxes. Click or right-click on the column header to tick or un-tick all items at once. 
- **(new)**  Next/previous match buttons now move to the next/previous file at the last/first match. Can be disabled in the Options screen. 
- **(new)**  Moved the match navigation controls to just above the file contents. Less mouse movement required when navigating through matches. 
- **(new)**  Syntax highlighting of Visual Basic and Python files. 
- **(changed)**  Updated all third party components to the latest versions. 

**v0.10**  (24 April 2014) 
- **(new)**  Replace text now has history. 
- **(fixed)**  Now retains file encoding and new line style during replace. Previously turned all replaced files into UTF-8 with CRLF new lines. 
- **(fixed)**  Detects and disallows regular expression searches that match all characters, such as "dog||cat". 
- **(fixed)**  Detects and reports folders that are too long (maximum of 248 characters). 
- **(fixed)**  Limited thread creation when searching network drives. Appears to improve search performance. 

**v0.09**  (5 April 2014) 
- **(new)**  Can now replace matches with a simple literal replace function. 
- **(new)**   Can perform "whole word only" searches. 
- **(new)**  Made "match case" and "match whole word only" options available on the ribbon interface. 
- **(fixed)**  Opening file in text editor would not find correct line in "matches only" mode. 
- **(fixed)**  The "context lines" option wasn't being saved correctly. 
- **(changed)**  Increased the text box history drop-downs to 20 items (was 10 before). 
- **(changed)**  Consolidated the built-in plug-ins into a single assembly. 

**v0.08**  (12 March 2013) 
- **(new)**  Can now search directly from the ribbon interface. Change search options in Options > Search. Alt+S, Alt+M and ALt+F to jump to search boxes. Old search dialog is available as advanced search. Menu and toolbar interface is as it was before. 
- **(fixed)**  Occasional timing/ordering problems at start-up on Windows 8. 
- **(changed)**  Stop search shortcut changed to Ctrl+Break (the old Ctrl+X shortcut would cut selected text from the search boxes). 
- **(changed)**  Start-up speed improvements. 

**v0.07**  (8 February 2013) 
- **(new)**  Can drag files from the results list into other applications, such as Visual Studio, Notepad++, Explorer etc. 
- **(changed)**  Now stores settings in a SQLite database. This reduces some of the oddities that could be seen when running multiple instances and changing settings in each. Imports existing settings into the database on first run. 
- **(changed)**  Improved reporting (in the search dialog) of the reasons why search criteria might be invalid (such as a previously searched folder no longer existing). 

**v0.06**  (8 October 2012) 
- **(new)**  Can switch between the ribbon interface and a more traditional menu and toolbar interface. 
- **(new)**  Can specify a custom text editor to open files in within the Options screen. 
- **(new)**  Can navigate matches with just the cursor keys when focus is on the results list. Up and Down move between files, Left and Right move between matches within a file. 
- **(new)**  Copied text now excludes the lines numbers added by Grind. 
- **(new)**  Syntax highlighting of Pascal/Delphi files. 
- **(fixed)**  Repeating a search on a now invalid location caused an unhandled error. 

**v0.05**  (23 August 2012) 
- **(new)**  Added shell extension. Can now start a search by right-clicking on a folder and selecting "Search with Grind". 
- **(new)**  Added splash screen to give more immediate feedback that Grind is in fact launching. 
- **(changed)**  Start-up speed improvements. 
- **(changed)**  Scrolling through results list no longer shows each file as it goes along. Results in faster scrolling and less disc reading. 
- **(changed)**  Tidied up the ribbon interface a bit. 

**v0.04**  (16 July 2012) 
- **(new)**  Added Options screen. 
- **(new)**  Shows matches in the scrollbar. Can be disabled in the Options screen. 
- **(fixed)**  Search could sometimes fail due to threading issues while loading internal resources. 

**v0.03**  (26 June 2012) 
- **(new)**  Recently used criteria files are listed in the ribbon menu. 
- **(fixed)**  Failed to open files in Notepad. 
- **(fixed)**  Searches did not complete under certain circumstances. 
- **(changed)**  Moved log files from installation folder to profile folder. 
- **(changed)**  Improved catching and logging of errors during searching. 

**v0.02**  (13 June 2012) 
- **(new)**  Shows first match when file is selected. 
- **(new)**  Buttons to move to first, last, next and previous matches. 
- **(new)**  Save and load search criteria to and from file. 
- **(fixed)**  Copying filename or location to clipboard could sometimes lock the app. 
- **(fixed)**  Highlighting adjacent matches didn't always work. 
- **(changed)**  Optimised highlighting logic - much faster with thousands of matches. 

**v0.01**  (29 April 2012) 
- **(new)**  Initial release 
