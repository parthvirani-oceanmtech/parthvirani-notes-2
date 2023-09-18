---
created: 2023-09-18T13:46:59+05:30
updated: 2023-09-18T13:46:59+05:30
---
# Repositories as abstract classes (program to interfaces, not implementations)

"Program to interfaces, not implementations" is a very important concept in software design.

It is used to decouple your code from implementation-specific details.

A good use case for this is when creating repositories that connect to external data sources:

![](022_repositories_abstract_classes.png)

---

Once you have an interface (abstract class), you can **implement** it with a concrete implementation.

You can even create a "fake", which can be very useful in your tests.

![](022-real-vs-fake-impl.png)

---

During app startup, you can initialize your repository with a **concrete** instance (using a service locator or any other dependency injection system).

And the rest of your app can just access the repository using the base abstract class.

![](022-registration-usage.png)

---

What are the benefits?

- You can swap your real repository with a completely different implementation - the rest of your code doesn't change at all
- You can mock the repository in your tests, so that they run faster and more reliably

Follow me for more tips like this: [@biz84](https://twitter.com/biz84)

  

| Previous | Next |
| -------- | ---- |
| [How to configure multiple Firebase environments with FlutterFire CLI](../0020-how-to-configure-multiple-firebase-environments-with-flutterfire-cli/index.md) | [App Development workflow in 6 steps](../0022-app-development-workflow-in-six-steps/index.md) |