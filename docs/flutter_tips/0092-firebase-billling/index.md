---
created: 2023-09-18T13:41:59+05:30
updated: 2023-09-18T13:41:59+05:30
---
# Firebase Billing and Cost Calculator

Did you know that Firebase offers a pricing calculator that you can use to estimate your monthly costs?

The free tier is so generous that you'd have to get past 1.5M Cloud Firestore *monthly* reads before being charged a penny. 😌

But how can you check your actual usage?

🧵

![](092.1-firebase-pricing-calculator.png)

---

Most Firebase products (Authentication, Cloud Firestore etc.) include a "Usage" tab where you can see a breakdown of your billable metrics. 👇

![](092.2-billable-metrics.png)

---

And if you go to "Usage and Billing", you can see your total project cost.

I couldn't take a screenshot with a good-looking chart here, since nearly all my projects cost ZERO. 😅

![](092.3-cost.png)

---

For extra peace of mind, you can go to your Google Cloud account to set a monthly budget amount.

And you can also receive email alerts when the forecasted spend exceeds a certain percent or amount.


![](092.4-budget-alerts.png)

---

So don't be scared about your Firebase bill. 🤝

Unless you do something catastrophic, you'll be fine. 🙌

Just be careful to avoid recursive document writes in your Cloud Function triggers. 😱

And even then, budget limits and alerts should help you out. ⚠️

---

I'm working on a brand new course about Flutter & Firebase that will be released in the coming months.

If you wanna learn Firebase, you can check it out and signup for the waitlist to get a big discount. 👇

- [Flutter & Firebase Masterclass](https://codewithandrea.com/courses/flutter-firebase-masterclass/)

 
| Previous | Next |
| -------- | ---- |
| [Got linter issues? Use `dart fix --apply`](../0091-dart-fix-apply/index.md) | [Add a part file with Riverpod Snippets](../0093-riverpod-part/index.md) |

