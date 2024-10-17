# 05 Password Generator

The **PyPassword Generator** is the **Day 05 Challenge** from Dr. Angela Yu's 100 Days of Code: Python Pro Bootcamp. This project demonstrates the following skills:
- For Loops with Python Lists
- Sum Function
- Range Function

## Project Description

Three versions of the password generator were created, each progressively more refined, leading to the final robust solution.

### Option 1: Basic Version
This first version constructs the password by randomly selecting a defined number of letters, symbols, and numbers and appending them directly to the password string.

#### Key Features:
- Use of `random.choice()` to select random characters.
- Constructs the password in a simple manner, but lacks shuffling.

```py
for char in range(1, nr_letters + 1):
    password += random.choice(letters)
# Repeats the process for symbols and numbers.
```

### Option 2: Refined Logic
The second version improves slightly on the first by refining the use of loops, with better control over indices and improved readability.

#### Key Features:
- Similar to Option 1 but uses `range(0, nr_)` for more intuitive indexing.
- Constructs the password without shuffling.

```py
for char in range(0, nr_letters):
    password += random.choice(letters)
# Similarly loops through symbols and numbers.
```

### Option 3: Final Version (with Shuffling)
The final version is the most refined solution, where all the characters (letters, symbols, and numbers) are selected and added to a list. Afterward, the list is shuffled to ensure a random distribution of the password characters before being converted into a string.

#### Key Features:
- Uses `random.shuffle()` to shuffle the password characters, enhancing security.
- More flexible and robust design compared to earlier versions.

```py
password_list = []
# Characters are appended to the list, then shuffled.
random.shuffle(password_list)
# Convert the list back to a string for the final password.
```

## Concepts Assessed
- **For Loops:** Used for iterating through ranges to append random characters.
- **Random Module:** To generate random choices for letters, symbols, and numbers.
- **List Operations:** Working with lists to append items, shuffle them, and convert them into a final password string.

## Running the Program
1. Run the program and input the desired number of letters, symbols, and numbers.
2. The generator will return a random password that meets the specified criteria.

## Example Output

```
Welcome to the PyPassword Generator!
How many letters would you like in your password?
5
How many symbols would you like?
2
How many numbers would you like?
3
Your password is: g$2A9f*D1
```

---
<section align="center">
  <code>coderBri © 2024</code>
</section>