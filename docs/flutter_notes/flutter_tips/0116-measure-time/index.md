---
created: 2023-09-18T13:38:47+05:30
updated: 2023-09-18T13:38:47+05:30
---
# Measuring execution time in Dart

Ever wanted to measure how long a network request takes in Dart?

This is easily done by creating a helper function that calculates the difference between two dates. 👇

![](116.1.png)

---

Then, you can wrap any asynchronous code block inside the function and reuse it as needed.

Very useful for benchmarking the execution time of your backend or database calls. 👌

![](116.2.png)



| Previous | Next |
| -------- | ---- |
| [Find the Invalid Switch Expression 🧐](../0115-switch-newline/index.md) | [Are global variables bad?](../0117-are-global-variables-bad/index.md) |
