---
created: 2023-09-15T21:33:06+05:30
updated: 2023-09-16T11:01:56+05:30
---
**

1.  Kyarey setState use nathi karavanu always proper state managment use karvanu che.
    
2.  State managment mate bloc(preferred) or provider bemathi aek j use karvanu rehshe.
    
3.  Never use getx for state managment.
	- Disadvantages: ([Ref: Medium](https://shirsh94.medium.com/beyond-the-hype-the-untold-truth-about-getx-and-its-downsides-for-flutter-development-2c0b0b9b2fb5))
		- Getx Provide Simplicity
		- GetX force to replacing Flutter
		- GetX tends to use anti-patterns
		- GetX tries to do everything
		- The level of documentation for GetX needs improvement.
		- The Unusual Number of API Elements in GetX
		
4.  Follow proper project architecture(MVC(Medium Project) or MVVM(Large Project))
5.  Official Documentation Read karvanu aavdvu jove and ae must required skills che.
6.  Effective Dart Programming Writing Style: 
	- Saro code write karvo and ae sari code pratice che and most important points che.
	- Consistent naming, ordering and format maintain karvathi ae code no look maintain thay shake che.
	- powerful pattern-matching hardware mate saru pade ke pattern match kari ne aapane suggestion provide kari aape (AI - Github Copilot)
	- and jo consistent code style hoy aakha dart na ecosystem mate to batha mate easier reshe ke aemathi shikhva mate and aek bija na code ma contributation karva mate.
	- and Oceanmtech aa code nu structure maintain karvu ae mandotory che je ne aapde universal code structure na rules par thi j aapde define karel che.
	- Aapde official dart language ni guide ne follow karvanu che:
	- [Dart Programming Writing Rules](https://dart.dev/effective-dart/style#formatting) (Read & Implement karvanu che)
    
8.  OceanMTech na aek pan flutter developer ne jyare code write karta hoy tyare keyboard same jovu na padvu jove aena mate typing speed mate ni daily pratice karvani che and biju keyabord and mouse ni click fast action ma perform thay ae mandatory che.

9. Jyare code write karo cho aena file name and file location always yad rakhvana and aej rite function name variable name ae pan yad rakhvana and aena name pan function na according j lakhvana jenathi jyare ae module nu logic update thay tyare direct file name par thi ae file par jay shakay because jyare projects ma 1000 files hoy tyare manually find karvi ae time consuming process che.

10.  Use Descriptive Variable and Function Names:  
	- koi pan variables, functions, classes and widget na name descriptive choose karvana reshe, je aapane code vadhu samajavama and bija pan easy way ma samji shake and in future aapde aa project par return work start karvi to samajava mate easy reshe. so single-letter or cryptic variable names ne avoid karvu jaruri che, nichenu exaple refer karvu more details mate.
	- Read More - [[Explain Use Descriptive Variable and Function Names]]
    
11.  Organize Code into Small Functions and Classes:
	- Je pan code write karo ae small, reusable function and classes ma hovo jaruri che because function find karva ae more easy che instead code find karvo, so aa pratice aek code ne readability and maintainability banavi aape che, and flutter ma widgets ae aek good example che jema aa pratice follow thayeli che.
	- Read More - [[Explain Organize Code into Small Functions and Classes]]

12.  Properly Comment Your Code:
	-  Je pan function create karo aeni uper comment kari ne aeno use explain karvano jenathi code understand karvo easy pade. and /// no use karavano jyare class methods and functions nu documentation write karo tyare.
	- For example jo flutter ae aenu documentation j na banavyu hot to aapde shikhva mate ketlu hard thay so better che ke properly comment karvani code ma.
	- Read More - [[Explain Properly Comment Your Code]]
    
13.   Use Proper Widget Composition: [(Read More)]    
	- aapde flutter ma jyare user interfaces(UI) banavi ae tyare aena widget ne composing(Smalled Blocks) kari ne banavviae ae j best pratice che.
	- widget ni hierarchy create karvathi complex ui ne pan easy way ma write kari shakay che. 
	- everytime setState and provider no nana functions mate use nai karvano so better che aene seprate design kari ne aena buildcontext and updates ne control karvanu.
	- Read More - [[Use Proper Widget Composition]]
 
14.  Avoid Deep Widget Nesting: 
	- Deep widget nesting means aek widget ni niche second and second ni niche third and third ni niche forth and so on. (example: ListView.builder)
	- Deep widget nesting ae code read and maintain karvama problem create karshe means aene samajvo ae hard thay jay che, so tamne jyare aevu lage ke bow batha widget nested thay che tyare aene smaller widget ma break karvanu consider karvu jove.
	- Read More - [[Avoid Deep Widget Nesting]]

15.   Keep UI and Business Logic Separated: 
	- Separate your UI code from your business logic. This can help with testing and code maintainability. Consider using packages like bloc(preferred) or provider for state management.
	- Read More - [[Keep UI and Business Logic Separated]]

16.  Use Flutter DevTools: 
	- Flutter provides a powerful set of tools for debugging and profiling your application. Familiarize yourself with Flutter DevTools to help identify and resolve issues in your code efficiently.
	- Read More - [[Use Flutter DevTools]]

17.  Test Your Code:
	- Write unit tests and widget tests to ensure that your code functions as expected. Flutter has built-in support for testing, making it easy to write and run tests.
	- Read More - [[Test Your Code]]

18.   Stay Up-to-Date:
	- Flutter is an evolving framework, and best practices can change over time. Keep up-to-date with Flutter updates, new packages, and community recommendations to improve your code quality.
	- Read More - [[Stay Up-to-Date]]

19.   Analyze and Format Your Code:
	- Use tools like dart analyze and dart format to ensure your code adheres to best practices and formatting guidelines.
	- Read More - [[Explain Analyse and Format Your Code]]
    
20.  Document Your Code:
	- Use documentation comments to describe the purpose, parameters, and return values of functions and classes. This helps other developers understand how to use your code.
	-  Read More - [[Explain Document Your Code]]

21.   Use Version Control:
	- Always use version control systems like Git to track changes in your code. This helps you collaborate with others and revert changes if needed.
	-  Read More - [[Explain Use Version Control]]
    
Remember that good code practices may vary depending on the project and team, but these guidelines can serve as a solid foundation for writing clean and maintainable Flutter code.
**