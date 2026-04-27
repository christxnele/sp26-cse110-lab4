# Part 2
1. Line 12 prints `3` because in the final iteration of the loop `i=3` which breaks the condition `i < prices.length` so it prints `3`. Also, since it was declared with var, `i` is function-scoped and escapes the for loop
2. Line 13 prints `150` which is the value of `discountedPrice` in the last iteration of the for loop. This is similar to line 12, `discountedPrice` was delcared with var, so it is function-scoped and escapes the for loop
3. Line 14 prints `150` which is the value of `finalPrice` in the last iteration of the for loop. This is similar to line 12, `finalPrice` was delcared with var, so it is function-scoped and escapes the for loop
4. The function returns the `discounted` array which is `[50, 100, 150]`. After calculating the `discountedPrice` and `finalPrice` each value is pushed into the array. Since there are no `console.log` statements, nothing is printed but the array is returned
5. Line 12 throws `ReferenceError: i is not defined` because `i` is now defined using `let`. This means `i` is block-scoped to the for loop and doesn't escape it.
6. Similar to Line 12, line 13 throws `ReferenceError: discountedPrice is not defined` because it is defined using `let` inside the for loop, is block-scoped and cannot escape.
7. Line 14 prints `150` because `finalPrice` was declared with `let` in the function scope, so it is visible and accessible in line 14 and prints the value of `finalPrice` after the final iteration.
8. The function returns the `discounted` array which is `[50, 100, 150]`. After calculating the `discountedPrice` and `finalPrice` each value is pushed into the array. Since there are no `console.log` statements, nothing is printed but the array is returned. `var` vs `let` doesn't affect the returned value in this case.
9.  Line 11 throws `ReferenceError: i is not defined` because `i` is defined using `let`. This means `i` is block-scoped to the for loop and doesn't escape it.
10. Line 12 prints `3` which is the length of the input array `prices`. `length` is declared with const in the function scope so it's accessible at line 12.
11. The function returns the `discounted` array which is `[50, 100, 150]`. After calculating the `discountedPrice`, each value is pushed into the array. Since there are no `console.log` statements, nothing is printed but the array is returned. `var` vs `let` vs `const` doesn't affect the returned value in this case.
12. PARTS A-E 
    1. PART A: `student.name` 
    2. PART B: `student['Grad Year']`
    3. PART C: `student.greeting()`
    4. PART D: `student['Favorite Teacher'].name`
    5. PART E: `student.courseLoad[0]`
13. PARTS A-H
    1.  PART A: `'3' + 2 = 32` because '3' is a string and the `+` acts as a string concatenation operator so `2` is forced to be a string, forming the string `32`
    2.  PART B: `'3' - 2 = 1`  because `-` operator has no string version so `'3'` is forced to be a number and does regular subtraction
    3.  PART C: `3 + null = 0` null is converted to `0` so `3 + null = 3 + 0 = 3`
    4.  PART D: similar to part A, `'3' + null = '3null'` because `null` is forced to be a string and the `+` acts as a string concatenation operator 
    5.  PART E: `true + 3 = 4` because `true` is forced to be number 1
    6.  PART F: `'false' + null = 0` since both `'false'` and `'null'` are forced to be 0
    7.  PART G:  similar to part A, `'3' + undefined  = '3undefined'` because `undefined` is forced to be a string
    8.  PART H: `'3' - undefined = NaN` because `undefined = NaN`  and any arithmetic with `NaN` returns `NaN`
14. PARTS A-F
    1.  PART A: `true` because `'2'` becomes the number 2 and `2 > 1` is true
    2.  PART B: `false` because the strings are compared lexicographically and it compares the first characters: `'2' and '1'` and `'2'` is conisdered greater
    3.  PART C: `true` because `'2'` gets converted to a number and `2==2` is true
    4.  PART D: `false` because `===` does strict equality with no type coercion and a string and number are never strictly equal
    5.  PART E: `false` because `true` is forced to be 1 and  `1 == 2` is false
    6.  PART F: `true` because `Boolean(2)` converts 2 to a boolean and since 2 is a truthy value, it becomes true, so we have `true === true`
15.  `==` is loose equality. it does type coercion before comparison  so values of diff types can be equal. `===` is strict equality with no type coercion, so both the value and type must match.
16.  see `part2-question16.js`
17.  `modifyArray([1,2,3], doSomething)` returns `[2, 4, 6]` because the function iterates over each element of `[1,2,3]` and applies the `doSomething` callback, which multiplies each element by 2. So `doSomething(1)=2`, `doSomething(2)=4`, `doSomething(3)=6`, and those results are pushed into a new array `[2, 4, 6]` which is returned
18.  see `part2-question18.js`
19.  The output is `1, 4, 3, 2`. Both `setTimeout` calls are asynchronous and get pushed to the event queue, so the synchronous statements run first printing `1` then `4`. Once the call stack is empty, the event loop processes the queued callbacks. The 0ms timeout fires first printing `3`, then the 1000ms timeout fires printing `2`