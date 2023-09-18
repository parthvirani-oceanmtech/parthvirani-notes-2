---
created: 2023-09-18T13:56:14+05:30
updated: 2023-09-18T13:56:14+05:30
---
# `AsyncValue` vs `FutureBuilder` & `StreamBuilder`

If you've been using Flutter for some time, you'll know that `FutureBuilder` & `StreamBuilder` help you deal with asynchronous data in your UI.

But working with `AsyncSnapshot` is quite tricky, and the AsyncValue class from the Riverpod package makes life much easier.

A thread. 🧵

![](035.1-async-snapshot-vs-async-value.png)

---

Let's take a peek at the definition of AsyncSnapshot.

This is a class that defines four properties:

- `connectionState`
- `data`
- `error`
- `stackTrace`

These properties are all **independent** from each other.

![](035.2-async-snapshot.png)

---

But what we really want are three **mutually exclusive** states:

- data
- loading
- error

And that's exactly what AsyncValue gives us, by defining them with some factory constructors:

![](035.3-async-value-def.png)

---

On top of that, we also get an AsyncValueX extension with a "when" method that we can use to map all possible states to our UI.

This technique is called **pattern matching**, and means that we don't need to rely on if/else clauses like we do when working with AsyncSnapshot.

![](035.4-async-value-usage.png)

---

Time to put things together.

You can create a `StreamProvider` that returns any method or function that returns a stream with a matching type.

Then you can declare a `ConsumerWidget` and **watch** the provider, ensuring that the widget will rebuild whenever there's a new value.

![](035.5-async-value-full.png)

---

That's all. You can now say bye-bye to all your `StreamBuilder`s and `FutureBuilder`s, and use `StreamProvider` & `FutureProvider` with `AsyncValue` instead.

---

I have covered state management with Riverpod in great detail in my new Flutter course:

- [The Complete Flutter Course Bundle](https://codewithandrea.com/courses/complete-flutter-bundle/)

And for more Flutter tips, just follow me: [@biz84](https://twitter.com/biz84)

Happy coding!

 

| Previous | Next |
| -------- | ---- |
| [How to use `WidgetsBindingObserver`](../0034-how-to-use-widgetsbindingobserver/index.md) | [GoRouter: `go` vs `push`](../0036-gorouter-go-vs-push/index.md) |