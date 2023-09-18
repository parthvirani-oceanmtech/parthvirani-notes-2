---
created: 2023-09-18T13:42:05+05:30
updated: 2023-09-18T13:42:05+05:30
---
# Using `serverTimestamp()` in Firestore

Sometimes it's useful to add a timestamp to documents in Firestore, so they can be ordered later.

For that, prefer using `serverTimestamp()`.

This always uses the UTC time standard, and is more reliable that using `DateTime.now()` on the client.

![](089.1.png)

---

In your serialization code, you can then use `Timestamp.toDate()` and `Timestamp.fromDate()` to get the corresponding `DateTime`.

Note that two snapshots will be emitted:
- immediately with a null timestamp
- again with a non-null timestamp once the document is written to the server

![](089.2.png)
 

| Previous | Next |
| -------- | ---- |
| [The Accessibility Tools package](../0088-list-single/index.md) | [Using `context.mounted` in Flutter 3.7](../0090-context-mounted/index.md) |