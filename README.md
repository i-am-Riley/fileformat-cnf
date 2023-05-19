# SYSTEM.CNF
This file is top-level and defines a few parameters for the PS2 to use to run the program.

## Contents
These are the contents for the copy of .hack//infection's ``System.cnf`` which uses CRLF for the newlines
```
BOOT2 = cdrom0:\SLUS_202.67;1
VER = 1.00
VMODE = NTSC

```

A ``PARAM2`` and ``PARAM4`` can also be present but aren't in this example.

## Loading in C#
For C# reference the following for use to load a CNF file:  
[CnfFile](https://github.com/i-am-Riley/fileformat-cnf/blob/main/Rileysoft.FileFormats.CNF/Rileysoft.FileFormats.CNF/CnfFile.cs) - Performs I/O to read/write CNF data.  
[CnfData](https://github.com/i-am-Riley/fileformat-cnf/blob/main/Rileysoft.FileFormats.CNF/Rileysoft.FileFormats.CNF/CnfData.cs) - Defines CNF data.  

Code Example:
```cs
using Rileysoft.FileFormats.CNF;

var file = new CnfFile("SYSTEM.CNF", true); // Reads SYSTEM.CNF and sets the underlying data to readonly.
var cnfData = file.Data;
```

## References
- Reference [this constructor](https://github.com/i-am-Riley/fileformat-cnf/blob/f81516c9acc5c0586826650ed86f10929fd8b9c6/Rileysoft.FileFormats.CNF/Rileysoft.FileFormats.CNF/CnfFile.cs#L29) for more information on the constructor used in this example.
- Reference [PS Dev Wiki](https://www.psdevwiki.com/ps2/System.cnf) for more information on ``System.cnf``.
