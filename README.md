Quiz Games are one of the most interactive and mind blogging games of all time. Whether it be a child or teen or an adult, these Quiz Games fascinate people of all age groups. In this article, we will make a simple Quiz Game using C programming language.

Functionalities of a Quiz Game
The Quiz Game program provides the following functionalities:

Store Questions
Randomly Pick One Question while playing
Check Answers if they are correct/wrong
Get the Final Score

Prerequisites: Basic knowledge of C, Control Statements, Arrays, Strings, Functions and Structures.

Components of the Quiz Game Program
The Quiz Game program is made up of the following major components:

1. Header Files and Macro Definitions
Include all the necessary header files that you are going to use in your program: Here we are using <stdio.h>, <stdlib.h>, <string.h>, and <time.h>
Use the define keyword to declare constants that you'll be using throughout your program. Here a constant "MAX_QUESTIONS" is defined to specify the maximum number of questions in the quiz. We are declaring MAX_QUESTIONS as 5 since we'll be having 5 questions in total for the quiz.
2. Question Structure
A structure named "Question" is defined to represent a quiz question containing the following fields:

question: It is declared as a string to store the question text.
options: It is a 2D array of strings to store the multiple-choice options.
correct_option: It is declared as an integer to store the index of the correct option (1-4).
3. displayQuestion() Function
This displayQuestion() function is defined for the purpose of displaying a quiz question. It takes a Question structure as an argument and prints the question text along with the answer options.
4. checkAnswer() Function
The checkAnswer() function is used to check whether a user's answer is correct or not. It also takes a Question structure and the user's answer as arguments and returns 1 if the answer is correct or returns 0 if the answer is incorrect.
5. main() Function
The main() function marks the beginning of the program. It means from here the program execution starts.
It initializes a random number generator using srand() based on the current time which is taken from <stdlib.h> header file.
An array of "original_questions" is defined which contains the quiz questions and their correct answers.
6. Randomized Questions
A copy of the original questions array ("original_questions") is created in the "questions" array. This copy will be used to randomize the order of questions.
The variable "num_questions" is set to "MAX_QUESTIONS", representing the total number of questions available.
Execution Flow of the Program
The program greets the user and then enters a loop to ask questions.
In each iteration of the loop:
A random index is generated to select a question from the remaining pool of questions. Since we have used srand as discussed earlier.
The selected question is displayed using the "displayQuestion" function.
The user is prompted to enter their answer (1-4).
The program checks if the answer is valid and within the range 1-4.
If the answer is valid, it checks if it's correct using the "checkAnswer" function and updates the user's score accordingly.
If the answer is incorrect, it displays the correct answer.
If the answer is invalid, it prompts the user to enter a valid choice.
The selected question is removed from the "questions" array by replacing it with the last question in the array, and "num_questions" is decremented.
After all questions have been asked, the program displays the user's score with a message of Well-Done Champ.
The program exits, ending the quiz game.
Overall, this program is determined to conduct a randomized quiz game with a fixed set of questions and multiple-choice answers to those questions. It provides feedback to the user on whether their answers are correct and keeps track of the score. The user's score is displayed at the end of the quiz with a message.
