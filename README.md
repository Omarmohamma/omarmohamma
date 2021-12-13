### Hi there 👋

<!--
**Omarmohamma/omarmohamma** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
   Constant 
Using constants is more a way of defensive programming, to protect yourself from yourself, from accidentally changing the value somewhere in the code Technically, yes, you can use a variable instead.
 Not using const can mean someone in a team project could declare where int FORTY_TWO = 42 and make it equal FORTY_TWO = 41 somewhere else by another team member. with const although none of this will ever happen. Plus const is stored elsewhere in memory, when compared to the storage of normal variables, and is more efficient.
The const keyword is often used for function parameters, particularly pointers, to suggest the memory the pointer points to will not be modified by the function. Look at the decleration 
Otherwise, for example, an declaration such as
const int my_magic_no = 54321;
might be preferred over:
#define MY_MAGIC_NO 54321
for type safety reasons.
It's a really easy way to trap a certain class of errors. If you declare a variable const, and accidentally try to modify it, the compiler will call you on it.Constants have several advantages over variables.
Constants provide some level of guarantee that code can't change the underlying value. This is not of much importance for a smaller project, but matters on a larger project with multiple components written by multiple authors.
Constants also provide a strong hint to the compiler for optimization. Since the compiler knows the value can't change, it doesn't need to load the value from memory and can optimize the code to work for only the exact value of the constant (for instance, the compiler can use shifts for multiplication/division if the const is a power of 2.)
Constants are also inherently static - you can declare the constant and its value in a header file, and not have to worry about defining it exactly one place
a low-level language like C, constants allow for several compilation optimizations.
For a programming language in general, you don't really need them. High level dynamic languages such as Ruby and JavaScript doesn't have them (or at least not in a true constant sense). Variables are used instead, just like you suggested

A variable, as you can guess from the name, varies over time. If it doesn't vary, there is "no loss". When you tell the compiler that the value will not change, the compiler can do a whole bunch of optimizations, like directly inlining the value and never allocating any space for the constant on the stack.
However, you cannot always count on your compiler to be smart enough to be able to correctly determine if a value will change once set. In any situation where the compiler is incapable of determining this with 100% confidence, the compiler will err on the side of safety and assume it could change. This can result in various performance impacts like avoiding inlining, not optimizing certain loops, creating object code that is not as parallelism-friendly.
Because of this, and since readability is also important, you should strive to use an explicit constant whenever possible and leave variables for things that can actually change.
As to why constants are used instead of literal numbers:
1) It makes code more readable. Everyone knows what 3.14 is (hopefully), not everyone knows that 3.07 is the income tax rate in PA. This is an example of domain-specific knowledge, and not everyone maintaining your code in the future will know it.
2) It saves work when you make a change. Going and changing every 3.07 to 3.18 if the tax rate changes in the future will be annoying. You always want to minimize changes and ideally make a single change. The more concurrent changes you have to make, the higher the risk that you will forget something, leading to errors.
3) You avoid risky errors. Imagine that there were two states with an income tax rate of 3.05, and then one of them changes to 3.18 while the other stays at 3.07. By just going and replacing, you could end up with severe errors. Of course, many integer or string constant values are more common than "3.07". For example, the number 7 could represent the number of days in the week, and something else. In large programs, it is very difficult to determine what each literal value means.
For example, if I have an enumeration for the days of the weeks and for the months, I will be warned if I assign a month into a day. If I just use integer constants, there will be no warning when day 3 is assigned to month 3. You always want type safety, and it improves readability. Enumerations are also better for defining order. Imagine that you have constants for the days of the week, and now you want your week to start on Monday rather than Sunday.




                 ampersand
& is a Binary as well as Unary operator.
When used as Binary operator (with 2 operands), it is called as- ‘Bitwise And’ operator. It checks each bit of the operands for AND, then it returns the value obtained.
In C language can be used as a Unary operator (with 1 operand) also. When used as a Unary operator, it returns the address of the operand

The & term is generally used in conditional operators, most often the “if” statement. It’s used when you want to imply that you want two conditions to be occurring simultaneously.
In real life, if you want to buy two things at a store, you tell the guy behind the counter, “I’ll have a pack of chips and a soda.”
Similarly, in coding, you may come across times when you need more than one condition to be true (or false) for a specific piece of code 
Related Questions (More Answers Below)
In pass by reference, you pass the address of the original argument .So the changes done are permanent. However, in pass by value, a copy of the original argument is manipulated, which doesn’t affect the original argument.

One advantage of the call by reference method is that it is using pointers, so there is no doubling of the memory used by the variables (as with the copy of the call by value method). This is of course great, lowering the memory footprint is always a good thing. So why don’t we just make all the parameters call by reference?
There are two reasons why this is not a good idea and that you (the programmer) need to choose between call by value and call by reference. The reason are: side effects and privacy. Unwanted side effects are usually caused by inadvertently changes that are made to a call by reference parameter. Also in most cases you want the data to be private and that someone calling a function only be able to change if you want it. So it is better to use a call by value by default and only use call by reference if data changes are expected.

and is used as shorthand to mean "and," as in "John & Rob went to the baseball game." It is also used in programming languages, including Visual Basic (to combine variables and literal text), C++ (denoting an address in memory) and Perl (to call a user-defined subroutine). It can also be used in Excel spreadsheet formulas to combine several values (cells) into a single value (cell) and in HTML for extended HTML characters.
When creating a web page, some characters (all shown on extended HTML characters page) require an extended character code to be correctly seen. For example, because quotes (") are used in HTML, to add a quote to a web page's text you need to use the extended HTML code &quot; in the HTML code. All extended HTML character codes begin with an ampersand and end with a semicolon.
Also, the ampersand itself must also use an extended character code. In other words, if you wanted to show "&" on an HTML web page, you would need to use the code &amp; in HTML.
the ampersand is used to separate variables
Visual Basic. 

    
