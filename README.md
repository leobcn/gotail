# gotail
A golang version of the UNIX command "tail"*.

\* Minus a whole lot of features. But if you simply want to tail lines of text from a file, it works!

##Usage:
Can be used from the CLI (go install-ed) or imported into other golang projects.

CLI: Very similar to "tail":
- `-file` : The path to the file you want to tail. Can be relative or absolute. (required)
- `-n` : The number of lines to tail.

Imported: Call the function `GoTail` with two inputs:
- `filename` : The path to the file you want to tail (string).
- `numLines` : The number of lines you want to return from the file (int).

##Performance Comparisons:
I have no idea how it performs compared to the UNIX "tail" command. I would assume worse.

##Why Did I Build This?:
I needed a way to retreive the last "x" many lines of some log files for displaying in an admin console GUI.  It seemed like a better idea to implement "tail" in go rather then call the system installed "tail" command and retreiving the stdout.  After building the "import-able" version I figured it was easy enough to modify the code into working from the CLI as well.
