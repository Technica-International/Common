# General Guidelines


## IDE and Tools

1. **IDE Used**: Visual Studio 2019 Community
2. **Text Editor**: Visual Studio Code
3. **Tools**:
	1. **VS19**:
		1. Codemaid - Menu Clear Code (use .config file under settings)
		2. Code Converter C# to VB.NET
		3. Microsoft Code Analysis 2019
		4. Comment Remover - Edit Comment - Remove All
		5. License Header Manager (Right-Click - License Header - Add Definition) - Edit - Advanced / Add License Header
		6. Security Code Scanner (to try)
		7. Solution Error Visualizer
		8. IntelliCode -  from Visual Studio Installer
		9. Avalonia
		10. Settings Sync
		11. File Icons
		12. RevDeBug
		13. Comments Plus 
			1. //! Important - formatted as bold.
			2. //? Question - colored red.
			3. //x Removed - formatted as strikethrough.
			4. //TODO: Task - colored light green.
			5. //!? WT*‽ - colored Purple.
		14. JetBrains Resharper
	2. **VS Code**:
		1. Python
		2. Visual Studio IntelliCode
		3. Javascript
		4. Code Runner
		5. AREPL
4. **VS DevOps**
	1. https://docs.microsoft.com/en-us/azure/devops/repos/tfvc/add-check-policies?view=azure-devops
	3. Team explorer -> Settings -> source control -> and check tabs
	4. 
		1. Changeset comments policy
		2. Builds
		3. Work items



## Languages and Libraries
1. C# (Main)
2. VB (Main)
3. Java (IoT, Mobile Android)
4. SQL (Database) - Unless Limitations use XML File Database
5. C++ (Low Level or Mandatory)
6. Python (Prototyping, Statistical and AI)
7. ASP.NET (Web, Azure), Maybe Node.js TypeScript or JavaScript (Web)
8. MATLAB (Advanced Prototyping, Statistical and Closed AI)



### Python Libraries
1. Basic environment reg-env.txt
2. Machine learning environment: ML-env.txt

To create or install from a text file use the following commands:
> `pip freeze > my-reqs.txt`
> `pip install -r requirements.txt`



## Android
- Android Studio with Java Android
- Projects must adhere to the Structure in Tech.Java repo
- Gradle as Project Manager



## Versioning
Our versions are in the format a.b.c.d

"a" is the yearly release version (0 for the release version, 1 is after one year since the initial release and so on...)

"b" is the Major release version, i.e. including new features

"c" is for bug fixes version.

"d" is for minor fixes.

