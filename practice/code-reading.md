# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.
=> Because line 4 is block scope and line 6 is global scope.

## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.
=> console.log(f1()) output will be: 10 as x defined outside the function is accessed by it. console.log(y) output will be undefined as y is only block scope and is not defined outside the function.

## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x);
console.log(x);

const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);
```

What will be the output of this code. Explain your answer in 50 words or less.
=> f1(x) output will be 10 because f1(x) takes x=9 as an argument returns 10 while and console.log(x) output will be 9 as that is what x is defined. 

=> f2(y) output will be {x:10} the object y's property x value is changed by the function f2. Output of console.log(y) will be {x:9} as this is just logging the y defined earlier.