# Chapter 2. Applescript in Principle



## Objects:

There are two kind of objects:

1. **AppleScript objects**: I think these are comparable to native data type in most language. like *number* type, *string* type, *list* type etc.
2. **Application objects**: I think these are a represantation of an application. It is an **application's model**. The *documentation* for application model is called **dictionary**

One of the tricks to mastering AppleScript is knowing what the similarities and differences are between *application* objects and *AppleScript* objects, and being able to tell which kind of object you’re dealing with at any point in your script.



## Commands

I think commands are like build-in methods in other language that operate on objects, for example, count the number charactor in a string object : 

```
count "Hello World!"
	--> 12
```

Another example is to count the number of item in a list:

```
count {2, 3, 17, 18, 43, 45}
	--> 6
```





## Operators

### Math operators:

```
1 + 2 
	--> 3
```

```
16 / 2.5
	--> 4.0
```

### Boolean oprators:

```
99 < 3.5 
  --> false
```

```
"HELLO" is equal to "hello"
	--> true
```

Note above `is equal to` does not distinguish cases.

### Concatenation

```
"Hello " & "World!"
	--> "Hello World!"
```

```
{2, 3, 17, 18, 43, 45} & {6} 
	--> {2, 3, 17, 18, 43, 45, 6}
```



## Variable assignment

```
set lucky_numbers to {2, 3, 17, 18, 43, 45}
```



## Flow control

### Conditional statements

```
if 2 + 2 is equal to 4 then 
	display dialog "Two plus two is four." 
end if
```

### Loops

```
repeat 15 times
	display dialog "Hello again!" 
end repeat
```

## Error handling

### try-catch

```
try 
	3 / 0 
on error
	display alert "Oops! Can't divide by zero." 
end try
```

## Function

Functions in Applescript are called **handlers**.

Handlers defination:

```
on square_root(the_number) 
	return the_number ^ 0.5 
end square_root
```

Call a handler:

```
square_root(25) 
	--> 5.0
```

