#quizz
import math
#python Quizz

Questions = [
    'What is the max possible len of an identifier in python?:',
    'len[\'Hello\',9,55,6.2,88.0]:',
    'What is the output print(math.pow(3,2))?:',
    'Creation of Anonymous functions at runtime,using constructor called as:',
    'Keyword of Function is! :',
    'Code snippet if x=1?  x<<2 :',
    'Whats the output  min(max(False,-3,-4),2,7):',
    'If S=56.236?     print(\'%.2f\'%x) :',
    'Pick the odd one:'
]

Options = [
    ('A.79 char', 'B.1 char', 'C.none of mentioned', 'D.31 char'),
    ('A.6', 'B.5', 'C.3', 'D.None'),
    ('A.8', 'B.6.0', 'C.9', 'D.9.0'),
    ('A.pi', 'B.Decorator', 'C.def', 'D.Lambda'),
    ('A.Mic', 'B.Def', 'C.Print', 'D.None'),
    ('A.4', 'B.0', 'C.8.2', 'D.1'),
    ('A.-5', 'B.False', 'C.2', 'D.None'),
    ('A.56.2', 'B.56.000', 'C.56.23', 'D.56.24'),
    ('A.Pass', 'B.Assert', 'C.Nonlocal', 'D.eval')
]

Answers = ['A', 'B', 'C', 'D', 'B', 'A', 'B', 'D', 'D']
Guesses = []
score = 0
question_num = 0

for question in Questions:
    print('-----------------------')
    print(question)
    for Option in Options[question_num]:
        print(Option)

    Guess = input('Enter (A,B,C,D):').upper()
    Guesses.append(Guess)
    if Guess == Answers[question_num]:
        score += 1
        print('CORRECT!')
    else:
        print('INCORRECT!')
        print(f'{Answers[question_num]} is the correct answer')
    question_num += 1

print('---------------------')
print('        RESULTS      ')
print("---------------------")

print('Answers:', end='')
for Answer in Answers:
    print(Answer, end=' ')
print()

print('Guesses:', end='')
for Guess in Guesses:
    print(Guess, end=' ')
print()

score = int(score / len(Questions) * 100)
print(f'Your score is: {score}%')
