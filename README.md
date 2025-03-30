Lexical Analyzer - Technical Overview

This program implements a lexical analyzer for arithmetic expressions, systematically parsing input from a file and segmenting it into discrete tokens. It classifies tokens into identifiers, numeric literals, operators, and delimiters, leveraging character-by-character analysis to construct lexemes and assign corresponding token types.

Functional Breakdown

1. Input Handling

Reads an arithmetic expression from an external file (front.in).

Iterates through the input sequentially, processing one character at a time.

2. Lexical Classification

Identifiers: Sequences of alphabetic characters (A-Z, a-z), denoting variable names (e.g., x, sum).

Numeric Literals: Sequences of digits (0-9), representing integer constants (e.g., 10, 47).

Operators: Recognized symbols (+, -, *, /), each mapped to a predefined token code.

Delimiters: Parentheses ((, )) are treated as structural markers.

Whitespace Handling: Ignored to ensure uninterrupted tokenization.

3. Lexeme Formation & Token Generation

Groups characters into lexemes based on their classification.

Utilizes a lookup table to determine the token type of operators and delimiters.

Outputs token-lexeme pairs as part of the lexical analysis process.

Execution Example

Input File (front.in)

x * (y - 10) / 5

Generated Token Stream

Next token is: 11, Next lexeme is x  
Next token is: 23, Next lexeme is *  
Next token is: 25, Next lexeme is (  
Next token is: 11, Next lexeme is y  
Next token is: 22, Next lexeme is -  
Next token is: 10, Next lexeme is 10  
Next token is: 26, Next lexeme is )  
Next token is: 24, Next lexeme is /  
Next token is: 10, Next lexeme is 5  
Next token is: -1, Next lexeme is EOF  

This output verifies the correct lexical breakdown of identifiers, literals, operators, and delimiters.
