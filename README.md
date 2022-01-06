# CSE232-VSCCONF
Recommended VSCode configurations for C++ debugging in CSE 232

## .gdbinit

This .gdbinit file skips over all STL code if a step-into is attempted. This is usually only a problem for Windows machines.

This will automatically be downloaded to your home directory (where GDB looks for a .gdbinit file).

```bash
curl -o ~/.gdbinit https://raw.githubusercontent.com/CSE232-MSU/CSE232-VSCCONF/main/.gdbinit
```

## .vscode_macos

Contains a launch.json and tasks.json file for C++ debugging on MacOS systems (`clang++`). Contains a single and multi-file configuration.

Navigate to the folder where you want to debug. Make a .vscode folder if one doesn't exist:

```bash
mkdir .vscode
```

Change directory to the .vscode folder:

```bash
cd .vscode
```

Then use:

```bash
curl --remote-name-all https://raw.githubusercontent.com/CSE232-MSU/CSE232-VSCCONF/main/.vscode_macos/{launch.json,tasks.json}
```

## .vscode_windows

Contains a launch.json and tasks.json file for C++ debugging on Windows systems (`g++` with WSL). Contains a single and multi-file configuration.

Navigate to the folder where you want to debug. Make a .vscode folder if one doesn't exist:

```bash
mkdir .vscode
```

Change directory to the .vscode folder:

```bash
cd .vscode
```

Then use:

```bash
curl --remote-name-all https://raw.githubusercontent.com/CSE232-MSU/CSE232-VSCCONF/main/.vscode_windows/{launch.json,tasks.json}
```
