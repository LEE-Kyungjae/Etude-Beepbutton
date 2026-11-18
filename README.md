# Etude-Beepbutton

**Etude-Beepbutton** is a small Windows dialog program that plays short beep patterns.
It is meant to be used alongside click macros: a macro can click one of the buttons
to get audible confirmation that a step was reached.

## Features

- **Low button (낮음)**: two short 200 Hz beeps (80 ms each).
- **High button (높음)**: a 500 Hz / 300 Hz / 500 Hz pattern (100 ms each).
- Large buttons that are easy for a click macro to target.
- Native Win32 executable with no runtime besides the Visual C++ / MFC redistributable.

The beep patterns are set in `MFCApplication2/MFCApplication2Dlg.cpp`
(`OnBnClickedButtonsoundbeeplow` and `OnBnClickedButtonsoundbeephigh`) and can be
changed by editing the `Beep(frequency, duration)` calls.

## Requirements

- Windows
- Visual Studio 2022 with the **Desktop development with C++** workload and the
  **C++ MFC for latest build tools** component (platform toolset `v143`)

## Build

1. Clone the repository:
   ```bash
   git clone https://github.com/LEE-Kyungjae/Etude-Beepbutton.git
   cd Etude-Beepbutton
   ```
2. Open `MFCApplication2.sln` in Visual Studio and build (`Debug` or `Release`, `x86` or `x64`),
   or build from a Developer Command Prompt:
   ```bat
   msbuild MFCApplication2.sln /p:Configuration=Release /p:Platform=x64
   ```
3. Run the built `MFCApplication2.exe` (for example `x64\Release\MFCApplication2.exe`).
