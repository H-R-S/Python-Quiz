# Python Quiz (Solved)

#### Python Assignments (Solved): [Python-Assignments]()

#### [Quiz: 01](https://github.com/H-R-S/Python-Quiz/blob/main/Quiz_01.md)
#### [Quiz: 02](https://github.com/H-R-S/Python-Quiz/blob/main/Quiz_02.md)
#### [Quiz: 03](https://github.com/H-R-S/Python-Quiz/blob/main/Quiz_03.md)

## [Quiz: 01](https://github.com/H-R-S/Python-Quiz/edit/main/Quiz_01.md)

Q1. Create a variable user_balance and set its value to 100. Simulate the user spending 20 dollars by updating the value of user_balance. What is the new value of user_balance?
### Code:
```
user_balance = 100
user_balance -= 20
print(user_balance)

```
### Output:
```
80
```

Q2. Create a Boolean variable is_logged_in and set its initial value to False. Simulate the user logging in by changing the value of is_logged_in to True. What is the new value of is_logged_in?
### Code:
```
is_logged_in = False
is_logged_in = True
print(is_logged_in)

```
### Output:
```
True
```

Q3. Create a variable product_rating and set its value to 4.2. Increase the value of product_rating by 0.3. What is the new value of product_rating?
### Code:
```
product_rating = 4.2
product_rating += 0.3
print(product_rating)

```
### Output:
```
4.5
```

Q4. Create a Boolean variable is_item_returned and set its initial value to False. Simulate the item being returned by changing the value of is_item_returned to True. What is the new value of is_item_returned?
### Code:
```
is_item_returned = False
is_item_returned = True
print(is_item_returned)

```
### Output:
```
True
```

Q5. Create a variable user_points and set its value to 50. Simulate the user earning 10 points by updating the value of user_points. What is the new value of user_points?
### Code:
```
user_points = 50
user_points += 10
print(user_points)

```
### Output:
```
60
```

Q6. Create a variable num_of_guests and set its value to 4. Simulate a guest leaving by decreasing the value of num_of_guests by 1. What is the new value of num_of_guests?
### Code:
```
num_of_guests = 4
num_of_guests -= 1
print(num_of_guests)

```
### Output:
```
3
```

Q7. Create a Boolean variable is_item_in_cart and set its initial value to False. Simulate a customer adding an item to their cart by changing the value of is_item_in_cart to True. What is the new value of is_item_in_cart?
### Code:
```
is_item_in_cart = False
is_item_in_cart = True
print(is_item_in_cart)

```
### Output:
```
True
```

Q8. Create a variable user_score and set its value to 85. Simulate the user achieving an additional 15 points by updating the value of user_score. What is the new value of user_score?
### Code:
```
user_score = 85
user_score += 15
print(user_score)

```
### Output:
```
100
```


Q9. Create a Boolean variable is_payment_made and set its initial value to True. Simulate a payment failure by changing the value of is_payment_made to False. What is the new value of is_payment_made?
### Code:
```
is_payment_made = True
is_payment_made = False
print(is_payment_made)

```
### Output:
```
False
```


Q10. Create a variable num_of_items and set its value to 10. Simulate the user adding 3 items to their cart by increasing the value of num_of_items by 3. What is the new value of num_of_items?
### Code:
```
num_of_items = 10
num_of_items += 3
print(num_of_items)

```
### Output:
```
13
```

## [Quiz: 02](https://github.com/H-R-S/Python-Quiz/blob/main/Quiz_02.md)

Q1. Problem Statement: You have been tasked with developing a simple todo list manager that allows a user to create and manage a list of tasks. The program should have the following functionalities:

• The ability to add a new task to the list

• The ability to display all tasks in the list

• The ability to mark a task as completed

• The ability to delete a task from the list

• The ability to exit the program

### Code:
```
tasks = []

while True:
    print("1. Add a new task")
    print("2. Display all tasks")
    print("3. Mark a task as completed")
    print("4. Delete a task")
    print("5. Exit")

    choice = input("Enter your choice (1-5): ")

    if choice == "1":
        task_name = input("Enter the task name: ")
        tasks.append({"name": task_name, "completed": False})
        print("Task added successfully!")
    elif choice == "2":
        print("Tasks:")
        for index, task in enumerate(tasks):
            print(f"{index+1}. {task['name']} - {'Completed' if task['completed'] else 'Incomplete'}")
    elif choice == "3":
        task_index = int(input("Enter the task number to mark as completed: "))
        tasks[task_index-1]["completed"] = True
        print("Task marked as completed!")
    elif choice == "4":
        task_index = int(input("Enter the task number to delete: "))
        del tasks[task_index-1]
        print("Task deleted successfully!")
    elif choice == "5":
        print("Exiting the program...")
        break
    else:
        print("Invalid choice. Please try again.")

```
### Output:
```
1. Add a new task
2. Display all tasks
3. Mark a task as completed
4. Delete a task
5. Exit
Enter your choice (1-5): 1
Enter the task name: quiz
Task added successfully!
1. Add a new task
2. Display all tasks
3. Mark a task as completed
4. Delete a task
5. Exit
Enter your choice (1-5): 3
Enter the task number to mark as completed: 1
Task marked as completed!
1. Add a new task
2. Display all tasks
3. Mark a task as completed
4. Delete a task
5. Exit
Enter your choice (1-5): 2
Tasks:
1. quiz - Completed
1. Add a new task
2. Display all tasks
3. Mark a task as completed
4. Delete a task
5. Exit
Enter your choice (1-5): 5
Exiting the program...

```

Q2. Problem Statement: You have been tasked with developing a simple word guessing game that allows a player to guess a secret word by entering individual letters. The program should have the following functionalities:

• The ability to read in a secret word from a file

• The ability to display the number of letters in the secret word

• The ability to allow the player to guess individual letters in the secret word

• The ability to keep track of the number of incorrect guesses made by the player

• The ability to display a message indicating whether the player has won or lost the game

• The ability to exit the game

### Code:
```
import random

words = ["pakistan", "iqra", "university", "python", "football", "quiz", "semester", "ramadan"]

def select_random_word(words):
    return random.choice(words)

def display_word(word, guessed_letters):
    output = ""
    for letter in word:
        if letter in guessed_letters:
            output += letter + " "
        else:
            output += "_ "
    return output.strip()

def play_game():
    secret_word = select_random_word(words)

    guessed_letters = set()
    incorrect_guesses = 0
    max_incorrect_guesses = 6

    print("Welcome to the word guessing game!")
    print(f"The secret word has {len(secret_word)} letters.")
    print(f"You have {max_incorrect_guesses} incorrect guesses before you lose the game.")

    while True:
        print(display_word(secret_word, guessed_letters))

        letter = input("Enter a letter: ").lower()

        if letter in guessed_letters:
            print("You already guessed that letter.")
        elif letter in secret_word:
            guessed_letters.add(letter)
            if set(secret_word) == guessed_letters:
                print(f"Congratulations, you won! The secret word was '{secret_word}'.")
                break
        else:
            guessed_letters.add(letter)
            incorrect_guesses += 1
            print(f"Sorry, '{letter}' is not in the secret word.")
            if incorrect_guesses == max_incorrect_guesses:
                print(f"Sorry, you lost. The secret word was '{secret_word}'.")
                break

    print("Thanks for playing!")

play_game()

```
### Output:
```
Welcome to the word guessing game!
The secret word has 8 letters.
You have 6 incorrect guesses before you lose the game.
_ _ _ _ _ _ _ _
Enter a letter: r
Sorry, 'r' is not in the secret word.
_ _ _ _ _ _ _ _
Enter a letter: p
Sorry, 'p' is not in the secret word.
_ _ _ _ _ _ _ _
Enter a letter: s
Sorry, 's' is not in the secret word.
_ _ _ _ _ _ _ _
Enter a letter: u
Sorry, 'u' is not in the secret word.
_ _ _ _ _ _ _ _
Enter a letter: f
f _ _ _ _ _ _ _
Enter a letter: o
f o o _ _ _ _ _
Enter a letter: o
You already guessed that letter.
f o o _ _ _ _ _
Enter a letter: t
f o o t _ _ _ _
Enter a letter: b
f o o t b _ _ _
Enter a letter: a
f o o t b a _ _
Enter a letter: l
f o o t b a l l
Enter a letter: l
You already guessed that letter.
f o o t b a l l
Enter a letter: j
Sorry, 'j' is not in the secret word.
f o o t b a l l
Enter a letter: x
Sorry, 'x' is not in the secret word.
Sorry, you lost. The secret word was 'football'.
Thanks for playing!

```

https://github.com/H-R-S/Python-Quiz/blob/main/Quiz_03.md?plain=1
