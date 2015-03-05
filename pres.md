# API Documentation
Rich Hart


## Fundimentals of OpenStax's Mission

OpenStax College is a nonprofit organization committed to improving student  __access__ to quality learning materials (that are __readable__ and __accurate__).

We should also be committed to improving __developer__ __access__ to code that is __readable__ and __accurate__.

API documentation is an intrinsic part of fulfilling our mission statement. 

## Accuracy / Readability / Accessibility

Good API documentation means taking these concepts into account in all levels of code. 

* __Source Code__
* Comments 
* Commit Messages
* ReadMe Files
* __REST API Documentation__


<!---
http://xkcd.com/1296/

Give a dolar line
-->
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

__Good documentation is an engineering problem and needs to be prioritized__

## ReadMe Driven Development *

A ReadMe file is to ReadMe Driven Developement as a unit test is to test driven developement

Write your Readme first while you're still excited about the project.

Writing the documentation first will also help you program to an interface, not to an implementation.

\* Might be controversial. 

## Categories of Documentation

* Descriptive
* Technical Reference & Code
* Tutorials
* Interactive

## Source Code Documentation

### Strategies

*  Standardized formatting
*  Seperation of tasks
*  Meaningful use of variables names and functions
*  Code that translates into english

### Python Example

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

## REST API Documentation

### Strategies

* Follow a standardized template for all web APIs
* Sample calls and responses are especially useful

### Examples

##### APIDOC

Allows REST APIs to be documented within sourse code comments.

```python
def postUser():
"""
 @api {post} /user Create a new User
 @apiVersion 0.3.0
 @apiName PostUser
 @apiGroup User
 @apiPermission none
 
 @apiDescription In this case "apiErrorStructure" is defined and used.
 Define blocks with params that will be used in several functions, so you dont have to rewrite them.
 
 @apiParam {String} name Name of the User.
 
 @apiSuccess {Number} id         The new Users-ID.
 
 @apiErrorStructure CreateUserError
"""
```

* http://apidocjs.com/example/

##### CNX-Archive

* https://github.com/Connexions/cnx-archive/blob/master/search_api_doc.rst

### Credits

* http://bocoup.com/weblog/documenting-your-api/

* http://www.programmableweb.com/news/api-consumers-want-reliability-documentation-and-community/2013/01/07

* http://www.twilio.com/engineering/2012/01/18/dont-skimp-on-documentation

* https://sendgrid.com/blog/cheat-codes-for-good-documentation/

* http://www.nngroup.com/articles/how-users-read-on-the-web/

* http://tom.preston-werner.com/2010/08/23/readme-driven-development.html
