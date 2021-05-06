

**CS3320**

**Mini Assignment #2**

**Lexical Conventions and Grammars of Languages: C vs. Python vs.**

**Javascript**

K. LAKSHMI SRAVYA

CS19BTECH11017

**C Kernighan and Ritchie, Appendix A.2:**

• Low level lexical transformations include carrying out directives and performing

macro definition and expansion. Then the would be reduced to sequence of tokens

• Tokens include identifiers, keywords, constants, string literals, operators and other

separators.

• White spaces like blanks, vertical tabs are ignored except when they separate tokens.

• Comments:

➢ Not executed by the compiler

➢ Single line comments → //

Multi line comments → /\* …… \*/

➢ Cannot be nested

➢ Shouldn’t be written between tokens

• Identifiers:

➢ Sequence of letters and digits

➢ First in the sequence should be either alphabet or underscore( \_ )

➢ Case sensitive (distinguishes between capital and small letters)

• Keywords:

➢ Few words are reserved identifiers which are called as keywords. These

identifiers cannot be used for any other purposes

➢ Keywords include words like auto, static, if, else, while, switch, and few more

• Constants:

➢ There are many types of constants that differ based on their type like integer

constants, character constants, floating constants, enumeration constants

➢ Integer constant has further divisions like short, long, signed, unsigned

➢ Constant values cannot be changed or altered in the program

• String literals

➢ Also called as string constants

➢ It is a sequence of characters surrounded by double quotes as in "..." and does

not contain newline or double-quote characters (in order to represent them,

escape sequences as for character constants are to be used)

**Python (Beazley, Chapter#2):**

• Line structure and Indentation:

➢ Each statement is terminated with a new line

➢ Long statements that take multiple lines can be written in the following ways

▪ By using the line-continuation character ( \ )

▪ By enclosing the part of program in parentheses (…), brackets[…],

braces{…} or triple quotes





➢ Indentation is used to denote different blocks of code like bodies of functions,

classes, loops

➢ Indentation should be consistent for the entire block of code

➢ The statement *pass* is used to denote an empty body or block

➢ The practice of using spaces over tab is preferred for indentation to avoid

errors arouse due to mixed inconsistent usage of tabs and spaces

➢ To place more than one statement in a line, separate the statements with

semicolon ( ; ). But using semicolon to terminate a line containing single

statement is considered as poor style

➢ # is used for comments. # inside a string (i.e., inside double quotes) doesn’t

mean comment

➢ Interpreter ignores all the blank spaces except when running in interactive

mode

• Identifiers and Reserved Words

➢ Identifiers:

▪ Sequence of letters and digits

▪ First in the sequence should be either alphabet or underscore( \_ )

▪ Case sensitive (distinguishes between capital and small letters)

▪ Special symbols like $, % and @ are not allowed

▪ Identifiers starting or ending with underscores often have special

meanings like \_foo

▪ Identifiers with leading and trailing double underscores such as

\_\_init\_\_ are reserved for special methods, and identifiers with leading

double underscores such as \_\_bar are used to implement private class

members

➢ Reserved Words:

▪ Few words are reserved identifiers which are called as reserved words.

These identifiers cannot be used for any other purposes

▪ Keywords include words like and, or, if, else, while, break, continue,

and few more

• Literals

➢ Booleans: true – 1, false – 0

➢ Integers:

▪ Includes octal or hexadecimal integers as well.

▪ Octal integers => value precedes with 0

▪ Hexadecimal integers => values precede with 0x

➢ Long Integers

▪ Typically written with trailing l or L character (can be omitted also)

➢ Floating point numbers

▪ Includes exponential numbers

➢ Complex numbers

▪ Integer or floating-point number with trailing j or J is a complex

number

▪ 1.2 + 12.34J => complex number with real and imaginary parts

➢ String literals

▪ 8-bit character data (ASCII)

\-

Defined by enclosing text in single (‘), double (“), or triple (‘ ’ ’ or

“ ” ”) quotes

▪ Unicode (16-bit-wide character data)





\- used to represent multibyte international character sets

\- defined by preceding an ordinary string literal with a *u* or *U*

\- -U command-line option would ensure interpreting all string

literals as Unicode

➢ Values enclosed in

▪ square brackets denote list

▪ parentheses denote tuple

▪ braces denote dictionary

• Operators, Delimiters and Special Symbols

➢ Operators include +, -, \*, \*\*, %, >=, >>= and few more

➢ Delimiters include ( ), [ ], { }, : and few more

➢ Special symbols include ‘, ”, #, \, @

➢ $ and ? have no meaning and cannot appear in the program except inside

quoted string literal

• Documentation Strings:

➢ In a class or function, if first statement is a string then that can be accessed

with *\_ \_doc\_* \_ attribute of the object like *print classname.\_ \_doc\_ \_* would

print the string in the first line of the class or function

• Decorators:

➢ denoted with @ symbol and must be placed on a separate line immediately

before the corresponding function or method. More than one decorator can

also be used

• Source Code Encoding

➢ It is possible to write Python source code in a different encoding by including

a special comment in the first or second line of a Python program:

#!/usr/bin/env python

\# -\*- coding: UTF-8 -\*-

**JavaScript (Chapter#2)**

• Whitespaces

➢ Whitespace can take the form of formatting characters or comments.

➢ Whitespace is usually insignificant, except when they separate tokens.

• Comments:

➢ Same as C language

➢ But single line comments to be preferred over multi line comments to avoid

errors possible in few cases

• Names:

➢ Similar to identifiers in C

➢ Keywords or reserved words cannot be used as names

➢ Used for statements, variables, parameters, property names, operators, and

labels

• Numbers:

➢ Only one type (no divisions like integer, short, long, floating point and double)

➢ This completely avoids cases of overflow in case of short integers

➢ Negative numbers can be formed by using the - prefix operator.





➢ The value *NaN* is a number value that is the result of an operation that cannot

produce a normal result. *NaN* is not equal to any value, including itself. *NaN*

can be detected using *isNaN(number)* function.

➢ The value *Infinity* represents all values greater than

1.79769313486231570e+308.

➢ JavaScript has a Math object that contains a set of methods that act on

numbers. For example, the *Math.floor(number)* method can be used to convert

a number into an integer.

• Strings

➢ Written between single quotes or double quotes

➢ JavaScript does not have character type. It is represented by making a string

with one character.

➢ All characters in JavaScript are 16 bits wide since they were built at the time

of Unicode

➢ Escape sequences are same as in C

➢ Concatenation of strings can be done by using + operator

➢ There are inbuilt functions for strings like toUpperCase (‘cat’.toUpperCase()

=== ‘CAT’)

• Statements

➢ *falsy* values:

▪ false

▪ null

▪ undefined

▪ The empty string ‘’

▪ The number 0

▪ The number NaN

All other values are truthy, including true, the string ‘false’, and all objects

➢ if…else, switch, while, do…while, break, continue are all same as in C with

few differences like the variables need to be defined at the top of function (not

in blocks)

➢ Few new statement types in JavaScript include try and throw

• Expressions

➢ All the operators in C are present in JavaScript like +, -, \*, /, ||

➢ Additional operators in JavaScript are delete, new and few more

• Literals

➢ There are many types like number literal, string literal, object literal, array

literal

➢ Most of the types are similar to that in C

• Functions

➢ Same as that in C

• To interpret the diagrams given in the text book follow the following steps

➢ Start on the left edge and follow the tracks to the right edge.

➢ Literals are represented in ovals, and rules or descriptions are represented in

rectangles.

➢ Any sequence that can be made by following the tracks is legal.

➢ Any sequence that cannot be made by following the tracks is not legal.





➢ Railroad diagrams with one bar at each end allow whitespace to be inserted

between any pair of tokens. Railroad diagrams with two bars at each end do

not.


