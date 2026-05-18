
![Logo](https://violet-raw-squirrel-412.mypinata.cloud/ipfs/bafybeiep33ifyvkykyvkwfb6eype5e5jjw3s7z5x42sg3et73mrm2lrmg4)


# Python Quiz Collection

This is collection of interactive Python quizzes designed to practice programming fundamentals and mathematical concepts.

This project is part of my journey to strengthen my data science skills by mastering core Python logic, problem-solving, and algorithm design.

It demonstrates skills in input/output, error handling, data structures, and algorithm design.


## Features

- Quiz 1: General knowledge quiz using dictionaries, loops, and conditionals

- Quiz 2: Number input and swapping exercise with error handling

- Quiz 3: Number classification (Prime, Armstrong, Palindrome)

- Quiz 4: Fibonacci sequence generator with input validation


## Used By

This project is designed for:

 - Beginners learning Python.
 - Data science learners building foundational skills.
 - Educators looking for teaching examples.
 - Coding enthusiasts who enjoy interactive challenges.
 
 It is also useful for interview candidates practicing logic-based questions.


## Lessons Learned

Practiced Python basics: input/output, loops, conditionals

Learned error handling with try/except

Implemented mathematical logic (prime, Armstrong, palindrome, Fibonacci)

Strengthened problem-solving and algorithm design skills

## Usage/Examples

```python
print("              QUIZ 1\n"
      "               ...\n"
      "               ...\n")

print("Welcome to JOSEPH GAMING QUIZ.")
username = input("   Please enter your username: ")
print(f"\nWelcome {username.capitalize()}.\nPlease proceed and provide the correct answer to the questions below\n")

# Dictionary and correct answer
questions = {"2 + 3 = ": "5", "Is the name 'JOHN' a male or a female name? (male/female) ": "male", "Can Birds fly? (yes/no) ": "yes", "Is Nigeria a country in Asia? (yes/no) ": "no", "Can dogs lay eggs? (yes/no) ": "no"}
point = 0 # init score

for question, answer in questions.items():
    print(question) # print my questions separately
    replies = input().lower() # collect case-insensitive reply from my game users
    if replies == answer.lower():
        point += 1
        print(f"Good job! Your current point is {point}\n")

    else:
        print(f"Incorrect answer! The correct answer is {answer}\n")

print("        .............................................")
print(f"Congratulations {username.upper()}, you got {point} points out of {len(questions)} questions correct on level 1.\n\n          Ready for some extra hard questions?\n")


print(          "QUIZ 2\n"
      "           ...\n"
      "           ...\n")

try:
    user_number_1 = int(round(float(input("enter your first number: "))))
    user_number_2 = int(round(float(input("enter your second number: "))))
    print(f"Your result are: {user_number_1} and {user_number_2}") #printing before swapping

    swapped_number = user_number_1, user_number_2 = user_number_2, user_number_1 # swapping with tuple
    print(f"Our swapped tupple is {swapped_number}")
except:
    print("Your value must be a number") # when user provides a non-numeric value, we get this feedback letting user know


print(          "QUIZ 3\n"
      "           ...\n"
      "           ...\n")

def is_prime_number(n): # check if the number is a prime
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

def is_amstrong_number(n): # check if the number is an armstrong
    digits = [int(d) for d in str(n)]
    return n == sum(d ** len(digits) for d in digits)

def is_palindrone_number(n): # check if the number is a palindrome
    return str(n) == str(n)[::-1]

try:
    number = int(input("Enter your proposed number to run a search if number is a prime, amstrong or palindrome number: "))
    results = []
# check the condition and print the one that is true
    if is_prime_number(number):
        results.append("Prime nuber")
    elif is_amstrong_number(number):
        results.append("Armstrong number")
    elif is_palindrone_number(number):
        results.append("Palindrome number")

    print(f"{number} is {', '.join(results)}" if results else f"{number} does not meet requirement.")

except ValueError:
    print("Invalid input. Please enter an integer") # handle any other result that doesnt fall under the scope



    print(          "QUIZ 4\n"
      "           ...\n"
      "           ...\n")

def fib(n):
    # To generate  the first nth term of the fib sequence
    sequence = [0, 1]
    for i in range(n - 2):
        sequence.append(sequence[-1] + sequence[-2])
    return sequence[:n] # return only the first n element

try:
        n = int(input("Enter a positive number to generate a fib sequence: "))

        if n <= 0:  # to validate the input
            print("Error, please entr a positive number!")
        else:
            print(f"fib sequence {fib(n)}")

except ValueError:
        print("Error, please enter a real number")

```


## Authors

- [@DataStudioHQ](https://www.github.com/DataStudioHQ)

