---
created: 2023-09-18T13:47:29+05:30
updated: 2023-09-18T13:47:29+05:30
---
# Simplified Flutter App Localization

The default way of accessing localized strings inside your widgets is to use the `AppLocalizations` class.

However, using the `!` operator everywhere is not good practice.

And it would be nice to have some more "lightweight" syntax.

A thread. 🧵

![](025-simplified-flutter-localization.png)

---

One issue we have is that `AppLocalizations.of(context)` returns a **nullable** object.

But at runtime this will never be null, as long as we call it inside a **descendant** of `MaterialApp` (which is always the case).

So what can we do?

![](025-app-localizations-of-context.png)

---

Dart extensions to the rescue!

We can define a `LocalizedBuildContext` extension with a `loc` getter variable defined like so:

![](025-localized-build-context-extension.png)

---

And now, whenever we need localized strings in our widgets, we can:

- import the file that defines the new extension
- use `context.loc.someString` to get the value we need

![](025-context-loc-widget.png)

---

If you have dozens or hundreds of localized strings, this amounts to a lot of developer happiness! 😀

If you found this thread useful, retweet the first tweet and spread the word. 🙏

Happy coding!

 
| Previous | Next |
| -------- | ---- |
| [The Gap Widget](../0023-the-gap-widget/index.md) | [How to run Flutter Integration Tests at Hyper Speed](../0025-how-to-run-flutter-integration-tests-at-hyper-speed/index.md) |