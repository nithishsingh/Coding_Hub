# Complete Guide on Python String
In the Article, we learn about string data type in python. we will discuss how to declare the strings data type, access characters in the string, slice techniques and methods that support strings.

Introduction to Python String

A string is an object that contains a sequence of characters. In python the character data type is absent, so a single character is also considered a string. However, we find the character data type in other programming languages like C and Java.

We can declare a python string using a single quote (' string'), a double quote ("string"), a triple quotes ("""string""") or the str() function.

# A single quote string
single_quote = 'a'  # This is an example of a character in other programming languages but it is a string in Python

# Another single quote string
another_single_quote = 'Programming teaches you patience.'

# A double quote string
double_quote = "Make sure you embarce it"

# Another double-quote string
another_double_quote = "It is impossible until it is done!"

# A triple quote string
triple_quote = '''Do small things with great love'''

# Also a triple quote string
another_triple_quote = """Welcome to the Python programming language. Ready, 1, 2, 3, Go!"""

# Using the str() function
string_function = str(123.45)  # str() converts float data type to string data type

# Another str() function
another_string_function = str(True)  # str() converts a boolean data type to string data type

# An empty string
empty_string = ''

# Also an empty string
second_empty_string = ""

# We are not done yet
third_empty_string = """"""  # This is also an empty string: ''''''


Strings can contain any character, such as letters, numbers, symbols, spaces, tabs, newlines, etc. Another way of getting a string in python is using the input() function allows us to get value from the user by default as a string, but we can convert them into other data types.

# Inputs into a Python program
input_float = input()  # Type in: 3.142 
input_boolean = input() # Type in: True

# Convert inputs into other data types
convert_float = float(input_float)  # converts the string data type to a float
convert_boolean = bool(input_boolean) # converts the string data type to a bool

We use the type() function to determine the data type of an object in Python. It returns the class of the object. When the object is a string, it returns the str class. Similarly, it returns dict, int, float, tuple, bool class when the object is a dictionary, integer, float, tuple, or Boolean, respectively. Let’s now use the type() function to determine the data types of variables declared in the previous code snippets:

print(type(single_quote))
print(type(another_triple_quote))
print(type(empty_string))

print(type(input_float))
print(type(input_boolean))

print(type(convert_float))
print(type(convert_boolean))

How to access characters in a string?

We can use square brackets [ ] to access individual characters or slices (substrings) of a string by specifying their index (position) within the string. Each character in a Python string is assigned an index, and the index starts with 0 and must be an integer. There are two ways of accessing the characters: 

using positive integers,

using negative integers.

For negative indexes, the index of -1 refers to the last item, -2 to the second last item, and so on. If you want to access a range of items in a string, you can use the slicing operator, :.

word = "Python"
print(word[:])   # Python
print(word[:4])  # Pyth (character from index 0 to index 3)
print(word[0])   # P
print(word[3])   # h
print(word[-1])  # n
print(word[-2])  # o
print(word[2:5]) # tho
print(word[::2]) # Pto
print(word[::-1]) # nohtyP one of reversing Technique

How to modify string?

Strings are immutable in Python, which means they cannot be changed once created. For example:

word = "Python"
word[0] = "J" # TypeError: 'str' object does not support item assignment

This will raise an error because we cannot assign a new value to an existing character in a string. However, we can create new strings by concatenating (joining) existing strings using the + operator or repeating them using the * operator. For example:

word = "Python"
new_word = "J" + word[1:] # Jython
another_word = word * 3 # PythonPythonPython

Python String Method

Python string methods allow developers to work with strings quickly and it does not the original string. Instead, it is used to return new values.

Some common built-in methods for strings with examples

greeting = "Welcome to   Opengenus"

# capitalize(): To convert the first character of a string to uppercase.
print(greeting.capitalize()) # Output: "Welcome to   Opengenus"

# casefold(): To convert a complete string into lowercase.
print(greeting.casefold()) # Output: "welcome to   Opengenus"

# center(): To get a centered string.
print(greeting.center(30)) # Output: "     Welcome to   Opengenus     "

# count(): To get the number of times a specified value occurs in a string.
print(greeting.count("e")) # Output: 3

# encode(): To get an encoded version of the string.
print(greeting.encode()) # Output: b'Welcome to   Opengenus'

#endswith(): To get a true value if the string ends with the specified value.
print(greeting.endswith("genus")) # Output: True

#expandtabs(): 	To set the tab size of the string.
greeting = "Welcome\tto\t  Opengenus"
print(greeting.expandtabs(4)) # Output: "Welcome to    Opengenus"
 
#find(): To search the string for a specified value and to get its position.
print(greeting.find("to")) # Output: 8

#format(): To format the specified values in a string.
name = "Nithish"
age = 25
greeting = "Hello, my name is {} and I am {} years old"
print(greeting.format(name, age)) # Output: "Hello, my name is Nithish and I am 25 years old"

# format_map(): To format the specified values in a string.
person = {'name': 'Nithish', 'age': 25}
greeting = "Hello, my name is {name} and I am {age} years old"
print(greeting.format_map(person)) # Output: "Hello, my name is Nithish and I am 25 years old"

# index(): To search the string for a specified value and to get its position.
greeting = "Welcome to   Opengenus"
print(greeting.index("Welcome")) # Output: 8

# isalnum(): To get a true value if all characters in the string are alphanumeric.
print(greeting.isalnum()) # Output: False

# isalpha(): To get a true value if all characters in the string are alphabets.
print(greeting.isalpha()) # Output: False

# isdecimal(): To get a true value if all characters in the string are decimals.
print(greeting.isdecimal()) # Output: False

# isdigit(): To get a true value if all characters in the string are digits.
print(greeting.isdigit()) # Output: False

# isidentifier(): To get a true value if the string is an identifier.
print(greeting.isidentifier()) # Output: False

# islower(): To get a true value if all characters in the string are lower case.
print(greeting.islower()) # Output: True
 
# isnumeric(): To get a true value if all characters in the string are numeric.
print(greeting.isnumeric()) # Output: False

# isprintable(): To get a true value if all characters in the string are printable.
print(greeting.isprintable()) # Output: True

# isspace(): To get a true value if all characters in the string are whitespaces.
greeting = "   "
print(greeting.isspace()) # Output: True

# istitle(): To get a true value if the string follows the rules of a title.
print(greeting.istitle()) # Output: True

# isupper(): To get a true value if all characters in the string are uppercase.
print(greeting.isupper()) # Output: True

# join(): To join the elements of an iterable to the end of the string.
separator = ', '
fruits = ['Welcome', 'To', '  Opengenus']
result = separator.join(fruits)
print(result)  #Output: 'Welcome, To,   Opengenus'

# len(): To return the length of a string.
length = len(greeting)
print(length)  #Output: 20

# ljust(): To return a left justified version of the string. 
result = greeting.ljust(30)
print(result)  # Output: 'Welcome to   Opengenus '

#lower(): To convert a string into lowercase.
result = greeting.lower()
print(result)  # Output: 'welcome to   Opengenus'

# lstrip(): To return a left trim version of the string.  
greeting = '    Welcome to   Opengenus    '
result = greeting.lstrip()
print(result)   # Output: 'Welcome to   Opengenus '

# maketrans(): To return a translation table to be used in translations.
table = greeting.maketrans('o', '0')
result = greeting.translate(table)
print(result)   # Output: 'Welc0me t0 0pengenus'

# partition(): To return a tuple where the string is parsed into three parts.
result = greeting.partition('to')
print(result)  # Output: ('Welcome ', 'to', '   Opengenus')

# replace(): To return a string where a specified value is replaced with a specified value.
result = greeting.replace('  Opengenus', 'Python')
print(result)   # Output: 'Welcome to Python'

# rfind(): To search the string for a specified value and to get its last position.
position = greeting.rfind('o')
print(position)  # Output: 14

# rindex(): To search the string for a specified value and to get its last position.
position = greeting.rindex('o')
print(position)  # Output: 14

# rpartition(): To return a tuple where the string is parsed into three parts.
result = greeting.rpartition('to')
print(result)   # Output: ('Welcome ', 'to', '   Opengenus')

# rsplit(): To split the string at the specified separator, and to get a list.
result = greeting.rsplit(' ')
print(result)   # Output: ['Welcome', 'to', '  Opengenus']

# rstrip(): To return a right trim version of the string.
greeting = '    Welcome to   Opengenus    '
result = greeting.rstrip()
print(result)    # Output: ' Welcome to   Opengenus'
 
# strip(): To remove any whitespace from the beginning or the end of the string.
greeting = '    Welcome to   Opengenus    '
result = greeting.strip()
print(result)   # Output: 'Welcome to   Opengenus'

# split(): To split the string at the specified separator, and to get a list.
result = greeting.split(' ')
print(result)   # Output: ['Welcome', 'to', '  Opengenus']

# splitlines() - split the string at line breaks and get a list
lines = "Hello\nWorld\n"
print(lines.splitlines())  # Output: ['Hello', 'World']

# startswith() - check if the string starts with the specified value
print(greeting.startswith("Welcome"))  # Output: True
print(greeting.startswith("Goodbye"))  # Output: False

# swapcase() - swap lowercase to uppercase and vice versa
print(greeting.swapcase())  # Output: wELCOME TO   Opengenus

# title() - convert the first character of each word to uppercase
print(greeting.title())  # Output: Welcome To   Opengenus

# translate() - get a translated string
table = greeting.maketrans("W", "w")
print(greeting.translate(table))  # Output: welcome to   Opengenus

# upper() - convert a string into uppercase
print(greeting.upper())  # Output: WELCOME TO   Opengenus

# zfill() - fill the string with a specified number of 0 values at the beginning
number = "42"
print(number.zfill(5))  # Output: 00042

End Notes

Thanks for reading!

I hope that you have enjoyed the article. If you like it, share it with your friends also. Something not mentioned or want to share your thoughts? Feel free to comment below And I’ll get back to you
