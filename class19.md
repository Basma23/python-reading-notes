# Python Regular Expression 

Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. They are used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining.

**Regular Expressions in Python**

In Python, regular expressions are supported by the re module. The **re library** in Python provides several functions that make it a skill worth mastering.

**Basic Patterns: Ordinary Characters**

We can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

**Wild Card Characters: Special Characters**

Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like.

**Repetitions**

It becomes quite tedious if you are looking to find long patterns in a sequence. Fortunately, the re module handles repetitions using the following special characters:

```+``` - Checks if the preceding character appears one or more times starting from that position.

```*``` - Checks if the preceding character appears zero or more times starting from that position.

```?``` - Checks if the preceding character appears exactly zero or one time starting from that position.

**Grouping in Regular Expressions**

The ***group*** feature of regular expression allows us to pick up parts of the matching text. Parts of a regular expression pattern bounded by parenthesis ```()``` are called groups. The parenthesis does not change what the expression matches, but rather forms groups within the matched sequence. 

**Greedy vs. Non-Greedy Matching**

When a special character matches as much of the search sequence (string) as possible, it is said to be a "Greedy Match".

**Function provided by 're'**

The re library in Python provides several functions to make our tasks easier, such as the ```re.search()```, ```re.match()```.



# [Shutil](https://pymotw.com/3/shutil/)

The shutil module includes high-level file operations such as copying and archiving.



