---
created: 2023-09-18T13:55:34+05:30
updated: 2023-09-18T13:55:34+05:30
---
# The Gap Widget

Did you know?

You can easily add gaps inside Flex widgets such as Columns and Rows or scrolling views.

Just install the `gap` package, and replace all those pesky SizedBoxes!

![](024-gap-widget.png)

---

You can find the package here:

https://pub.dev/packages/gap

Credit to [@lets4r](https://twitter.com/lets4r) for making it.

---

This caused some confusion, so I'll try to clear it up.

There is **NOTHING** wrong with `SizedBox`.

`Gap(x)` is a valid substitute for both `SizedBox(width: x)` and `SizedBox(height: x)`, because it works **along** the main axis of the parent widget.

---

Of course, it's a package so it adds an extra dependency to your project.

If you feel it's not justified, don't use it. Again, `SizedBox` is **just fine**.

If you like the shorter syntax and not having to specify width/height, go for it.

YOU choose.

 

| Previous | Next |
| -------- | ---- |
| [App Development workflow in 6 steps](../0022-app-development-workflow-in-six-steps/index.md) | [Simplified Flutter App Localization](../0024-simplified-flutter-app-localization/index.md) |