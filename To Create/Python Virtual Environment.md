## **Creating a Python Virtual Environment on Windows**

---

### **Step 1: Ensure Python is Installed**

Run the following command in **PowerShell** or **CMD** to check if Python is installed:

```sh
python --version
```

If Python is not installed, download and install it from [Python’s official website](https://www.python.org/downloads/).

### **Step 2: Navigate to Your Project Directory**

```sh
cd C:\Your\Project\Directory
```

### **Step 3: Create a Virtual Environment**

```sh
python -m venv "name of the virtual environment"
```

This will create a folder named `[name of the virtual environment]` inside your project directory.

### **Step 4: Activate the Virtual Environment**

**In PowerShell:**

```powershell
.\"name of the virtual environment"\Scripts\activate
```

**In CMD:**

```sh
"name of the virtual environment"\Scripts\activate
```

If you see an error about script execution, run:

```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned -Force
```

### **Step 5: Deactivate the Virtual Environment**

To exit:

```sh
deactivate
```

---

To learn more *about* Python Virtual Environment, [click here.]()
To *verify* that your Python is installed and works properly on your Windows machine, [click here.]()
