## **Creating a System-Wide Alias to activate a virtual environment in CMD and PowerShell**

---

### **Method 1: Create a Batch File Alias (Works in CMD)**

1. Open **Notepad** and add the following:
   ```bat
   @echo off
   call C:\Your\Project\Directory\NameOfTheVirtualEnvironmentDirectory\Scripts\activate
   ```
2. Save it as `NameOfTheAlias.bat` in `C:\Your\Directory\For\Aliases\`.
3. Add `C:\Your\Directory\For\Aliases\` to the **System Path**:
   - Open **System Environment Variables** (`sysdm.cpl` → Advanced → Environment Variables → Edit `Path`).
   - Add `C:\Your\Directory\For\Aliases\`.
4. Restart CMD and test:
   ```sh
   NameOfTheAlias
   ```

### **Method 2: Create a PowerShell Function (Works in PowerShell)**

1. Open PowerShell and run:
   ```powershell
   notepad $PROFILE
   ```
2. Add the following function:
   ```powershell
   function NameOfTheAlias { & "C:\Your\Project\Directory\NameOfTheVirtualEnvironmentDirectory\Scripts\Activate.ps1" }
   ```
3. Save the file and reload the profile:
   ```powershell
   . $PROFILE
   ```
4. Now, simply run:
   ```powershell
   NameOfTheAlias
   ```

If your alias works in CMD but not in PowerShell, it is because PowerShell does not use the same alias system as CMD. PowerShell does not recognize batch file aliases added via the Path environment variable the same way CMD does.
If you want an alias to function on both CMD and Powershell, you must use the same name when creating it for both.

If you want to know more *about* Aliases, [click here.]()

---
