# Education Code Mutation

The concept of writing a program as we know it is being replaced by AI systems that are trained rather than coded. With CoPilot and other AI coding assistance tools, the future of computing will involve AIs creating all programs, while humans have minimal supervisory roles. The new atomic unit of computing will be a sizable, previously trained and highly adaptive AI model. In the future, computer science will resemble education more than engineering, focusing on how to best teach the machines, rather than how to construct them. These AI systems will be running our infrastructure, aircraft and governing entire nations.

Now, in introductory computing science courses that is offered at University of Alberta, like CMPUT 174, in order to assess student’s knowledge, instructors prepare exam questions that often include code snippets. Since preparing good quality questions requires significant time and effort, often, only a single version of an exam is used, so each student receives the same questions, which increases the chances of plagiarism. Therefore, the primary goal of this capstone project is to propose a tool that would allow CS instructors to generate unique code snippets based on their needs, where the semantics of the code will remain the same but the code will be mutated (e.g., input and output may change). That would allow the instructors to automatically generate a large (potentially, unlimited) number of questions testing the same concept. Hence, the main objective of this library is that CS course instructors can use it to generate different code snippets based on a given code snippet for exams and quizzes.

## Library Code
The library code can be found at: https://github.com/pranjal080598/Education_Code_Mutation 

## Library Published on PyPI
The library is published at: https://pypi.org/project/edu-code-mutate/0.0.1/ 

## Steps to use the library

[1] Run command on terminal: pip install edu-code-mutate==0.0.1

[2] Write the following code in a python file:

from edu_code_mutate import mutate

my_code = "print(1+2)"
my_api_key = "YOUR_API_KEY_HERE"

code_versions = mutate(my_code, 1, my_api_key)

print(code_versions)

** Please note that "my_code" can be any code that needs to be mutated and "my_api_key" needs to be updated to an actual api key from OpenAI **

## Check and Mutations

|    CheckID    | Check description | Mutation0 | Mutation1 | Mutation 2 |
| ------------- | ----------------- | ----------|-----------| -----------|            
|StrLit         |String literals    | Change the string literal to a different one, keeping the same length | | |
|IntLit         |Integer literals| Change the integer literal to a different one | | |
|SnglFor        |Single-level for loop| Tweak loop | | |
|NstdFor        |Nested for loop (two levels)| Swap levels of the for loop | | |
|RngStmt        |Range statement| Change first argument of range() | Change the second argument of range, or add it if it doesn't exist | Change the third argument of range, or add it if it doesn't exist |
|SnglIf         |Single-level if statement| Change if statement with values in it | | |
|NstdIf2        |Nested if statement (two levels)| Swap levels of if statement | | |
|NstdIf3        |Nested if statement (three levels)| Swap levels of if statement | | |
|ElifBlk        |Elif block| Replace elif with else | | |
|ElseBlk        |Else block| Replace else with elif | | |
|CmpOper        |Any comparison operator| Replace with a different comparison operator | | |
|EqlOper        |Equality operator (==)| Add "not" | Replace == with != | |
|IneqOper       |Inequality operator (!=)|Add "not" | Replace != with == | |
|BoolOper       |Boolean operator (and, or)| Add "not" | Replace and with or, or with and | 
|ArithExpr      |Arithmetic expression with parentheses (where order of operations is important)| Rearrange parentheses | Add extra parentheses | Remove some parentheses |
|LenList        |len() function called on a list| Add 1 to len() | Subtract 1 from len() |
|LenStr         |len() function called on a string | Add 1 to len() | Subtract 1 from len() | |
|IdxList        |Accessing list elements by index | Add 1 to the index | Subtract 1 from index | |
|IdxStr         | Accessing string elements by index | Add 1 to the index | Subtract 1 from index| | 
|LstStrLIT      |List of string literals | Change string literals to different string literals | Change number of string literals, keeping literals intact | |
|LstIntLit      | List of integer literals | Change integer literals to different integer literals | Change number of integer literals, keeping literals intact | |
|TplStrLit      |Tuple of string literals| Change string literals to different string literals | Change number of string literals, keeping literals intact | |
|TplIntLit      | Tuple of integer literals | Change integer literals to different integer literals | Change number of integer literals, keeping literals intact | |
|LstLstStr      |List of lists of string literals | Change string literals to different string literals | Change number of string literals, keeping literals intact | Change number of inner lists |
|LstLstInt      | List of lists of integer literals | Change integer literals to different integer literals | Change number of integer literals, keeping literals intact | Change number of inner lists |
|WhileLoop      | While loop | same as for loop condition | | |
|BinAritOp      | Binary arithmetic operator | Change to a different arithmetic operator | | |
|UnrAritOp      | Unary arithmetic operator (-) | Remove the unary operator | | |
|IdxVar         | Integer variable as index| Add 1 | Subtract 1 | |
|IdxVarP1       | Integer variable plus 1" as index | Add 1 | Subtract 1 | |
|IdxVarM1       | Integer variable minus 1 as index| Add 1 | Subtract 1 | |

## License

MIT License
