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
Deeply nested callbacks are bad because the code becomes hard to read and follow since everything keeps stacking inside other functions. It also makes debugging harder because you have to check multiple layers if something goes wrong.

Promise chaining helps make code cleaner by letting asynchronous tasks run in order using .then(). Instead of nesting logic, each .then() handles the next step, making the program easier to understand and maintain.
