# Short Response Questions

## Question 1: Promise States

What are the three states of a Promise? For each state, explain what it represents and which Promise method (`.then()` or `.catch()`) is used to handle it.

**Your Answer:**

The three states of a Promise are:

Pending – The promise is still waiting for the operation to finish. It represents an ongoing asynchronous task. You don’t handle this state directly.

Fulfilled – The operation completed successfully and returned a result. You handle this state using `.then()`.

Rejected – The operation failed or an error occurred. You handle this state using `.catch()`.


## Question 2: Callback Hell vs. Promise Chaining

Explain why deeply nested callbacks (callback hell) are problematic, and describe how Promise chaining with `.then()` solves this problem.

**Your Answer:**

Deeply nested callbacks, or callback hell, are problematic because the code becomes difficult to read, understand, and debug. Each callback is nested inside the previous one. It makes error handling more complicated, since each nested callback may need its own `try/catch` or conditional checks. Promise chaining with `.then()` solves this by allowing `asynchronous` operations to be written in a flat, sequential manner. Each `.then()` handles the result of the previous step, keeping the code clean, readable, and making error handling easier with a single `.catch()`.

## Question 3: Error Handling with `.catch()`

If you have a chain of three `.then()` calls followed by a single `.catch()`, and the second `.then()` throws an error, what happens? Why is this behavior useful?

**Your Answer:**

When the second `.then()` throws an error, the third `.then()` gets skipped entirely and the error jumps straight to the `.catch()` at the end. The `.catch()` receives the error and handles it there.

This is useful because you only need one `.catch()` to handle errors from anywhere in the chain. Instead of writing separate error handling for every step, a single `.catch()` at the end catches whatever goes wrong, keeping the code clean and easy to manage.
