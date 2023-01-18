[<< Lesson 5](../05_Lesson_Lists/lesson-05_lists.md)

- [Lesson 6:](#lesson-6)
  - [Tuples](#tuples)
    - [Creating a Tuple](#creating-a-tuple)
    - [Tuple length](#tuple-length)
    - [Accessing Tuple Items](#accessing-tuple-items)
    - [Slicing tuples](#slicing-tuples)
    - [Changing Tuples to Lists](#changing-tuples-to-lists)
    - [Checking an Item in a Tuple](#checking-an-item-in-a-tuple)
    - [Joining Tuples](#joining-tuples)
    - [Deleting Tuples](#deleting-tuples)
  - [💻 Exercises: Lesson 6](#-exercises-lesson-6)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)

# 💻 Lesson 6:

## Tuples

A tuple is a collection of different data types which is ordered and unchangeable (immutable). Tuples are written with round brackets, (). Once a tuple is created, we cannot change its values. We cannot use add, insert, remove methods in a tuple because it is not modifiable (mutable). Unlike list, tuple has few methods. Methods related to tuples:

- tuple(): to create an empty tuple
- count(): to count the number of a specified item in a tuple
- index(): to find the index of a specified item in a tuple
- + operator: to join two or more tuples and to create a new tuple

### Creating a Tuple

- Empty tuple: Creating an empty tuple
  
  ```py
  # syntax
  empty_tuple = ()
  # or using the tuple constructor
  empty_tuple = tuple()
  ```

- Tuple with initial values
  
  ```py
  # syntax
  tpl = ('item1', 'item2','item3')
  ```

**Example:**

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  ```

### Tuple length

We use the _len()_ method to get the length of a tuple.

```py
# syntax
tpl = ('item1', 'item2', 'item3')
len(tpl)
```

### Accessing Tuple Items

- Positive Indexing
  Similar to the list data type we use positive or negative indexing to access tuple items.
  
![Accessing tuple items](../images/tuples_index.png)

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3')
  first_item = tpl[0]
  second_item = tpl[1]
  ```

**Example:**

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  first_fruit = fruits[0]
  second_fruit = fruits[1]
  last_index =len(fruits) - 1
  last_fruit = fruits[las_index]
  ```

- Negative indexing
  Negative indexing means beginning from the end, -1 refers to the last item, -2 refers to the second last and the negative of the list/tuple length refers to the first item.
  
![Tuple Negative indexing](../images/tuple_negative_indexing.png)

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  first_item = tpl[-4]
  second_item = tpl[-3]
  ```

**Example:**

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  first_fruit = fruits[-4]
  second_fruit = fruits[-3]
  last_fruit = fruits[-1]
  ```

### Slicing tuples

We can slice out a sub-tuple by specifying a range of indexes where to start and where to end in the tuple, the return value will be a new tuple with the specified items.

- Range of Positive Indexes

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  all_items = tpl[0:4]         # all items
  all_items = tpl[0:]         # all items
  middle_two_items = tpl[1:3]  # does not include item at index 3
  ```

**Example:**

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  all_fruits = fruits[0:4]    # all items
  all_fruits= fruits[0:]      # all items
  orange_mango = fruits[1:3]  # doesn't include item at index 3
  orange_to_the_rest = fruits[1:]
  ```

- Range of Negative Indexes

  ```py
  # Syntax
  tpl = ('item1', 'item2', 'item3','item4')
  all_items = tpl[-4:]         # all items
  middle_two_items = tpl[-3:-1]  # does not include item at index 3 (-1)
  ```

**Example:**

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  all_fruits = fruits[-4:]    # all items
  orange_mango = fruits[-3:-1]  # doesn't include item at index 3
  orange_to_the_rest = fruits[-3:]
  ```

### Changing Tuples to Lists

We can change tuples to lists and lists to tuples. Tuple is immutable if we want to modify a tuple we should change it to a list.

```py
# Syntax
tpl = ('item1', 'item2', 'item3','item4')
lst = list(tpl)
```

**Example:**

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
fruits = list(fruits)
fruits[0] = 'apple'
print(fruits)     # ['apple', 'orange', 'mango', 'lemon']
fruits = tuple(fruits)
print(fruits)     # ('apple', 'orange', 'mango', 'lemon')
```

### Checking an Item in a Tuple

We can check if an item exists or not in a tuple using _in_, it returns a boolean.

```py
# Syntax
tpl = ('item1', 'item2', 'item3','item4')
'item2' in tpl # True
```

**Example:**

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
print('orange' in fruits) # True
print('apple' in fruits) # False
fruits[0] = 'apple' # TypeError: 'tuple' object does not support item assignment
```

### Joining Tuples

We can join two or more tuples using + operator

```py
# syntax
tpl1 = ('item1', 'item2', 'item3')
tpl2 = ('item4', 'item5','item6')
tpl3 = tpl1 + tpl2
```

**Example:**

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
vegetables = ('Tomato', 'Potato', 'Cabbage','Onion', 'Carrot')
fruits_and_vegetables = fruits + vegetables
```

### Deleting Tuples

It is not possible to remove a single item in a tuple but it is possible to delete the tuple itself using _del_.

```py
# syntax
tpl1 = ('item1', 'item2', 'item3')
del tpl1

```

**Example:**

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
del fruits
```

🌕 You are so brave, you made it to this far. You have just completed lesson 6 challenges and you are 6 steps a head in to your way to greatness. Now do some exercises for your brain and for your muscle.

## 💻 Exercises: Lesson 6

### Exercises: Level 1

1. Create a tuple containing names of your sisters and your brothers (imaginary siblings are fine).
2. Join _brothers_ and _sisters_ tuples and assign it to siblings.
3. Modify the _siblings_ tuple and add the name of your father and mother and assign it to _family_members_.
4. Unpack siblings and parents from _family_members_.
5. Create _fruits_, _vegetables_ and _animal_ products tuples. Join the three tuples and assign it to a variable called _food_stuff_tp_.

### Exercises: Level 2

6. Change the about _food_stuff_tp_  tuple to a _food_stuff_lt list_.
7. Slice out the middle item or items from the _food_stuff_tp_ tuple or _food_stuff_lt_ list.
8. Slice out the first three items and the last three items from _food_staff_lt_ list.
9. Delete the _food_staff_tp_ tuple completely.
10. Check if an item exists in the tuple:

- Check if 'Estonia' is a nordic country;
- Check if 'Iceland' is a nordic country;

  ```py
  nordic_countries = ('Denmark', 'Finland','Iceland', 'Norway', 'Sweden')
  ```

🎉 CONGRATULATIONS ! 🎉

[lesson 7 >>](../07_Lesson_Sets/lesson-07_sets.md)