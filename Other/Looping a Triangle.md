# Looping a Triangle

Eloquent JavaScript Exercise

---

Write a loop that makes seven calls to `console.log` to output following triangle

```
#
##
###
####
#####
######
```

---

## Pseudocode

Write a loop that calls `console.log` seven times and increments the number of `#` printed



* Initialize a for loop
  * Set the initalization variable to a string with the value `#`
  * Use the `.length` property on the variable to track the length of the string
    * Break the loop if the length is over 7
  * add `#` to the initialization string after every loop 
  * `console.log` the initialization string within the loop body 

## Solution

### JavaScript

```javascript
for(let pound = '#'; pound.length < 8; pound += '#') {{
  console.log(pound)
}}
```



`pound += '#'` is syntactic sugar for reassignment - `pound = pound + '#'` 