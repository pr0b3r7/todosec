---
description: mawk - pattern scanning and text processing language
---

# AWK

TL/DR:

`awk '{print $2}' --> prints the second columns`

```text
catn /var/log/auth.log | grep "session" | awk '{print $2}' 

22
23
24
25
26
27
```

\`\`

```text
awk 'length($2) == 2 { print $2 }'  /var/log/auth.log

#prints the second column if it character count is 2. 

22
23
24
25
26
27
```

mawk interpreter for the AWK Programming Language. 

The AWK language is useful for manipulation of data files, text retrieval and processing, and for prototyping and experimenting with algorithms. mawk is a new awk meaning it implements the AWK language as defined in Aho, Kernighan and Weinberger, The AWK Programming Language, Addison-Wesley Publishing, 1988 \(hereafter referred to as the AWK book.\) mawk conforms to the POSIX 1003.2 \(draft 11.3\) definition of the AWK lan‐ guage which contains a few features not described in the AWK book, and mawk provides a small number of extensions.

An  AWK  program is a sequence of pattern {action} pairs and function definitions. Short programs are entered on the command line usually enclosed in ' ' to avoid shell interpretation. Longer programs can be read in from a file with  the  -f option. Data input is read from the list of files on the command line or from standard input when the list is empty.

The input is broken into records as determined by the record separator variable, RS. Initially, RS = “\n” and records are synonymous with lines. Each record is compared against each pattern and if it matches, the program text for {action} is executed.

#### OPTIONS

```text
-F value - sets the field separator, FS, to value.
-f file - Program text is read from file instead of from the command line. Multiple -f options are allowed.
-v var=value   assigns value to program variable var.
-- : indicates the unambiguous end of options.
```

The above options will be available with any POSIX compatible implementation of AWK.  Implementation specific options are prefaced with -W. mawk provides these:

```text
-W dump - writes  an  assembler  like listing of the internal representation of the program to stdout and exits 0 (on successful compilation).
-W exec file - Program text is read from file and this is the last option.
    his is a useful alternative to -f on systems that support the #!  “magic number” convention for executable scripts. Those implicitly pass  the pathname of the script itself as the final parameter, and expect no more than one “-” option on the #! line. Because mawk can combine multiple -W options separated by commas, you can use this option when an additional 
    -W option is needed.
-W help        prints a usage message to stderr and exits (same as “-W usage”).
-W interactive sets  unbuffered writes to stdout and line buffered reads from stdin. Records from stdin are lines regardless of the value of RS.
-W posix_space forces mawk not to consider '\n' to be space.
-W random=num  calls srand with the given parameter (and overrides the auto-seeding behavior).
-W sprintf=num adjusts the size of mawk's internal sprintf buffer to num bytes.  More than rare use of this  option  indicates mawk should be recompiled.
-W usage prints a usage message to stderr and exits (same as “-W help”).
- W version: mawk writes its version and copyright to stdout and compiled limits to stderr and exits 0.
```

mawk accepts abbreviations for any of these options, e.g., “-W v” and “-Wv” both tell mawk to show its version.

mawk  allows multiple -W options to be combined by separating the options with commas, e.g., -Wsprint=2000,posix.  This is useful for executable \#! “magic number” invocations in which only one argument is supported, e.g., -Winteractive, exec.

THE AWK LANGUAGE

#### 1. Program structure

An AWK program is a sequence of pattern {action} pairs and user function definitions.

A pattern can be:

```text
BEGIN
END
expression
expression , expression
```

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

#### 2. Data types, conversion and comparison

There are two basic data types, numeric and string. Numeric constants can be integer like -2, decimal like 1.08, or in scientific notation like -1.1e4 or .28E-3. All numbers are represented internally and all computations are done in floating point arithmetic. So for example, the expression 0.2e2 == 20 is true and true is represented as 1.0.

String constants are enclosed in double quotes.

"This is a string with a newline at the end.\n"

Strings can be continued across a line by escaping \(\) the newline. The following escape sequences are recognized.

```text
            \\        \
            \"        "
            \a        alert, ascii 7
            \b        backspace, ascii 8
            \t        tab, ascii 9
            \n        newline, ascii 10
            \v        vertical tab, ascii 11
            \f        formfeed, ascii 12
            \r        carriage return, ascii 13
            \ddd      1, 2 or 3 octal digits for ascii ddd
            \xhh      1 or 2 hex digits for ascii  hh
```

If you escape any other character \c, you get \c, i.e., mawk ignores the escape.

There are really three basic data types; the third is number and string which has both a numeric value and a string value at the same time.  
User defined variables come into existence when first referenced and are initialized to null, a number and string value which has numeric value 0 and string value "".  
Non-trivial number and string typed data come from input and are typically stored in fields. \(See section 4\).

The type of an expression is determined by its context and automatic type conversion occurs if needed.  
For example, to evaluate the statements

```text
y = x + 2  ;  z = x  "hello"
```

The value stored in variable y will be typed numeric. 

If x is not numeric, the value read from x is converted to numeric before it is added to 2 and stored in y. The value stored in variable z will be typed string, and the value of x will be converted to string if necessary and concatenated with "hello". \(Of course, the value and type stored in x is not changed by any conversions.\) 

A string expression is converted to numeric using its longest numeric prefix as with atof\(3\). 

A numeric expression is converted to string by replacing expr with sprintf\(CONVFMT, expr\), unless expr can be represented on the host machine as an exact integer then it is converted to sprintf\("%d", expr\). 

Sprintf\(\) is an AWK built-in that duplicates the functionality of sprintf\(3\), and CONVFMT is a built-in variable used for internal conversion from number to string and initialized to "%.6g". Explicit type conversions can be forced, expr "" is string and expr+0 is numeric.

To evaluate, expr1 rel-op expr2, if both operands are numeric or number and string then the comparison is numeric; if both operands are string the comparison is string; if one operand is string, the non-string operand is converted and  the  comparison is string.  The result is numeric, 1 or 0.

In  boolean contexts such as, if \( expr \) statement, a string expression evaluates true if and only if it is not the empty string ""; numeric values if and only if not numerically zero.

#### 3. Regular expressions

In the AWK language, records, fields and strings are often tested for matching a regular expression. Regular expressions are enclosed in slashes, and

```text
expr ~ /r/
```

is an AWK expression that evaluates to 1 if expr “matches” r, which means a sub-string of expr is in the set of strings defined by r. With no match the expression evaluates to 0; replacing ~ with the “not match” operator, !~ , reverses the meaning. As pattern-action pairs,  

```text
/r/ { action }   and   $0 ~ /r/ { action }
```

are  the  same,  and  for each input record that matches r, action is executed.  In fact, /r/ is an AWK expression that is equivalent to \($0 ~ /r/\) anywhere except when on the right side of a match operator or passed as an argument to a built-in function that expects a regular expression argument.

AWK  uses  extended  regular  expressions  as with the -E option of grep\(1\).  The regular expression meta-characters, i.e., those with special meaning in regular expressions are

```text
\ ^ $ . [ ] | ( ) * + ?
```

Regular expressions are built up from characters as follows:

```text
c            matches any non-metacharacter c.
\c           matches a character defined by the same escape sequences used in string constants or the literal character c if \c is not an escape sequence.
.            matches any character (including newline).
^            matches the front of a string.
$            matches the back of a string.
[c1c2c3...]  matches  any  character  in  the  class c1c2c3... .  An interval of characters is denoted c1-c2 inside a class [...].
[^c1c2c3...] matches any character not in the class c1c2c3...
```

Regular expressions are built up from other regular expressions as follows:

```text
r1r2         matches r1 followed immediately by r2 (concatenation).
r1 | r2      matches r1 or r2 (alternation).
r*           matches r repeated zero or more times.
r+           matches r repeated one or more times.
r?           matches r zero or once.
(r)          matches r, providing grouping.
```

The increasing precedence of operators is alternation, concatenation and unary \(\*, + or ?\).

For example,

```text
/^[_a-zA-Z][_a-zA-Z0-9]*$/  and
/^[-+]?([0-9]+\.?|\.[0-9])[0-9]*([eE][-+]?[0-9]+)?$/
```

are matched by AWK identifiers and AWK numeric constants respectively.  Note that “.” has to be escaped to be  recognized as a decimal point, and that meta-characters are not special inside character classes.

Any  expression can be used on the right hand side of the ~ or !~ operators or passed to a built-in that expects a regular expression.  If needed, it is converted to string, and then interpreted as a regular expression.  For example,

```text
BEGIN { identifier = "[_a-zA-Z][_a-zA-Z0-9]*" }
$0 ~ "^" identifier
```

prints all lines that start with an AWK identifier.

mawk recognizes the empty regular expression, //, which matches the empty string and hence is matched by any string at the front, back and between every character.  For example,

```text
echo  abc | mawk { gsub(//, "X") ; print }
XaXbXcX
```

#### 4 - Records and fields

Records  are read in one at a time, and stored in the field variable **$0.**  The record is split into fields which are stored in **$1, $2**, ..., **$NF.** The built-in variable **NF** is set to the number of fields, and  **NR**  and  **FNR**  are  incremented  by  1. Fields above **$NF** are set to "".

Assignment  to **$0** causes the fields and **NF** to be recomputed.  Assignment to **NF** or to a field causes **$0** to be reconstructed by concatenating the **$i's** separated by **OFS**.  Assignment to a field with index greater than **NF,** increases **NF** and causes  **$0** to be reconstructed.

Data  input  stored  in fields is string, unless the entire field has numeric form and then the type is number and string. For example,

```text
            echo 24 24E |
            mawk '{ print($1>100, $1>"100", $2>100, $2>"100") }'
            0 1 1 1
```

#### 5 - Expressions and operators

The  expression  syntax  is similar to C.  Primary expressions are numeric constants, string constants, variables, fields, arrays and function calls.  The identifier for a variable, array or function can be a sequence of letters, digits and  underscores,  that  does  not start with a digit.  Variables are not declared; they exist when first referenced and are initialized to null.

New expressions are composed with the following operators in order of increasing precedence.

```text
            assignment          =  +=  -=  *=  /=  %=  ^=
            conditional         ?  :
            logical or          ||
            logical and         &&
            array membership    in
            matching       ~   !~
            relational          <  >   <=  >=  ==  !=
            concatenation       (no explicit operator)
            add ops             +  -
            mul ops             *  /  %
            unary               +  -
            logical not         !
            exponentiation      ^
            inc and dec         ++ -- (both post and pre)
            field               $
```

Assignment, conditional and exponentiation associate right to left; the other operators associate left to right.  Any  expression can be parenthesized.

#### 6 - Arrays

Awk provides one-dimensional arrays. Array elements are expressed as array\[expr\]. Expr is internally converted to string type, so, for example, A\[1\] and A\["1"\] are the same element and the actual index is "1". Arrays indexed by strings are called associative arrays. Initially an array is empty; elements exist when first accessed. An expression, expr in array evaluates to 1 if array\[expr\] exists, else to 0.

There is a form of the for statement that loops over each index of an array.

```text
for ( var in array ) statement
```

sets **var** to each index of array and executes statement.  The order that var transverses the indices of array  is  not  defined.

The  statement,  **delete**  **array\[expr\]**,  causes  **array\[expr\]**  not to exist.

mawk supports an extension, delete array, which deletes all elements of array.

Multidimensional arrays are synthesized with concatenation using the  built-in  variable  **SUBSEP.   array\[expr1,expr2\]**  is equivalent to **array\[expr1 SUBSEP expr2\].**  Testing for a multidimensional element uses a parenthesized index, such as:

```text
if ( (i, j) in A )  print A[i, j]
```

#### 7 - Builtin-variables

The following variables are built-in and initialized before program execution.

```text
ARGC      number of command line arguments.
ARGV      array of command line arguments, 0..ARGC-1.
CONVFMT   format for internal conversion of numbers to string, initially = "%.6g".
ENVIRON   array  indexed  by  environment  variables.   An  environment string, var=value is stored as ENVIRON[var] = value.
FILENAME  name of the current input file.
FNR       current record number in FILENAME.
FS        splits records into fields as a regular expression.
NF        number of fields in the current record.
NR        current record number in the total input stream.
OFMT      format for printing numbers; initially = "%.6g".
OFS       inserted between fields on output, initially = " ".
ORS       terminates each record on output, initially = "\n".
RLENGTH   length set by the last call to the built-in function, match().
RS        input record separator, initially = "\n".
RSTART    index set by the last call to match().
SUBSEP    used to build multiple array subscripts, initially = "\034".
```





          



#### Examples

```text
       1. emulate cat.

            { print }

       2. emulate wc.

            { chars += length($0) + 1  # add one for the \n
              words += NF
            }

            END{ print NR, words, chars }

       3. count the number of unique “real words”.

            BEGIN { FS = "[^A-Za-z]+" }

            { for(i = 1 ; i <= NF ; i++)  word[$i] = "" }

            END { delete word[""]
                  for ( i in word )  cnt++
                  print cnt
            }

       4. sum the second field of every record based on the first field.

            $1 ~ /credit|gain/ { sum += $2 }
            $1 ~ /debit|loss/  { sum -= $2 }

            END { print sum }

       5. sort a file, comparing as string

            { line[NR] = $0 "" }  # make sure of comparison type
                            # in case some lines look numeric

            END {  isort(line, NR)
              for(i = 1 ; i <= NR ; i++) print line[i]
            }

            #insertion sort of A[1..n]
            function isort( A, n,    i, j, hold)
            {
              for( i = 2 ; i <= n ; i++)
              {
                hold = A[j = i]
                while ( A[j-1] > hold )
                { j-- ; A[j+1] = A[j] }
                A[j] = hold
              }
              # sentinel A[0] = "" will be created if needed
            }
```



