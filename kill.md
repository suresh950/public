Step 1 — Create the script

Right-click Desktop → New → Text Document

Rename it to:

killapps.ps1

Right-click → Edit

Paste this:
```
Get-Process | Where-Object {$_.MainWindowTitle} | Stop-Process -Force
```

Save and close

This kills all user apps that have windows open (safe — avoids core system processes).


Step 2 — Create a one-click shortcut

Right-click Desktop → New → Shortcut

Paste this:
```
powershell.exe -ExecutionPolicy Bypass -File "C:\Users\YOURNAME\Desktop\killapps.ps1"
```

👉 Replace YOURNAME with your Windows username

Name it:

Kill All Apps


Done ✅

Double-click = instantly closes all open apps.

Optional: Add keyboard shortcut

Right-click the shortcut → Properties

Click Shortcut key

Press something like:

Ctrl + Alt + K

Apply
