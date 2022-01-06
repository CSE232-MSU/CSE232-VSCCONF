# CSE232-VSCCONF

Recommended VSCode configurations for C++ debugging in CSE 232

Downloading these files can be done using the given `curl` commands. The `curl` (or, "cURL") program is a command-line tool used to transfer data from network protocols. This GitHub repository is simply a host for these configuration files.

## gdbinit

This is a GDB configuration file that skips over all STL code if a step-into is attempted. This is usually only a problem for Windows machines.

This will download the file to your home directory, and rename it to .gdbinit for GDB to discover.

```bash
curl -o ~/.gdbinit https://raw.githubusercontent.com/CSE232-MSU/CSE232-VSCCONF/main/gdbinit
```

## macos

Contains a launch.json and tasks.json file for C++ debugging on MacOS systems (`clang++`). Contains a single and multi-file configuration.

Execute the following commands one-by-one, after changing your directory to the folder where you want to debug some files:

```bash
mkdir .vscode
cd .vscode
curl --remote-name-all https://raw.githubusercontent.com/CSE232-MSU/CSE232-VSCCONF/main/macos/{launch.json,tasks.json,c_cpp_properties.json}
cd ..
```

This will create a .vscode folder if one doesn't exist, change directories to the .vscode folder, download the configuration files, and back out of the .vscode folder.

## windows

Contains a launch.json and tasks.json file for C++ debugging on Windows systems (`g++` with WSL). Contains a single and multi-file configuration.

Execute the following commands one-by-one, after changing your directory to the folder where you want to debug some files:

```bash
mkdir .vscode
cd .vscode
curl --remote-name-all https://raw.githubusercontent.com/CSE232-MSU/CSE232-VSCCONF/main/windows/{launch.json,tasks.json}
cd ..
```

This will create a .vscode folder if one doesn't exist, change directories to the .vscode folder, download the configuration files, and back out of the .vscode folder.
