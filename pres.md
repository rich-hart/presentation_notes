# API Documentation
Rich Hart


## About OpenStax

OpenStax College is a nonprofit organization committed to improving student __access__ to quality learning materials (that are __readable__ and __accurate__).

## Accuracy / Readability / Accessibility

Good API documentation means taking these concepts into account in all levels of code. 

* Source Code
* Comments 
* Commit Messages
* ReadMe Files
* API Documentation

## How Users Read Documentation

__THEY DON'T!!!__ People rarely read web pages / documentation / source code word by word; instead, they scan the page, picking out individual words and sentences. 

__You can't expect that users will actually read any of your documentation__

Many users will try to copy and paste the exact contents of a code box into a text file or command prompt and expect it to run, without reading any of the surrounding comments.

You cannot assume your users have any context besides what you put in a code sample and maybe one or two sentences above or below.



## Source Code

### Strategies For Documentation

Web pages have to employ scannable text using:

*  Standardized formatting
*  Meaningful use of variables names and functions
*  Clear seperations of functions
*  I/O of functions stated in their descriptions

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

## Comments / Commit Messages

##### (See Karen's talk)

## ReadMe Files / API Documentation

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

## Other Thoughts

### Controversial Strategies For Documentation
 * Writing the documentation first will also help you program to an interface, not to an implementation.
 * ReadMe Driven Development

### Credits

* http://www.programmableweb.com/news/api-consumers-want-reliability-documentation-and-community/2013/01/07

* http://www.twilio.com/engineering/2012/01/18/dont-skimp-on-documentation

* https://sendgrid.com/blog/cheat-codes-for-good-documentation/

* http://www.nngroup.com/articles/how-users-read-on-the-web/
