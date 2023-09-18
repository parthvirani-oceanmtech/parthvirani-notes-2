---
created: 2023-09-18T13:56:53+05:30
updated: 2023-09-18T13:56:53+05:30
---
# Adding a Custom Test timeout

Did you know?

When writing tests in Flutter, you can add a custom timeout argument.

This is very useful for tests that can potentially hang (when waiting on an asynchronous stream matcher). 👇

If you have many tests running on CI, this can save you a lot of time and money! 💰

![](052.1-test-timeout.png)

---

You know what else is cool?

Custom timeouts can be configured per-file, per-test, or per-group, just like this. 👇

![](052.2-test-timeout.png)
 
| Previous | Next |
| -------- | ---- |
| [Golden Image Testing with Robot Testing](../0051-golden-image-testing-with-robot-testing/index.md) | [How to Create DartPad Examples from GitHub Gists](../0053-how-to-create-dartpad-examples-from-github-gists/index.md) |
