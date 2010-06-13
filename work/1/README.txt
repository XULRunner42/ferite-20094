Developers: Kingdon Barrett (kpb1363)


Table of Contents
1. Building
2. Generating Documentation
3. Usage
4. Known Issues
5. Resources


========================================
1. Building
========================================
There is nothing to build yet.  Ferite is a scripting language.


========================================
2. Generating Documentation
========================================
Have yet to explore the feritedoc command.  This code is adapted from
a Go language implementation of expr that was submitted for Go-2009-3
at RIT.  Our implementation was in some ways not good.  Part of this
effort is also revising the solutions presented then, into a 20094 set.


========================================
3. Usage
========================================
./expr -- escaped-expression

example:
$ ./expr -- 7 \* \( 5 + 3 \* 8 \) / 4 - \( 2 + 9 \) - 1
38

The escapes ['\*', '\(', '\)'] may be necessary to prevent the shell
from interpreting your arguments as shell commands.  The expr command
should correctly handle any operators that you throw at it, including
parenthesis to force a particular order of operations.

Ferite requires that arguments passed into the script are following a
symbolic -- to indicate the end of compiler/interpreter argument list.
There might be something better to say than "#!/usr/bin/env ferite" ?

========================================
4. Known Issues
========================================
The software has not been developed yet.  A modular approach that mirrors
the Go-2009-3 implementation is planned.  This program requires a minimum
understanding of the way that command line arguments are parsed, arrayish
data structures, 


========================================
5. Resources
========================================
Resource: Assignment 1: Arithmetic
Location: http://www.cs.rit.edu/~ats/go-2009-3/1/problem.xml
Provided: This assignment was developed by Axel Schreiner for the Go-2009-3
          curriculum.  The hints must be discarded, they are not for ferite.

Resource: GoLang/work/hw/1/
Location: http://harrydavis.csh.rit.edu/~yebyen/GoLang/work/hw/1/
Provided: A solution in another language, plus some other solutions for the
          purpose of comparison.
