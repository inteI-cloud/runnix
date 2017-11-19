runnix
======

Run linux executables or scripts in Windows 10 without opening Bash

 

Usage
=====

Usage is fairly simple:

`runnix [executable] --args1 [arg1a] [arg2b] ... [arg1N] --args2 [arg2a] [arg2b]
... [arg2N] --options [option1] [option2] ... [optionN]`

 

**where:**

-   **[executable]** is path to the linux executable or script you want to run

-   arguments corresponding to `--arg1` will be thrown before the executable
    when we run it in WSL:

    `arg1a arg1b ... arg1N C:\path\to\my\linux\script.sh`

-   arguments corresponding to `--arg2` will be thrown after the executable when
    we run it in WSL, like this:

    `C:\path\to\my\linux\script.sh arg2a arg2b ... arg2N`

-   **[options]** are arguments for runnix. They will not be part of the command
    that’ll be executed.

Available options are:

\-h Print help

\-s Treat the [executable] as script

\-d [str] Choose yourself the distro in which you want to run your command.

NOTE: [str] must be a unique name representing a distro e.g.
Fabrikam.Distro.10.01 or Ubuntu. Default is Ubuntu.

**Rules:**

-   you **MUST** follow the order shown but

-   you **ARE ALLOWED** to use ONLY the switches YOU desire.

e.g. one may only use the `--args1` and `--options`, or the `--args1` and
`--args2`, etc. That's ok.

Build
=====

You will need Visual Studio (At least with C++ Support)

Aknowledgements
===============

Many thanks to GitHub user "0xbadfca11" for his code related to getting the
WslLaunch function from the wslapi.dll.

Notes
=====

This will *NOT* work on some older versions of Windows 10. Please update your
Windows to latest version if you want to use this software.

License
=======

MIT License
