# 🔑 Building Core Sign-Up Functions to Help Validate New Users

## 🎯 Objective

Implement a function called `validate_name()`, that takes in one parameter, which will be a datatype of string to check the user has inputted a valid name.

- The function should check that the user has inputted a name that is a data type of string.
- The function should check that the name is greater than two characters long.
- The function should return a boolean value, `True` if the name is valid, and `False` if not.

Implement a function called `validate_email()`, that takes in one parameter, which will be a datatype of string to check the user has inputted a valid email.

- The function should check that the user has inputted an email that contains an `'@'` symbol.
- The function should check that the email contains any top-level domain included in the `top_level_domains` list variable. This has been preloaded to the workbook for you.
- The function should return a boolean value, `True` if the name is valid, and `False` if not.