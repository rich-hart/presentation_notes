# API Documentation
Rich Hart


## About OpenStax

OpenStax College is a nonprofit organization committed to improving student __access__ to quality learning materials (that are __readable__ and __accurate__).

API documentation is an intrinsic part of fulfilling out mission statement. 

## Accuracy / Readability / Accessibility

Good API documentation means taking these concepts into account in all levels of code. 

* __Source Code__
* Comments 
* Commit Messages
* ReadMe Files
* __REST API Documentation__

## How Users Read Documentation

__THEY DON'T!!!__ People rarely read web pages / documentation / source code word by word; instead, they scan the page, picking out individual words and sentences. 

__You can't expect that users will actually read any of your documentation__

Many users will try to copy and paste the exact contents of a code box into a text file or command prompt and expect it to run, without reading any of the surrounding comments.

You cannot assume your users have any context besides what you put in a code sample and maybe one or two sentences above or below.

- Kevin Burke

## How Developers Write Documentation

__WE DON'T!!!__ ... Unless forced or threatened.

Just like quick-and-dirty coding decisions can lead to technical debt, poor documentation can lead to operational debt.

You also need to dedicate time in your product development cycle to writing documentation good enough so that users can figure out your product.

__Good documentation is an engineering problem and needs to be a prioritized__

## ReadMe Driven Development *

A ReadMe file is to ReadMe Driven Developement as a unit test is to test driven developement

Write your Readme first while you're still excited about the project.

Writing the documentation first will also help you program to an interface, not to an implementation.

\* Might be controversial. 

## Source Code

### Strategies For Documentation

*  Standardized formatting
*  Meaningful use of variables names and functions
*  Seperation of tasks
*  Code that translates into english
*  Meaningful is more valuable than clever

### Example

##### MessyCode.py

```python
letters = ['a','b','c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

print(''.join(letters))
```

Prints a concatenated string of letters.

##### Pep8

A python style guide for formatting Python scripts.

```sh
$ pep8 MessyCode.py
MessyCode.py:2:80: E501 line too long (140 > 79 characters)
MessyCode.py:6:1: W391 blank line at end of file
```

You can also link pep8 with git to see you changes in relation to another branch.

```sh
git diff [branch_1] [branch_2] | pep8 --diff
```

##### AutoPep8

A tool to format your code to pep8 standards. 

```sh
$ autopep8 MessyCode.py
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l',
           'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
print(''.join(letters))
```

##### Clever vs Meaningful

```python
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l',
           'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
print(''.join(letters))
```

vs

```python
import string

letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l',
           'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

null_character = ''

concat_string = string.join(letters, null_character)

print(concat_string)
```

## API Documentation

### Strategies For Documentation

Web pages have to employ scannable text using:
*  highlighted keywords (hypertext links serve as one form of highlighting; typeface variations and color are others)
*  meaningful sub-headings (not "clever" ones)
*  bulleted lists
*  the inverted pyramid style, starting with the conclusion

### Categories of Documentation

* Descriptive
* Technical Reference & Code
* Tutorials
* Interactive

### Examples

* http://apidocjs.com/
* https://github.com/Connexions/cnx-archive/blob/master/search_api_doc.rst

### Credits

* http://www.programmableweb.com/news/api-consumers-want-reliability-documentation-and-community/2013/01/07

* http://www.twilio.com/engineering/2012/01/18/dont-skimp-on-documentation

* https://sendgrid.com/blog/cheat-codes-for-good-documentation/

* http://www.nngroup.com/articles/how-users-read-on-the-web/

* http://tom.preston-werner.com/2010/08/23/readme-driven-development.html
