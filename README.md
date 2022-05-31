# winfsp.sym &middot; WinFsp Symbol Server

This is the repository of the WinFsp symbol and source server for use with the Debugging Tools for Windows. Private symbols for WinFsp Beta and Gold releases can be found here.

# How to use

Use the following symbol and source paths to access the symbols:

```
sympath: https://github.com/winfsp/winfsp.sym/raw/master/sym
srcpath: srv*
```

For example in WinDbg:

```
.sympath+ https://github.com/winfsp/winfsp.sym/raw/master/sym
.srcfix
```

# How to add symbols

Execute the following command to add new private symbols:

```
.\tools\symadd.ps1 ..\winfsp\build\VStudio\build\Release -PdbKind Private
```

For more information see https://github.com/billziss-gh/symsrv.
