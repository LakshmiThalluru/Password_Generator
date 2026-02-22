# Password_Generator
#password generator by using python
import random

letter = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
number = ['0','1','2','3','4','5','6','7','8','9']

symbols = ['!','#','$','%','&','(',')','*','+']

password_list = []

print("Welcome to password generator!")

n_letter = int(input("How many letters you want in your password?\n"))
n_symbols = int(input("How many symbols you want in your password?\n"))
n_number = int(input("How many numbers you want in your password?\n"))

# Add letters
for i in range(n_letter):
    char = random.choice(letter)
    password_list.append(char)

# Add symbols
for i in range(n_symbols):
    char = random.choice(symbols)
    password_list.append(char)

# Add numbers
for i in range(n_number):
    char = random.choice(number)
    password_list.append(char)

print("Before shuffle:", password_list)

# Shuffle the list
random.shuffle(password_list)

print("After shuffle:", password_list)

# Convert list to string
password = ""
for char in password_list:
    password += char

print("Your password is:", password)
