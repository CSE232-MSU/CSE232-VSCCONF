# CSE232-VSCCONF

Recommended VSCode configurations for C++ debugging in CSE 232

Used by the CSE 232 website. [Repository for the website can be found here.](https://github.com/CSE232-MSU/CSE232)

Downloading these files can be done using the given `curl` commands. The `curl` (or, "cURL") program is a command-line tool used to transfer data from network protocols. This GitHub repository is simply a host for these configuration files.

Please use the configuration that corresponds to your operating system.

## MacOS

**Important**: requires that you have the CodeLLDB extension made by Vadim Chugunov.

Contains a launch.json, tasks.json, and c_cpp_properties.json file for C++ debugging on MacOS systems (`clang++` with `lldb`). Contains a single and multi-file configuration.

c_cpp_properties.json is included to set VSCode's C++ linting version to C++ 17. The linter will not default to the latest C++ version on MacOS, for whatever reason.

Execute the following commands one-by-one, after changing your directory to the folder where you want to debug some files:

```bash
mkdir .vscode
cd .vscode
curl --remote-name-all https://raw.githubusercontent.com/CSE232-MSU/CSE232-VSCCONF/main/macos/{launch.json,tasks.json,c_cpp_properties.json}
cd ..
```

This will create a .vscode folder if one doesn't exist, change directories to the .vscode folder, download the configuration files, and back out of the .vscode folder.

## Windows

Contains a launch.json and tasks.json file for C++ debugging on Windows systems with WSL (`g++` with `gdb`). Contains a single and multi-file configuration.

Execute the following commands one-by-one, after changing your directory to the folder where you want to debug some files:

```bash
mkdir .vscode
cd .vscode
curl --remote-name-all https://raw.githubusercontent.com/CSE232-MSU/CSE232-VSCCONF/main/windows/{launch.json,tasks.json}
cd ..
```

This will create a .vscode folder if one doesn't exist, change directories to the .vscode folder, download the configuration files, and back out of the .vscode folder.

GDB will step into C++ source code by default. To avoid this, I also recommend downloading the GDB configuration file below.

This will download the file to your home directory, and rename it to .gdbinit for GDB to discover. You should only need to download this file once unless it's removed.

```bash
curl -o ~/.gdbinit https://raw.githubusercontent.com/CSE232-MSU/CSE232-VSCCONF/main/gdbinit
```
