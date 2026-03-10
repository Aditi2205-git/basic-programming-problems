# basic-programming-problems
Practical Assignment(25-02-26)
# Basic Programming Problems (JavaScript)

# 1. Fibonacci Series

## Question

Write a program to print the Fibonacci series up to `n` terms.

## Approach

* The Fibonacci sequence starts with `0` and `1`.
* Each next number is the **sum of the previous two numbers**.
* Use a loop to generate the sequence.

## Solution

```javascript
function fibonacci(n) {
    let a = 0, b = 1;

    for (let i = 1; i <= n; i++) {
        console.log(a);

        let next = a + b;
        a = b;
        b = next;
    }
}

fibonacci(10);
```

---

# 2. Sum of Total Digits in a Number

## Question

Write a program to calculate the **sum of all digits** in a given number.

Example
Input: `1234`
Output: `10`

## Approach

* Convert the number into digits.
* Use modulus `% 10` to extract the last digit.
* Add digits one by one.
* Divide the number by `10` each step.

## Solution

```javascript
function sumOfDigits(num) {

    let sum = 0;

    while (num > 0) {
        sum += num % 10;
        num = Math.floor(num / 10);
    }

    console.log("Sum of digits:", sum);
}

sumOfDigits(1234);
```

---

# 3. Palindrome Number

## Question

Write a program to check whether a number is a **Palindrome**.

Example
Input: `121`
Output: `Palindrome`

## Approach

* Reverse the digits of the number.
* Compare the reversed number with the original number.

## Solution

```javascript
function isPalindrome(num) {

    let original = num;
    let reversed = 0;

    while (num > 0) {

        let digit = num % 10;
        reversed = reversed * 10 + digit;
        num = Math.floor(num / 10);

    }

    if (original === reversed) {
        console.log("Palindrome");
    } else {
        console.log("Not Palindrome");
    }
}

isPalindrome(121);
```

---

# 4. Print Triangle Pattern

## Question

Write a program to print the following triangle pattern:

```
*
**
***
****
*****
```

## Approach

* Use nested loops.
* The outer loop controls the number of rows.
* The inner loop prints stars.

## Solution

```javascript
function printTriangle(rows) {

    for (let i = 1; i <= rows; i++) {

        let pattern = "";

        for (let j = 1; j <= i; j++) {
            pattern += "*";
        }

        console.log(pattern);
    }
}

printTriangle(5);
```

---

# 5. Factorial of a Number

## Question

Write a program to find the **factorial** of a number.

Example
`5! = 5 × 4 × 3 × 2 × 1 = 120`

## Approach

* Initialize a variable `result = 1`.
* Multiply the result with numbers from `1` to `n`.

## Solution

```javascript
function factorial(n) {

    let result = 1;

    for (let i = 1; i <= n; i++) {
        result *= i;
    }

    console.log("Factorial:", result);
}

factorial(5);
```

---

