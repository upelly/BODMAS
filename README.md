# BODMAS

I wrote this C++ script to solve arithmetic strings back in 2019- before I knew anything about parsing. It takes in a string like "2*(3+4\*cos30)" and returns an answer.

It uses a recursive method to do this. First it adds brackets (parentheses) to the string to ensure each set of brackets has one operator (+,-,etc) surrounded by two numbers (or other brackets). Then it solves through those brackets recursively.

I'll take you through an example string to see how it works:

Input:
1+5*(9+4-3\*1)-5

Adding brackets:
1+5*(9+4-(3\*1))-5
1+5*((9+4)-(3\*1))-5
1+(5*((9+4)-(3\*1)))-5
(1+(5*((9+4)-(3\*1))))-5

Solving recursively - it goes into the string, then into each substring as indicated by the brackets
(1+(5*((9+4)-(3\*1))))-5
(1+(5*(13-(3\*1))))-5
(1+(5*(13-3)))-5
(1+(5\*10))-5
(1+50)-5
51-5
46
