# BODMAS

I wrote this c++ script to solve arithmetic strings back in 2019- before I knew anything about parsing. It takes in a string like "2*(3+4\*cos30)" and returns an answer.

It uses a recursive method to do this. First it adds brackets (parentheses) to the string to ensure each set of brackets has one operator (+,-,etc) surrounded by two numbers (or other brackets). Then it solves through those brackets recursively.
