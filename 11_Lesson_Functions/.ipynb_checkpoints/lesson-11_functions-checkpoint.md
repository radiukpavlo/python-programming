[<< Lesson 10](../10_Lesson_Loops/lesson-10_loops.md)

- [📘 Lesson 11](#-lesson-11)
  - [Functions](#functions)
    - [Defining a Function](#defining-a-function)
    - [Declaring and Calling a Function](#declaring-and-calling-a-function)
    - [Function without Parameters](#function-without-parameters)
    - [Function Returning a Value - Part 1](#function-returning-a-value---part-1)
    - [Function with Parameters](#function-with-parameters)
    - [Passing Arguments with Key and Value](#passing-arguments-with-key-and-value)
    - [Function Returning a Value - Part 2](#function-returning-a-value---part-2)
    - [Function with Default Parameters](#function-with-default-parameters)
    - [Arbitrary Number of Arguments](#arbitrary-number-of-arguments)
    - [Default and Arbitrary Number of Parameters in Functions](#default-and-arbitrary-number-of-parameters-in-functions)
    - [Function as a Parameter of Another Function](#function-as-a-parameter-of-another-function)
  - [💻 Exercises: Lesson 11](#-exercises-lesson-11)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)

# 📘 Lesson 11

## Functions

So far we have seen many built-in Python functions. In this section, we will focus on custom functions. What is a function? Before we start making functions, let us learn what a function is and why we need them?

### Defining a Function

A function is a reusable block of code or programming statements designed to perform a certain task. To define or declare a function, Python provides the _def_ keyword. The following is the syntax for defining a function. The function block of code is executed only if the function is called or invoked.

### Declaring and Calling a Function

When we make a function, we call it declaring a function. When we start using the it,  we call it *calling* or *invoking* a function. Function can be declared with or without parameters.

```py
# syntax
# Declaring a function
def function_name():
    codes
    codes
# Calling a function
function_name()
```

### Function without Parameters

Function can be declared without parameters.

**Example:**

```py
def generate_full_name ():
    first_name = 'Asabeneh'
    last_name = 'Yetayeh'
    space = ' '
    full_name = first_name + space + last_name
    print(full_name)
generate_full_name () # calling a function

def add_two_numbers ():
    num_one = 2
    num_two = 3
    total = num_one + num_two
    print(total)
add_two_numbers()
```

### Function Returning a Value - Part 1

Function can also return values, if a function does not have a return statement, the value of the function is None. Let us rewrite the above functions using return. From now on, we get a value from a function when we call the function and print it.

```py
def generate_full_name ():
    first_name = 'Asabeneh'
    last_name = 'Yetayeh'
    space = ' '
    full_name = first_name + space + last_name
    return full_name
print(generate_full_name())

def add_two_numbers ():
    num_one = 2
    num_two = 3
    total = num_one + num_two
    return total
print(add_two_numbers())
```

### Function with Parameters

In a function we can pass different data types(number, string, boolean, list, tuple, dictionary or set) as a parameter

- Single Parameter: If our function takes a parameter we should call our function with an argument

```py
  # syntax
  # Declaring a function
  def function_name(parameter):
    codes
    codes
  # Calling function
  print(function_name(argument))
```

**Example:**

```py
def greetings (name):
    message = name + ', welcome to Python for Everyone!'
    return message

print(greetings('Asabeneh'))

def add_ten(num):
    ten = 10
    return num + ten
print(add_ten(90))

def square_number(x):
    return x * x
print(square_number(2))

def area_of_circle (r):
    PI = 3.14
    area = PI * r ** 2
    return area
print(area_of_circle(10))

def sum_of_numbers(n):
    total = 0
    for i in range(n+1):
        total+=i
    print(total)
print(sum_of_numbers(10)) # 55
print(sum_of_numbers(100)) # 5050
```

- Two Parameter: A function may or may not have a parameter or parameters. A function may also have two or more parameters. If our function takes parameters we should call it with arguments. Let us check a function with two parameters:

```py
  # syntax
  # Declaring a function
  def function_name(para1, para2):
    codes
    codes
  # Calling function
  print(function_name(arg1, arg2))
```

**Example:**

```py
def generate_full_name (first_name, last_name):
    space = ' '
      full_name = first_name + space + last_name
      return full_name
print('Full Name: ', generate_full_name('Asabeneh','Yetayeh'))

def sum_two_numbers (num_one, num_two):
    sum = num_one + num_two
    return sum
print('Sum of two numbers: ', sum_two_numbers(1, 9))

def calculate_age (current_year, birth_year):
    age = current_year - birth_year
    return age;

print('Age: ', calculate_age(2021, 1819))

def weight_of_object (mass, gravity):
    weight = str(mass * gravity)+ ' N' # the value has to be changed to a string first
    return weight
print('Weight of an object in Newtons: ', weight_of_object(100, 9.81))
```

### Passing Arguments with Key and Value

If we pass the arguments with key and value, the order of the arguments does not matter.

```py
# syntax
# Declaring a function
def function_name(para1, para2):
    codes
    codes
# Calling function
print(function_name(para1 = 'John', para2 = 'Doe')) # the order of arguments does not matter here
```

**Example:**

```py
def print_fullname(firstname, lastname):
    space = ' '
    full_name = firstname  + space + lastname
    print(full_name)
print(print_fullname(firstname = 'Asabeneh', lastname = 'Yetayeh'))

def add_two_numbers (num1, num2):
    total = num1 + num2
    print(total)
print(add_two_numbers(num2 = 3, num1 = 2)) # Order does not matter
```

### Function Returning a Value - Part 2

If we do not return a value with a function, then our function is returning _None_ by default. To return a value with a function we use the keyword _return_ followed by the variable we are returning. We can return any kind of data types from a function.

- Returning a string:
**Example:**

```py
def print_name(firstname):
    return firstname
print_name('Asabeneh') # Asabeneh

def print_full_name(firstname, lastname):
    space = ' '
    full_name = firstname  + space + lastname
    return full_name
print_full_name(firstname='Asabeneh', lastname='Yetayeh')
```

- Returning a number:

**Example:**

```py
def add_two_numbers (num1, num2):
    total = num1 + num2
    return total
print(add_two_numbers(2, 3))

def calculate_age (current_year, birth_year):
    age = current_year - birth_year
    return age;
print('Age: ', calculate_age(2019, 1819))
```

- Returning a boolean:
  **Example:**

```py
def is_even (n):
    if n % 2 == 0:
        print('even')
        return True    # return stops further execution of the function, similar to break 
    return False
print(is_even(10)) # True
print(is_even(7)) # False
```

- Returning a list:
  **Example:**

```py
def find_even_numbers(n):
    evens = []
    for i in range(n + 1):
        if i % 2 == 0:
            evens.append(i)
    return evens
print(find_even_numbers(10))
```

### Function with Default Parameters

Sometimes we pass default values to parameters, when we invoke the function. If we do not pass arguments when calling the function, their default values will be used.

```py
# syntax
# Declaring a function
def function_name(param = value):
    codes
    codes
# Calling function
function_name()
function_name(arg)
```

**Example:**

```py
def greetings (name = 'Peter'):
    message = name + ', welcome to Python for Everyone!'
    return message
print(greetings())
print(greetings('Asabeneh'))

def generate_full_name (first_name = 'Asabeneh', last_name = 'Yetayeh'):
    space = ' '
    full_name = first_name + space + last_name
    return full_name

print(generate_full_name())
print(generate_full_name('David','Smith'))

def calculate_age (birth_year,current_year = 2021):
    age = current_year - birth_year
    return age;
print('Age: ', calculate_age(1821))

def weight_of_object (mass, gravity = 9.81):
    weight = str(mass * gravity)+ ' N' # the value has to be changed to string first
    return weight
print('Weight of an object in Newtons: ', weight_of_object(100)) # 9.81 - average gravity on Earth's surface
print('Weight of an object in Newtons: ', weight_of_object(100, 1.62)) # gravity on the surface of the Moon
```

### Arbitrary Number of Arguments

If we do not know the number of arguments we pass to our function, we can create a function which can take arbitrary number of arguments by adding \* before the parameter name.

```py
# syntax
# Declaring a function
def function_name(*args):
    codes
    codes
# Calling function
function_name(param1, param2, param3,..)
```

**Example:**

```py
def sum_all_nums(*nums):
    total = 0
    for num in nums:
        total += num     # same as total = total + num 
    return total
print(sum_all_nums(2, 3, 5)) # 10
```

### Default and Arbitrary Number of Parameters in Functions

```py
def generate_groups (team,*args):
    print(team)
    for i in args:
        print(i)
print(generate_groups('Team-1','Asabeneh','Brook','David','Eyob'))
```

### Function as a Parameter of Another Function

```py
#You can pass functions around as parameters
def square_number (n):
    return n * n
def do_something(f, x):
    return f(x)
print(do_something(square_number, 3)) # 27
```

🌕 You achieved quite a lot so far.  Keep going! You have just completed lesson 11 and you are 11 steps a head in to your way to greatness. Now do some exercises for your brain and muscles.

## 💻 Exercises: Lesson 11

### Exercises: Level 1

1. Declare a function _add_two_numbers_. It takes two parameters and it returns a sum.
2. Area of a circle is calculated as follows: area = π x r x r. Write a function that calculates _area_of_circle_.
3. Write a function called _add_all_nums_, which takes arbitrary number of arguments and sums all the arguments. Check if all the list items are number types. If not, do give a reasonable feedback.
4. Temperature in °C can be converted to °F using this formula: °F = (°C x 9/5) + 32. Write a function which converts °C to °F, _convert_celsius_to_fahrenheit_.
5. Write a function called _check_season_. It takes a month parameter and returns the season: Autumn, Winter, Spring or Summer.
6. Quadratic equation is calculated as follows: ax² + bx + c = 0. Write a function which calculates solution set of a quadratic equation, _solve_quadratic_eqn_.
7. Declare a function named _print_list_. It takes a list as a parameter and it prints out each element of the list.
8. Declare a function named _capitalize_list_items_. It takes a list as a parameter and it returns a capitalized list of items.
9. Declare a function named _reverse_list_. It takes an array as a parameter and it returns the reverse of the array (use loops).

```py
print(reverse_list([1, 2, 3, 4, 5]))
# [5, 4, 3, 2, 1]
print(reverse_list1(["A", "B", "C"]))
# ["C", "B", "A"]
```

10. Declare a function named _add_item_. It takes a list and an item parameters. It returns a list with the item added at the end.

```py
food_staff = ['Potato', 'Tomato', 'Mango', 'Milk'];
print(add_item(food_staff, 'Meat'))     # ['Potato', 'Tomato', 'Mango', 'Milk','Meat'];
numbers = [2, 3, 7, 9];
print(add_item(numbers, 5))      [2, 3, 7, 9, 5]
```

### Exercises: Level 2

11. Declare a function named _sum_of_numbers_. It takes a number parameter and it adds all the numbers in that range.

```py
print(sum_of_numbers(5))  # 15
print(sum_all_numbers(10)) # 55
print(sum_all_numbers(100)) # 5050
```

12. Declare a function named _sum_of_odds_. It takes a number parameter and it adds all the odd numbers in that range.
13. Declare a function named _sum_of_even_. It takes a number parameter and it adds all the even numbers in that range.
14.  Declare a function named _evens_and_odds_. It takes a positive integer as parameter and it counts number of evens and odds in the number.

```py
    print(evens_and_odds(100))
    # The number of odds are 50.
    # The number of evens are 51.
```

15. Call your function _factorial_, it takes a whole number as a parameter and it return a factorial of the number.
16. Call your function _is_empty_, it takes a parameter and it checks if it is empty or not.
17. Write different functions which take lists. They should calculate_mean, calculate_median, calculate_mode, calculate_range, calculate_variance, calculate_std (standard deviation).
18. Write a functions called _unique_in_the_list_, which checks if all items are unique in the list.
19. Write a function called _valid_python_variable_, which check if provided variable is a valid python variable.
20. Go to the data folder and access the countries-data.py file.

- Create a function called _most_spoken_languages_ in the world. It should return 10 or 20 most spoken languages in the world in descending order
- Create a function called _most_populated_countries_. It should return 10 or 20 most populated countries in descending order.

🎉 CONGRATULATIONS ! 🎉

[Lesson 12 >>](../12_Lesson_Modules/lesson-12_modules.md)
