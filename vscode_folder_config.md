## Step 1 - C/C++ Edit Configurations (UI)

1. shift+cmd+P - open command pallet and select C/C++ Edit Configurations (UI)
2. Compiler path - /usr/bin/g++
3. C++ standard - select c++17
4. Save
5. .vscode/c_cpp_properties.json is created

## Step 2 - Setup Build Task

1. Select main.cpp from project tree
2. Select Filemenu >> Terminal >> Configure Default Build Task
3. Select C/C++: g++ build active file
4. tasks.json is created in .vscode folder
5: Add the missing args to "args":
    "args": [
				"-fdiagnostics-color=always",
				"-g",
				"-Wall",
				"-std=c++17",
				"${fileDirname}/*.cpp",
				"-o",
				"${fileDirname}/${fileBasenameNoExtension}"
			],
6. Now Build main.cpp Shift+CMD+B
7. Compiled Main file appears in project tree.
8. Right click on compiled Main, select "Open in intergrated terminal"
9. In Terminal, type: "./main" to run executable 