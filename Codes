1. Digital Root Calculator
Write a program that keeps summing the digits of a number until only one digit remains.
Example: 942 → 9+4+2=15 → 1+5=6

def digital_root(n):
    while n > 9:  # keep going until it's a single digit
        n = sum(int(digit) for digit in str(n))
    return n

# Example usage
num = 942
print(f"Digital root of {num} is:", digital_root(num))


2. Sentence Word Replacer
Take a sentence from the user and replace all occurrences of the longest word with Python.

def replace_longest_with_python(sentence):
    words = sentence.split()
    longest_word = max(words, key=len)   # find the longest word
    replaced_sentence = sentence.replace(longest_word, "Python")
    return replaced_sentence

# Example usage
sentence = input("Enter a sentence: ")
print("Modified sentence:", replace_longest_with_python(sentence))


3. Pattern With Word
Ask the user for a word and print it in a pyramid shape.
Example for "CAT":

C  
C A  
C A T

def word_pyramid(word):
    for i in range(1, len(word) + 1):
        print(" ".join(word[:i]))

# Example usage
word = input("Enter a word: ")
word_pyramid(word)


4. Roman Numeral Converter
Convert an integer to its Roman numeral representation.
Example: 58 → LVIII

def int_to_roman(num):
    val = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1]
    syms = ["M", "CM", "D", "CD", "C", "XC", "L", "XL", "X", "IX", "V", "IV", "I"]
    
    roman_num = ""
    i = 0
    while num > 0:
        for _ in range(num // val[i]):
            roman_num += syms[i]
            num -= val[i]
        i += 1
    return roman_num

# Example usage
num = 58
print(f"Roman numeral for {num} is:", int_to_roman(num))


5. Find Hidden Message
Given a mixed string, extract only uppercase letters to reveal a hidden message.
Example: "heLLoPYthonWOrld" → "LLPYWO"

def hidden_message(text):
    return "".join([ch for ch in text if ch.isupper()])

# Example usage
msg = "heLLoPYthonWOrld"
print("Hidden message:", hidden_message(msg))


6. Reverse Words but Keep Order
Reverse every word in a sentence without changing the order of the words.
Example: "Python is fun" → "nohtyP si nuf"

def reverse_words(sentence):
    return " ".join(word[::-1] for word in sentence.split())

# Example usage
text = "Python is fun"
print("Modified sentence:", reverse_words(text))


7. File Extension Sorter
Given a list of file names, group them based on their extension.
Example:
["data.csv", "report.pdf", "image.png", "notes.txt", "code.py"]

from collections import defaultdict

def sort_by_extension(files):
    grouped = defaultdict(list)
    for file in files:
        name, ext = file.rsplit(".", 1)  # split from the right
        grouped[ext].append(file)
    return dict(grouped)

# Example usage
files = ["data.csv", "report.pdf", "image.png", "notes.txt", "code.py"]
sorted_files = sort_by_extension(files)

for ext, group in sorted_files.items():
    print(f".{ext} → {group}")


8. Custom Encryption
Shift every character in a string by 2 positions in ASCII (Caesar Cipher).
Example: "abc" → "cde"

def encrypt(text, shift=2):
    encrypted = "".join(chr(ord(ch) + shift) for ch in text)
    return encrypted

# Example usage
msg = "abc"
print("Encrypted text:", encrypt(msg))


9. Password Strength Checker
Check if a password is strong based on:

Minimum 8 characters

At least one uppercase, one lowercase, one digit, and one special character

import re

def check_password(password):
    if len(password) < 8:
        return "Weak: Must be at least 8 characters long"
    if not re.search(r"[A-Z]", password):
        return "Weak: Must contain at least one uppercase letter"
    if not re.search(r"[a-z]", password):
        return "Weak: Must contain at least one lowercase letter"
    if not re.search(r"\d", password):
        return "Weak: Must contain at least one digit"
    if not re.search(r"[@$!%*?&]", password):
        return "Weak: Must contain at least one special character (@$!%*?&)"
    return "Strong Password ✅"

# Example usage
passwords = ["hello123", "Hello123", "Hello@123"]
for pwd in passwords:
    print(f"{pwd} → {check_password(pwd)}")


10. Remove Consecutive Duplicates from String
Write a function that takes a string and removes any consecutive duplicate characters.

Example:
"aaabbcdddde" → "abcde"

def remove_consecutive_duplicates(s):
    result = s[0]  # start with first character
    for ch in s[1:]:
        if ch != result[-1]:  # only add if different from last char
            result += ch
    return result

# Example usage
text = "aaabbcdddde"
print("After removing duplicates:", remove_consecutive_duplicates(text))


11. Sentence Word Reversal (Preserve Punctuation)
Reverse the words in a sentence without changing punctuation positions.
Example:
"Hello, world!" → "world, Hello!"

import re

def reverse_words_with_punctuation(sentence):
    # Extract words only (ignoring punctuation)
    words = re.findall(r"\b\w+\b", sentence)
    words.reverse()
    
    result = ""
    word_index = 0
    
    for token in re.finditer(r"\b\w+\b|[^\w\s]", sentence):
        if token.group().isalnum():  # replace words
            result += words[word_index]
            word_index += 1
        else:  # keep punctuation
            result += token.group()
    
    return result

# Example usage
text = "Hello, world!"
print("Modified sentence:", reverse_words_with_punctuation(text))
