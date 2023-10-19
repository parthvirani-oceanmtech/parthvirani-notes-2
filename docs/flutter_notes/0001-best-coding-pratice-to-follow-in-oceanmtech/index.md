---
created: 2023-09-15T21:33:06+05:30
updated: 2023-10-19T11:44:05+05:30
title: Best Coding Practice to Follow in Oceanmtech
share: "true"
---

1. Kyarey setState use nathi karavanu always proper state managment use karvanu che.
2. State managment mate bloc(preferred) or provider bemathi aek j use karvanu rehshe.
3. Never use getx for state managment.
	- Disadvantages: ([Ref: Medium](https://shirsh94.medium.com/beyond-the-hype-the-untold-truth-about-getx-and-its-downsides-for-flutter-development-2c0b0b9b2fb5))
		 - Getx Provide Simplicity
		- GetX force to replacing Flutter
		- GetX tends to use anti-patterns
		- GetX tries to do everything
		- The level of documentation for GetX needs improvement.
		- The Unusual Number of API Elements in GetX.

4. Follow proper project architecture(MVC(Medium Project) or MVVM(Large Project))
5. Official Documentation Read karvanu aavdvu jove and ae must required skills che.
6. Effective Dart Programming Writing Style: 
	- Saro code write karvo and ae sari code pratice che and most important points che.
	- Consistent naming, ordering and format maintain karvathi ae code no look maintain thay shake che.
	- powerful pattern-matching hardware mate saru pade ke pattern match kari ne aapane suggestion provide kari aape (AI - Github Copilot)
	- and jo consistent code style hoy aakha dart na ecosystem mate to batha mate easier reshe ke aemathi shikhva mate and aek bija na code ma contributation karva mate.
	- and Oceanmtech aa code nu structure maintain karvu ae mandotory che je ne aapde universal code structure na rules par thi j aapde define karel che.
	- Aapde official dart language ni guide ne follow karvanu che:
	- [Dart Programming Writing Rules](https://dart.dev/effective-dart/style#formatting) (Read & Implement karvanu che)   
7. OceanMTech na aek pan flutter developer ne jyare code write karta hoy tyare keyboard same jovu na padvu jove aena mate typing speed mate ni daily pratice karvani che and biju keyabord and mouse ni click fast action ma perform thay ae mandatory che.
8. Jyare code write karo cho aena file name and file location always yad rakhvana and aej rite function name variable name ae pan yad rakhvana and aena name pan function na according j lakhvana jenathi jyare ae module nu logic update thay tyare direct file name par thi ae file par jay shakay because jyare projects ma 1000 files hoy tyare manually find karvi ae time consuming process che.

### 9. Use Descriptive Variable and Function Names { #use-descriptive-variable-and-function-names}

koi pan variables, functions, classes and widget na name descriptive choose karvana reshe, je aapane code vadhu samajavama and bija pan easy way ma samji shake and in future aapde aa project par return work start karvi to samajava mate easy reshe. so single-letter or cryptic variable names ne avoid karvu jaruri che, nichenu exaple refer karvu more details mate.

#### More in details:

"Use Descriptive Variable and Function Names" is a fundamental coding practice that involves choosing meaningful and informative names for variables, functions, methods, classes, and other identifiers in your code. The goal is to make your code more readable, self-explanatory, and maintainable by conveying the purpose and functionality of these elements through their names. This practice is crucial in Dart and Flutter development, as it enhances code understanding and collaboration. Here's why it's important and how to implement it effectively:

**Why Use Descriptive Names**:

1. **Code Readability**: Clear and descriptive names make your code more readable and easier to understand for both yourself and other developers who may work on the project.

2. **Intent Clarification**: Well-chosen names help convey the intent and purpose of variables, functions, and classes, reducing the need for extensive comments.

3. **Documentation Reduction**: Descriptive names can replace or reduce the need for comments, as they provide self-documentation by describing what the code does.

4. **Maintenance**: During maintenance or debugging, descriptive names can significantly reduce the time it takes to understand the code and locate potential issues.

5. **Collaboration**: When working on a team, using descriptive names ensures that team members can understand and collaborate on code more effectively.

**How to Use Descriptive Names Effectively**:

1. **Choose Meaningful Names**:
   - Select names that accurately represent the purpose and role of the variable, function, class, or method.
   - Avoid generic or cryptic names like `x`, `temp`, or `foo`.

2. **Use Clear and Understandable Language**:
   - Use words from the problem domain or domain-specific terminology to name your identifiers.
   - Avoid abbreviations or acronyms that may not be universally understood unless they are well-known and widely accepted in your domain.

3. **Be Explicit**:
   - Be explicit in your naming. A longer, descriptive name is often better than a shorter, ambiguous one. For example, use `calculateTotalPrice` instead of `calc` or `total`.

4. **Follow Naming Conventions**:
   - Adhere to naming conventions and conventions outlined in the Dart Style Guide. For example, use `lowerCamelCase` for variables and function names, and `UpperCamelCase` for class names.

5. **Use Nouns for Variables and Constants**:
   - Variable names should generally be nouns or noun phrases that describe what the variable represents. For example, `userProfile`, `productList`, or `invoiceTotal`.

6. **Use Verbs for Functions and Methods**:
   - Function and method names should generally be verbs or verb phrases that describe what action they perform. For example, `calculateTotalPrice()`, `fetchUserData()`, or `validateEmail()`.

7. **Avoid Overly Generic Names**:
   - Avoid using names like `data`, `result`, or `value` without additional context. Provide context that clarifies what the data represents.

8. **Avoid Magic Numbers and Strings**:
   - Replace magic numbers and strings in your code with well-named constants. For instance, replace `const int maxAttempts = 3` instead of `const int 3` when limiting attempts.

9. **Refactor as Needed**:
   - If you find that an existing name is no longer descriptive due to code changes, don't hesitate to refactor and choose a more appropriate name.

10. **Use Consistent Naming Styles**:
    - Maintain consistency in naming styles throughout your codebase. Consistency makes the code more predictable and easier to navigate.

11. **Self-Explanatory Code**:
    - Strive to make your code as self-explanatory as possible through the use of descriptive names. Minimize the need for comments by making the code's intent evident in the names themselves.

Here's an example of code with descriptive names:

```dart
// Descriptive variable names
String userName = 'john_doe';
int itemCount = 10;
bool isLoggedIn = false;

// Descriptive function names
double calculateTotalPrice(double itemPrice, int quantity) {
  return itemPrice * quantity;
}

List<User> fetchActiveUsers() {
  // Implementation
}
```

By consistently using descriptive names, you enhance the clarity and maintainability of your Dart and Flutter code. This practice promotes better collaboration among developers, reduces the risk of misunderstandings, and ultimately leads to more robust and maintainable codebases.


10. [[explanation/organize_code_into_small_functions_and_classes|Organize Code into Small Functions and Classes]]:
	- Je pan code write karo ae small, reusable function and classes ma hovo jaruri che because function find karva ae more easy che instead code find karvo, so aa pratice aek code ne readability and maintainability banavi aape che, and flutter ma widgets ae aek good example che jema aa pratice follow thayeli che.
11. [[explanation/properly_comment_your_code|Explain Properly Comment Your Code]]:
	-  Je pan function create karo aeni uper comment kari ne aeno use explain karvano jenathi code understand karvo easy pade. and /// no use karavano jyare class methods and functions nu documentation write karo tyare.
	- For example jo flutter ae aenu documentation j na banavyu hot to aapde shikhva mate ketlu hard thay so better che ke properly comment karvani code ma.
12. [[explanation/use_proper_widget_composition|Use Proper Widget Composition]]: 
	- aapde flutter ma jyare user interfaces(UI) banavi ae tyare aena widget ne composing(Smalled Blocks) kari ne banavviae ae j best pratice che.
	- widget ni hierarchy create karvathi complex ui ne pan easy way ma write kari shakay che. 
	- everytime setState and provider no nana functions mate use nai karvano so better che aene seprate design kari ne aena buildcontext and updates ne control karvanu.
13. [[explanation/avoid_deep_widget_nesting|avoid_deep_widget_nesting]]: 
	- Deep widget nesting means aek widget ni niche second and second ni niche third and third ni niche forth and so on. (example: ListView.builder)
	- Deep widget nesting ae code read and maintain karvama problem create karshe means aene samajvo ae hard thay jay che, so tamne jyare aevu lage ke bow batha widget nested thay che tyare aene smaller widget ma break karvanu consider karvu jove.
14. [[explanation/keep_ui_and_business_logic_seprated|Keep UI and Business Logic Separated]]: 
	- Separate your UI code from your business logic. This can help with testing and code maintainability. Consider using packages like bloc(preferred) or provider for state management.
15. [[explanation/use_flutter_devtools|Use Flutter DevTools]]: 
	- Flutter provides a powerful set of tools for debugging and profiling your application. Familiarize yourself with Flutter DevTools to help identify and resolve issues in your code efficiently.
16. [[explanation/test_your_code|Test Your Code]]:
	- Write unit tests and widget tests to ensure that your code functions as expected. Flutter has built-in support for testing, making it easy to write and run tests.
17.  [[explanation/stay_up_to_date|Stay Up-to-Date]]:
	- Flutter is an evolving framework, and best practices can change over time. Keep up-to-date with Flutter updates, new packages, and community recommendations to improve your code quality.
18. [[explanation/analyse_and_format_your_code|Analyse and Format Your Code]]:
	- Use tools like dart analyse and dart format to ensure your code adheres to best practices and formatting guidelines.
21. [[explanation/document_your_code|Document Your Code]]:
	- Use documentation comments to describe the purpose, parameters, and return values of functions and classes. This helps other developers understand how to use your code.
22. [[explanation/use_version_control|Use Version Control]]:
	- Always use version control systems like Git to track changes in your code. This helps you collaborate with others and revert changes if needed.
    
Remember that good code practices may vary depending on the project and team, but these guidelines can serve as a solid foundation for writing clean and maintainable Flutter code.
