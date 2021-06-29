# Python Regular Expression
- Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not.

#### Regular Expressions in Python:
- In Python, regular expressions are supported by the re module.

- The re library in Python provides several functions that make it a skill worth mastering. You will see some of them closely in this tutorial.

#### Wild Card Characters: Special Characters:
- Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like.

#### Repetitions:
- It becomes quite tedious if you are looking to find long patterns in a sequence. Fortunately, the re module handles repetitions using the following special characters:

+ - Checks if the preceding character appears one or more times starting from that position.

#### Grouping in Regular Expressions:
- The group feature of regular expression allows you to pick up parts of the matching text. Parts of a regular expression pattern bounded by parenthesis () are called groups.

#### Greedy vs. Non-Greedy Matching:
- When a special character matches as much of the search sequence (string) as possible, it is said to be a "Greedy Match".

#### Compilation Flags:
- An expression's behavior can be modified by specifying a flag value. You can add flags as an extra argument to the different functions that you have seen in this tutorial.


#### shutil — High-level File Operations:
- The shutil module includes high-level file operations such as copying and archiving.

#### Copying Files:
- copyfile() copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.

#### Copying File Metadata:
- By default when a new file is created under Unix, it receives permissions based on the umask of the current user. To copy the permissions from one file to another, use copymode().

#### Working With Directory Trees:
- shutil includes three functions for working with directory trees. To copy a directory from one place to another, use copytree(). It recurses through the source directory tree, copying files to the destination. The destination directory must not exist in advance.