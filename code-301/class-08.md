# **API & RegEx**

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## SuperAgent

Code samples from: [https://visionmedia.github.io/superagent/](https://visionmedia.github.io/superagent/)

* ajax API

* light-weight, progressive

* flexibility, readability, low learning curve

```javascript
 request
   .post('/api/pet')
   .send({ name: 'Manny', species: 'cat' })
   .set('X-API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(res => {
      alert('yay got ' + JSON.stringify(res.body));
   });
```

### Request basics

```javascript
 request
   .get('/search')
   .then(res => {
      // res.body, res.headers, res.status
   })
   .catch(err => {
      // err.message, err.response
   });

    request
   .get('/search')
   .then(res => {
      // res.body, res.headers, res.status
   })
   .catch(err => {
      // err.message, err.response
   });
```

### Setting header fields

```javascript
 request
   .get('/search')
   .set('API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(callback);

 request
   .get('/search')
   .set({ 'API-Key': 'foobar', Accept: 'application/json' })
   .then(callback);
```

## RegEx

* created by gskinner.com
  
* hosted by Media Temple

Cheatsheet from [https://regexr.com/](https://regexr.com/):

```javascript
Character classes
.	any character except newline
\w\d\s	word, digit, whitespace
\W\D\S	not word, digit, whitespace
[abc]	any of a, b, or c
[^abc]	not a, b, or c
[a-g]	character between a & g
Anchors
^abc$	start / end of the string
\b\B	word, not-word boundary
Escaped characters
\.\*\\	escaped special characters
\t\n\r	tab, linefeed, carriage return
Groups & Lookaround
(abc)	capture group
\1	backreference to group #1
(?:abc)	non-capturing group
(?=abc)	positive lookahead
(?!abc)	negative lookahead
Quantifiers & Alternation
a*a+a?	0 or more, 1 or more, 0 or 1
a{5}a{2,}	exactly five, two or more
a{1,3}	between one & three
a+?a{2,}?	match as few as possible
ab|cd	match ab or cd
```

* Regular expressions are useful for extracting information from text

* search for matches of specific pattern

* validation

* parsing

* replacing strings

* web scraping

* translating data

### Basic topics

Cheatsheet from [https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285):

#### Anchors

```javascript
^The        matches any string that starts with The -> Try it!
end$        matches a string that ends with end
^The end$   exact string match (starts and ends with The end)
roar        matches any string that has the text roar in it
```

#### Quantifiers

```javascript
abc*        matches a string that has ab followed by zero or more c -> Try it!
abc+        matches a string that has ab followed by one or more c
abc?        matches a string that has ab followed by zero or one c
abc{2}      matches a string that has ab followed by 2 c
abc{2,}     matches a string that has ab followed by 2 or more c
abc{2,5}    matches a string that has ab followed by 2 up to 5 c
a(bc)*      matches a string that has a followed by zero or more copies of the sequence bc
a(bc){2,5}  matches a string that has a followed by 2 up to 5 copies of the sequence bc
```

#### Or Operator

```javascript
a(b|c)     matches a string that has a followed by b or c (and captures b or c) -> Try it!
a[bc]      same as previous, but without capturing b or c
```

#### Character Classes

```javascript
\d         matches a single character that is a digit -> Try it!
\w         matches a word character (alphanumeric character plus underscore) -> Try it!
\s         matches a whitespace character (includes tabs and line breaks)
.          matches any character -> Try it!
```

#### Flags

g - global

m - multi-line

i - insensitive

## Resources

[Documentation for SuperAgent](https://visionmedia.github.io/superagent/)

[RegExr](https://regexr.com/)

[Regex Tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)

[Regex 101](https://regex101.com/)