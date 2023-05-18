# Chapter 3. Applescript in practice



## Get current date object:

```applescript
current date
```

The above is a **command**, it returns the current date and time at run time.

*Result*:

```
date "Thursday, May 18, 2023 at 11:09:11"
```



## Property accessor `of`

```applescript
(date string) of (current date)
```

*Results*:

```
"Thursday, May 18, 2023"
```

*Explaination*: 

The keyword `of` let you access a property of an objects. 

In the above we are access the value of property `date string` in the `date` object.



## Expression

Expression is any piece of code that returns an object when evaluated. For example these are expression:

```applescript
"I am a string"       -- returns the string literal object "I am a string"
1 + 1                 -- returns the number 2
2 + 2 is equal to 4   -- returns a boolean true
```



## Parentheses

Parenthesis let you goup code into a single unit. As an example, the following won't work:

```
date string of current date
```

but the following will work:

```
date string of (current date)
```



### Assign an objact to a variable

```
set date_string to ((date string) of (current date))
```



## Concatenation operator `&`

```
"foo bar" & "ice cream"
```

```
"Desktop Archive for " & ((date string) of (current date))
```



## Constructing a folder name with date and assign it to a variable

```
set date_string to (date string of (current date))
set folder_name to ("Desktop Archive for " & date_string)
```











