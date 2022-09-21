# FizzBuzz

https://www.codecademy.com/code-challenges/code-challenge-fizzbuzz-javascript

---

Write a `fizzbuzz()` function that takes in a number, `n`, and returns an array of the numbers from 1 to `n`. For multiples of three, use `"Fizz"` instead of the number, and for the multiples of five, use `"Buzz"`. For numbers that are multiples of both three and five, use `"FizzBuzz"` (capitalization matters).

For example, `fizzbuzz(16)` should return `[1, 2, 'Fizz', 4, 'Buzz', 'Fizz', 7, 8, 'Fizz', 'Buzz', 11, 'Fizz', 13, 14, 'FizzBuzz', 16]`.

---



## PEDAC

Input: integer

Output: array of integers and strings 

* Take the input and return an array of the numbers from 1..`n`
* Subsitute multiples of 3 with "Fizz"
* Subsitute multiples of 5 with "Buzz"

* Subsitute multiples of 3 and 5 with "Fizz"



1. Initialize a `counter` variable assign it the value `1`
2. Initialize an empty array `arr`
3. Initiate a `while` loop. Break when `counter` variable is >= input
   1. Initialize `str` variable and assign it an empty str - within the loop so it gets rest to `''` each iteration
   2. If `counter` variable is a multiple of 3 push 'Fizz' to the `str` variable
   3. If `counter` variable is a multiple of 5 push 'Buzz' to the `str` variable
   4. If `str` variable is empty push the `counter` variable to `arr` else push the `str` variable
   5. Increment `counter`
4. Return `arr`



## Solution

### JavaScript

```javascript
function fizzbuzz(n) {
  let counter = 1
  const array = []
  
  while(counter <= n) {
    let str = ''
    if(counter % 3 === 0) str+='Fizz' 
    if(counter % 5 === 0) str +='Buzz'
    if (str) {
      array.push(str)
    } else {
      array.push(counter)
    }
    counter += 1
  }
return array
}

// Leave this line for testing:
module.exports = fizzbuzz;
```