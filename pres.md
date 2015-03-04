# API Documentation
Rich Hart

## About OpenStax

OpenStax College is a nonprofit organization committed to improving student access to quality learning materials (that are readable and accurate).

## Accuracy / Readability / Accessibility

Good API documentation means taking these three concepts into account in all levels of documentation. 
* Source Code
* Comments / Commit Messages
* ReadMe Files

## Source Code

Messy_Code.py

```python
letters = ['a','b','c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

print(''.join(letters))
```

Prints a concatenated string of letters.

__Pep8__ is a python style guide for formatting Python scripts.

```
$ pep8 MessyCode.py
MessyCode.py:2:80: E501 line too long (140 > 79 characters)
MessyCode.py:6:1: W391 blank line at end of file
```

__autopep8__ is a tool to format your code to pep8 standards. 

```
$ autopep8 MessyCode.py
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l',
           'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
print(''.join(letters))
```

