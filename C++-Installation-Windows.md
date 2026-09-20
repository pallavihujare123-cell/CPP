# C++ Installation & Setup on Windows

## 1. Introduction

This document contains the steps I followed to install and configure C++ on Windows for learning C++ and Data Structures & Algorithms.

### Tools Used

* Windows
* VS Code
* MSYS2
* GCC / G++
* Git & GitHub

---

# 2. Install MSYS2

MSYS2 provides the GCC compiler needed to compile C++ programs on Windows.

Download MSYS2 from:

https://www.msys2.org/

Install it using the default location:


C:\msys64


---

# 3. Open MSYS2 UCRT64

After installation, open:


MSYS2 UCRT64
```

Do not use normal PowerShell for the MSYS2 package installation commands.

The terminal looks similar to:


Hp@LAPTOP UCRT64 ~
$
```

---

# 4. Update MSYS2

Run:


pacman -Syu
```

If it asks for confirmation:


Proceed with installation? [Y/n]
```

Enter:

Y
```

If the terminal asks you to close and reopen MSYS2, do that and run the update command again if required.

---

# 5. Install GCC / G++

Install the C++ compiler using:


pacman -S mingw-w64-ucrt-x86_64-gcc
```

Press `Y` when confirmation is requested.

---

# 6. Check G++ Installation

Inside the MSYS2 UCRT64 terminal, run:


g++ --version
```

Expected result:

g++.exe (Rev3, Built by MSYS2 project) 16.2.0
```

The exact version may change over time.
If a GCC/G++ version is displayed, the compiler is installed successfully.

---

# 7. Check the Compiler Location

The compiler is installed inside:

```text
C:\msys64\ucrt64\bin
```

The G++ executable is:

```text
C:\msys64\ucrt64\bin\g++.exe
```

To check this in PowerShell:

```powershell
Test-Path "C:\msys64\ucrt64\bin\g++.exe"
```

Expected result:

```text
True
```

---

# 8. Add G++ to PATH

To use `g++` from VS Code PowerShell, add the following folder to the Windows PATH:

```text
C:\msys64\ucrt64\bin
```

### Steps

1. Search Windows for `Environment Variables`.
2. Open `Edit the system environment variables`.
3. Click `Environment Variables`.
4. Under User Variables, select `Path`.
5. Click `Edit`.
6. Click `New`.
7. Add:

```text
C:\msys64\ucrt64\bin
```

8. Click `OK` on all windows.
9. Restart VS Code.

---

# 9. Verify G++ in VS Code

Open VS Code and create a new terminal.

Run:

```powershell
g++ --version
```

If the version is displayed, the compiler is available from VS Code.

---

# 10. Create the First C++ Program

Create a file:

```text
hello.cpp
```

Code:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, C++!";
    return 0;
}
```

---

# 11. Compile the Program

Open the VS Code terminal in the folder containing `hello.cpp`.

Run:

```powershell
g++ hello.cpp -o hello
```

If there are no errors, an executable file will be created:

```text
hello.exe
```

---

# 12. Run the Program

Run:

```powershell
.\hello.exe
```

Output:

```text
Hello, C++!
```

---

# 13. Basic C++ Workflow

The basic workflow is:

```text
Write Code
    ↓
Save .cpp file
    ↓
Compile using g++
    ↓
Create .exe file
    ↓
Run the program
    ↓
Check Output
```

Example:

```text
hello.cpp
    ↓
g++ hello.cpp -o hello
    ↓
hello.exe
    ↓
.\hello.exe
```

---

# 14. Common Commands

### Check compiler

```bash
g++ --version
```

### Compile

```bash
g++ filename.cpp -o filename
```

### Run

```powershell
.\filename.exe
```

### Check compiler path

```powershell
Test-Path "C:\msys64\ucrt64\bin\g++.exe"
```

---

# 15. Common Problem

### Error

```text
g++ : The term 'g++' is not recognized
```

### Possible reason

The compiler may be installed, but the compiler folder is not available in the Windows PATH.

Check:

```text
C:\msys64\ucrt64\bin\g++.exe
```

If the file exists, add:

```text
C:\msys64\ucrt64\bin
```

to the Windows PATH and restart VS Code.

---

# 16. My Setup Status

```text
MSYS2              ✅ Installed
GCC/G++             ✅ Installed
G++ Compiler        ✅ Working
VS Code             ✅ Configured
C++ Environment     ✅ Ready
```
