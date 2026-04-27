# Part 1

1. Line 9 prints `values added: 20` because `add` is `true` and the if block runs so result is set to `10+10=20`
2. Line 13 prints `final result: 20` because `result` is declared with var, so it is visible across the whole function. It escapes the if block and is accessible at line 13, so it keeps the value `20`
3. You should not use `var` because it is function-scoped and not block-scoped. So variables declared with `var` inside `if` statements or `for` loops can be visible outside of those blocks. This can cause unexpected behavior and bugs.
4. Line 9 prints `values added: 20` because `result` was declared using `let` so it is accessible at line 9 and holds teh value `20`
5.  Throws `ReferenceError: result is not defined` because `result` was declared with `let`. It is block-scoped to the if block and cannot be accessed outside of it at line 13.
6.  Line 9 isn't reached because line 8 throws `TypeError: Assignment to constant variable.` because `result` was declared with `const`. `result` cannot be reassigned after its initial value of 0
7.  Similar to line 9, line 13 is also never reached because of the `TypeError` in line 7