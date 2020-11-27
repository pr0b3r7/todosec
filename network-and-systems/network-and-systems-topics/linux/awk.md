---
description: mawk - pattern scanning and text processing language
---

# AWK

mawk interpreter for the AWK Programming Language. 

The AWK language is useful for manipulation of data files, text retrieval and processing, and for prototyping and experimenting with algorithms. mawk is a new awk meaning it implements the AWK language as defined in Aho, Kernighan and Weinberger, The AWK Programming Language, Addison-Wesley Publishing, 1988 \(hereafter referred to as the AWK book.\) mawk conforms to the POSIX 1003.2 \(draft 11.3\) definition of the AWK lan‐ guage which contains a few features not described in the AWK book, and mawk provides a small number of extensions.

An  AWK  program is a sequence of pattern {action} pairs and function definitions.  Short programs are entered on the command line usually enclosed in ' ' to avoid shell interpretation.  Longer programs can be read in from a file with  the  -f option. Data input  is  read from the list of files on the command line or from standard input when the list is empty.

The input is broken into records as determined by the record separator variable, RS.  Initially, RS = “\n” and records are synonymous  with  lines.  Each record is compared against each pattern and if it matches, the program text for {action} is executed.

OPTIONS

-F value - sets the field separator, FS, to value.

-f file - Program text is read from file instead of from the command line. Multiple -f options are allowed.

-v var=value   assigns value to program variable var.

-- : indicates the unambiguous end of options.

The above options will be available with any POSIX compatible implementation of AWK.  Implementation specific options are prefaced with -W. mawk provides these:

-W dump - writes  an  assembler  like listing of the internal representation of the program to stdout and exits 0 \(on successful compilation\).

-W exec file - Program text is read from file and this is the last option.

This is a useful alternative to -f on systems that support the \#!  “magic number” convention for executable scripts. Those implicitly pass  the pathname of the script itself as the final parameter, and expect no more than one “-” option on the \#! line. Because mawk can combine multiple -W options separated by commas, you can use this option when an additional -W option is needed.

-W help        prints a usage message to stderr and exits \(same as “-W usage”\).

-W interactive sets  unbuffered writes to stdout and line buffered reads from stdin. Records from stdin are lines regardless of the value of RS.

-W posix\_space forces mawk not to consider '\n' to be space.

-W random=num  calls srand with the given parameter \(and overrides the auto-seeding behavior\).

-W sprintf=num adjusts the size of mawk's internal sprintf buffer to num bytes.  More than rare use of this  option  indicates mawk should be recompiled.

-W usage prints a usage message to stderr and exits \(same as “-W help”\).

- W version: mawk writes its version and copyright to stdout and compiled limits to stderr and exits 0.

mawk accepts abbreviations for any of these options, e.g., “-W v” and “-Wv” both tell mawk to show its version.

mawk  allows multiple -W options to be combined by separating the options with commas, e.g., -Wsprint=2000,posix.  This is useful for executable \#! “magic number” invocations in which only one argument is supported, e.g., -Winteractive, exec.

THE AWK LANGUAGE

   1. Program structure

An AWK program is a sequence of pattern {action} pairs and user function definitions.

       A pattern can be:

BEGIN

END

expression

expression , expression

One, but not both, of pattern {action} can be omitted.  If {action} is omitted it is implicitly {print}. If pattern is omitted, then it is implicitly matched.  BEGIN and END patterns require an action.

Statements  are  terminated  by  newlines, semi-colons  or both. Groups of statements such as actions or loop bodies are blocked via { ... } as in C. The last statement in a block doesn't need a terminator. Blank lines have  no  meaning;  an empty  statement  is terminated with a semi-colon. Long statements can be continued with a backslash, \. A statement can be broken without a backslash after a comma, left brace, &&, \|\|, do, else, the right parenthesis of an if,  while  or  for statement,  and  the right parenthesis of a function definition.  A comment starts with \# and extends to, but does not include the end of line. The following statements control program flow inside blocks.

```text
if ( expr ) statement
if ( expr ) statement else statement
while ( expr ) statement
do statement while ( expr )
for ( opt_expr ; opt_expr ; opt_expr ) statement
for ( var in array ) statement
continue
break
```





