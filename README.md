# About Education Code Mutation

The concept of writing a program as we know it is being replaced by AI systems that are trained rather than coded. With CoPilot and other AI coding assistance tools, the future of computing will involve AIs creating all programs, while humans have minimal supervisory roles. The new atomic unit of computing will be a sizable, previously trained and highly adaptive AI model. In the future, computer science will resemble education more than engineering, focusing on how to best teach the machines, rather than how to construct them. These AI systems will be running our infrastructure, aircraft and governing entire nations.

Now, in introductory computing science courses that is offered at University of Alberta, like CMPUT 174, in order to assess student’s knowledge, instructors prepare exam questions that often include code snippets. Since preparing good quality questions requires significant time and effort, often, only a single version of an exam is used, so each student receives the same questions, which increases the chances of plagiarism. Therefore, the primary goal of this capstone project is to propose a tool that would allow CS instructors to generate unique code snippets based on their needs, where the semantics of the code will remain the same but the code will be mutated (e.g., input and output may change). That would allow the instructors to automatically generate a large (potentially, unlimited) number of questions testing the same concept. Hence, the main objective of this library is that CS course instructors can use it to generate different code snippets based on a given code snippet for exams and quizzes.

## Library Code
The library code can be found at: https://github.com/pranjal080598/Education_Code_Mutation 

## Library Published on PyPI
The library is published at: https://pypi.org/project/edu-code-mutate/0.0.1/ 

## Steps to use the library

[1] Run command on terminal: pip install -i https://test.pypi.org/simple/ edu-code-mutate==0.0.1

[2] Write the following code in a python file:

from edu_code_mutate import mutate

my_code = "print(1+2)"
my_api_key = "YOUR_API_KEY_HERE"

code_versions = mutate(my_code, 1, my_api_key)

print(code_versions)

** Please note that "my_code" can be any code that needs to be mutated and "my_api_key" needs to be updated to an actual api key from OpenAI **

