String filters are used to manipulate outputs and variables of the string type.

##### Directory

* [append](#append)
* [camelcase](#camelcase)
* [capitalize](#capitalize)
* [downcase](#downcase)
* [strip](#strip)
* [lstrip](#lstrip)
* [rstrip](#rstrip)
* [prepend](#prepend)
* [remove](#remove)
* [remove_first](#remove_first)
* [replace](#replace)
* [replace_first](#replace_first)
* [strip_html](#strip_html)
* [truncate](#truncate)
* [truncatewords](#truncatewords)
* [upcase](#upcase)


## append
Appends characters to a string.
##### Input
```jinja
{{ 'sales' | append('.jpg') }}
```
##### Output
```html
sales.jpg
```

---

## camelcase
Converts a string into CamelCase.
##### Input
```jinja
{{ 'coming-soon' | camelcase }}
```
##### Output
```html
ComingSoon
```

---

## capitalize
Capitalizes the first word in a string
##### Input
```jinja
{{ 'capitalize me' | capitalize }}
```
##### Output
```html
Capitalize me
```

---

## downcase
Converts a string into lowercase.
##### Input
```jinja
{{ 'UPPERCASE' | downcase }}
```
##### Output
```html
uppercase
```

---

## strip
Strips tabs, spaces, and newlines (all whitespace) from the left side of a string.
##### Input
```jinja
{{ '   too many spaces           ' | strip }}
```
##### Output
```html
too many spaces
```


---

## lstrip
Strips tabs, spaces, and newlines (all whitespace) from the left side of a string.
##### Input
```jinja
{{ '   too many spaces           ' | lstrip }}
```
##### Output
```html
<!-- Highlight to see the empty spaces to the right of the string -->
too many spaces
```

---

## rstrip
Strips tabs, spaces, and newlines (all whitespace) from the right side of a string.
##### Input
```jinja
{{ '              too many spaces      ' | rstrip }}
```
##### Output
```html
<!-- Notice the empty spaces to the left of the string -->
              too many spaces
```

---

## prepend
Prepends characters to a string.
##### Input
```jinja
{{ 'sale' | prepend('Made a great ') }}
```
##### Output
```html
Made a great sale
```

---

## remove
Removes all occurrences of a substring from a string.
##### Input
```jinja
{{ 'Hello, world. Goodbye, world.' | remove('world') }}
```
##### Output
```html
Hello, . Goodbye, .
```

---

## remove_first
Removes only the first occurrence of a substring from a string.
##### Input
```jinja
{{ 'Hello, world. Goodbye, world.' | remove_first('world') }}
```
##### Output
```html
Hello, . Goodbye, world.
```

---

## replace
Replaces all occurrences of a string with a substring.
##### Input
```jinja
<!-- product.title = "Awesome Shoes" -->
{{ product.title | replace('Awesome', 'Mega') }}
```
##### Output
```html
Mega Shoes
```

---

## replace_first
Replaces the first occurrence of a string with a substring.
##### Input
```jinja
<!-- product.title = "Awesome Awesome Shoes" -->
{{ product.title | replace_first('Awesome', 'Mega') }}
```
##### Output
```html
Mega Awesome Shoes
```

---

## strip_html
Strips all HTML tags from a string.
##### Input
```jinja
{{ '<h1>Hello</h1> World' | strip_html }}
```
##### Output
```html
Hello World
```

---

## truncate
Truncates a string down to the number of characters passed as the first parameter. An ellipsis (...) is appended to the truncated string and is included in the character count.
##### Input
```jinja
{{ 'The cat came back the very next day' | truncate(13) }}
```
##### Output
```html
The cat ca...
```

---

## truncatewords
Truncates a string down to the number of characters passed as the first parameter. An ellipsis (...) is appended to the truncated string and is included in the character count.
##### Input
```jinja
{{ 'The cat came back the very next day' | truncatewords(4) }}
```
##### Output
```html
The cat came back...
```

---

## upcase
Converts a string into uppercase.
##### Input
```jinja
{{ 'i want this to be uppercase' | upcase }}
```
##### Output
```html
I WANT THIS TO BE UPPERCASE
```

---