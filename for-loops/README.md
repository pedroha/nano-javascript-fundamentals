## For & While Loops

The two loops that are primarily used are known as the **for** loop and **while** loop.

Say you wanted to write

```
1
2
3
4
5
```

To do this, you one would normally type.

```javascript
    document.write("1");
    document.write("2");
    document.write("3");
    document.write("4");
    document.write("5");
```

This is a tedious process when you have to write 100, or 1000 numbers. Instead we can do the following.


```javascript
    for (var i = 1; i <= 5; i++) {
        document.write(i + "<br/>");
    }
    
    var i = 1;
    while (i <= 5) {
        document.write(i + "<br/>");
        i += 1; // can also be written as i = i + 1; or i++;
    }
```

There are three parts to the loop. The first part `var i = 1` is known as the instantiation. This is where you declare or start the variable. `i` is typically used, but you can use anything, `var x = 0` or `var hello = 0`. Name the variable something that makes sense.

The second part is known as the conditional. Basically, each time a loop runs, it will check to this condition to see if it is **true** or **false**. If it is true, it will execute the content in the **block**, otherwise it will exit the loop.

The third part is the incrementor. Here you typically use it to increment the variable you set in the first part (the instantiation). 

### Example 1:
*Printing 1 through 10*

**Code**
```javascript
    for (var i = 1; i <= 10; i++) {
        document.write(i + "<br/>");
    }
```

**Output**
```
1
2
3
4
5
6
7
8
9
10
```

### Example 2:
*Print even numbers from 1 through 10*

```javascript
    // one way to do it
    for (var i = 1; i <= 10; i++) {
        document.write(i * 2 + "<br/>");
    }
    
    // another way to do it
    for (var i = 2; i <= 20; i+=2) {
        document.write(i + "<br/>");
    }
    
    // using a while loop and modulus operator. 
    var i = 1;
    while (i < 20) {
        if (i % 2 == 0) {
            document.write(i + "<br/>");
        }
    }
```

What is modulus? It's basically known as the remainder of a value if it were to be divided.  

```
2 % 1 = 0
10 % 2 = 0
5 % 2 = 1
10 % 3 = 1
10 % 8 = 2
```

So let's explore this a bit further.

```
Example 1: 2 % 1
2 / *1* = **2**
2 - (**2** * *1*) = 0

Example 2: 5 % 2
5 / *2* = **2** *(ignore the decimal)*
5 - (**2** * *2*) = 1
```