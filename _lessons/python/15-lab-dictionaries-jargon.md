---
  layout: post
  title: Lab - Python Dictionaries - Secret Language Translator
  language: python
---
It's super fun to have a secret language. Thankfully, Python makes it super easy to create a language and translate strings back and forth.

First, create a dictionary that maps words in English to words in your new language. A small example might be:

```python
{
'hello':'largig',
'goodbye':'lirgag',
'friend':'goorp',
'good':'trurp',
'see':'spelg'
'me':'ick',
'you':'mmmph'
}
```

Write a function to add a word pair to the dictionary. It should take two strings as parameters - the first to be the key (the english word), the second to be the value (the word in the new language). If the word already existed, update it. Don't return anything.

```python
add('walk','burble')
```

Write a lookup function. It should check whether a string has a translation in the dictionary - whether that key is in the dictionary's keys. Return the value if the key exists. Otherwise, return False.

```python
lookup('walk') #=> 'burble'
lookup('run') #=> False
```

Write a function to remove a word from the dictionary. It should return the word if the word was removed. If the word was not in the dictionary, return False.

```python
remove('good') #=> 'good'
remove('evil') #=> False
```

Write a translate function. It should take a string as a parameter and return a string with all the english words replaced. It should ignore capitalization, so both 'Hello' and 'hello' should become 'largig'

```python
translate("hello friend! It's good to see you.") #=> "largig goorp! It's trurp to spelg mmmph."
```

Modify your translate function so that it takes an optional dictionary parameter. The default value should be the dictionary you created. If a dictionary is passed in, that dictionary's keys and values should be used for translation.

```python
translate('hello friend!') #=>  'largig goorp!'
translate('hello friend!', {'hello':'molk','blarmfirts'}) #=> 'molk blarmfirts!'
```
