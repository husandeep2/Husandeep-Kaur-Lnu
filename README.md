# CIS 524 -- Spring 2026

## Programming Assignment

**Student Name:** Husandeep Kaur
**CSU ID:** 2923304

------------------------------------------------------------------------

# Project Overview

This project develops a top-down recursive descent interpreter in Python for a simple programming language described in the CIS 524 project specification.

The interpreter:

-   Reads a .tiny input file from the command line
-   Performs lexical analysis (tokenizes the input)
-   Parses the program based on the specified grammar
-   Evaluates expressions while parsing
-   Displays the result of each valid let-in-end block
-   Outputs Error for invalid blocks
-   Continues running even after encountering errors

------------------------------------------------------------------------
# Program Structure

## Lexer

The Lexer class:

-   Transforms the input text into tokens
-   Identifies keywords such as let, in, end, int, real, if, then, and else
-   Detects identifiers and numeric literals
-   Recognizes arithmetic and comparison operators
-   Skips over whitespace
-   Adds an EOF token at the end of the input

## Parser

The Parser class uses a recursive descent approach to perform parsing.
Each grammar rule is implemented as a separate function:

-   let_in_end()
-   decl_list()
-   decl()
-   type_rule()
-   expr()
-   term()
-   factor()
-   cond()
-   if_expr()

Expressions are evaluated during parsing.

------------------------------------------------------------------------
# Type Handling

The language supports:

-   int
-   real

Features implemented:

-   Explicit casting: int(x), real(x)
-   Proper type conversion during assignment
-   Correct return type for each block

------------------------------------------------------------------------
# Symbol Table

A dictionary is used to store variables in the form:
variable_name → (type, value)
The symbol table is reset for each new let block to maintain correct scoping.

------------------------------------------------------------------------

# Error Handling

The interpreter prints:

Error

when:

-   Syntax errors occur
-   Undeclared variables are used
-   Type mismatches occur
-   Grammar rules are violated

If one block fails, execution continues to the next block.

------------------------------------------------------------------------
# How to Run

From terminal:

python3 parser_2923304.py sample2.tiny

Example output:

20 </n>
314.16 
0.25

Example with error:

48.0 
Error

------------------------------------------------------------------------
# Features Implemented

-   Top-down recursive descent parsing
-   Lexical analysis using regular expressions
-   Symbol table with scoped variables
-   Integer and real types
-   Explicit type casting
-   Arithmetic operations with correct precedence
-   Conditional expressions (if-then-else)
-   Comparison operators
-   Multiple let blocks
-   Robust error handling

------------------------------------------------------------------------
# Conclusion

This project showcases a fully functional recursive descent interpreter implemented in Python. The interpreter adheres to the specified grammar, evaluates expressions with correct precedence, manages scoped symbol tables, and includes robust error handling that allows execution to continue across multiple blocks.

All project requirements have been successfully implemented.
