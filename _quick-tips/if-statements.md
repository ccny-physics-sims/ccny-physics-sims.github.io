---
title: About if Statements

---

## About `if` Statements

An `if` statement, otherwise known as a conditional, tell the program to check _if something is true_, then, based on that assessment, do something. Nearly every programming language has such structures. In javascript, they look like:

```
if (something is true) {
  do this stuff!
}
```

the *conditional* goes in the parenthesis, then in the curly brackets, we put the stuff to do.

An example: we'll check if I'm over 35 years old. If so, we'll tell my program to call the function where I gain 10 pounds.

```javascript
if (myAge > 35) {
  gainWeight(10)
}
```

We can put a lot of things inside the conditional statement. These are all types of *comparisons*.

- `>` greater than
- `<` less than
- `==` equal to (yes, there are two equal signs there)
- `!=` not equal to
- `>=` greater than _or_ equal to
- `<=` less than _or_ equal to
