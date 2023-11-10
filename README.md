# Compiler_Construction_Mini_Project
Group 6
Group Members
______________
135581-Peter Owira  
134703 Rita Maringa  
137023 Booker Ongalo  
134707 Joseph Mutua  
132759 Leon Langat  
136902 Cheruiyot Emmanuel
___________________________________________________________________________________________________________

Recursive Descent parser
*************************
In class we looked at Parsing and different types of parsing techniques. Recursive-descent parsing is a top-down method of syntax analysis in which a set of recursive procedures is used to process the input. One procedure is
associated with each nonterminal of a grammar. Here, we consider a simple form of recursive-descent parsing, called predictive parsing, in which the lookahead symbol unambiguously determines the 
flow of control through the procedure
body for each nonterminal. The sequence of procedure calls during the analysis
of an input string implicitly denes a parse tree for the input, and can be usedto build an explicit parse tree, if desired.

The implementation we have here is of a Recursive descent parser which basically implements an arithematic expression grammar that supports addition and multiplication with 
E as the expression
T as the term
F as the factor
the code checks whether a given input string is syntactically valid according to the specified grammar. The input string is read from the user and stored in the list (s) and Tthe variable (i) is used as an index to traverse the input string.. The parsing process is done through a series of functions, each corresponding to a non-terminal in the grammar.
The code checks if the input string forms a valid expression according to the grammar. If the E() function returns True and the index i reaches the end of the input string, it prints "String is accepted"; otherwise, it prints "String is not accepted."

match(a) checks if the current character in the input string matches the expected character 'a'
F(): Implements the production rules for the non-terminal F
Tx(): Implements the production rules for the non-terminal T' where there is a multiplication
T(): Implements the production rules for the non-terminal T. It checks for a factor (F) followed by optional multiplications (Tx)
Ex(): Implements the production rules for the non-terminal E'. It handles the case where there is an addition followed by another term (T) and another expression (Ex)
E(): Implements the production rules for the non-terminal E. It checks for a term (T) followed by optional additions (Ex)
