# JS_day_3-var-
...................... var .....................
- About Lesson
var: The Basics
A. Introduction
In JavaScript, var is how you declare variables. It’s like naming a box to store something. Imagine you have a box labeled “snacks.” That’s what var does—lets you name a container for storing data.

B. Syntax
Declaring a variable with var is simple:

var myBox = "Snacks";
console.log(myBox); // Output: Snacks
C. Key Features
Re-declaration Allowed
You can declare the same variable name multiple times without getting an error.

var item = "Pen";
var item = "Notebook";
console.log(item); // Output: Notebook
Hoisting
Variables declared with var can be used before they are written in the code, but their value will be undefined until assigned.

console.log(thing); // Output: undefined
var thing = "Chair";
Global Scope
If you declare var outside of anything else, it becomes available everywhere in your code.

var city = "Kolkata";
console.log(city); // Output: Kolkata
D. Common Mistakes
Declaring the same name twice may confuse you later.

var fruit = "Mango";
var fruit = "Banana"; // Overwrites the previous value
Using var without assigning a value gives undefined.

var name;
console.log(name); // Output: undefined
E. Conclusion
The var keyword is the foundation of JavaScript variables. It’s simple, flexible, and works fine. While newer methods exist, var still does the job and is easy to learn. Stick to this when starting out—no need to overthink!
 - ............................ const .....................
- About Lesson
A. Introduction
Imagine you have a name tag that says, “Hi, my name is John.” Once you write your name on it, you can’t change the name anymore—it stays the same forever!

In JavaScript, const works just like that name tag. It’s a way to declare a variable that keeps the same value and cannot be changed after you set it.

B. Syntax
Here’s how to use const:

const myName = "John";
console.log(myName); // Output: John
Once you set the value of myName, you cannot change it:

const myName = "John";
myName = "Sarah"; // ❌ Error: Assignment to constant variable
C. Key Features
Cannot Be Reassigned: Once you set the value, it cannot be changed.
Must Be Initialized: You have to give it a value immediately when declaring it.
 
const age; // ❌ Error: Missing initializer
age = 25;
Only Works Inside Its Block: const variables exist only within the {} where you declare them.
 
{
    const favoriteFood = "Pizza";
    console.log(favoriteFood); // Output: Pizza
}
console.log(favoriteFood); // ❌ Error: favoriteFood is not defined
D. Common Mistakes
Trying to Reassign a const Variable

 
const age = 30;
age = 35; // ❌ Error
Fix: Use const only for values you know won’t change.

Declaring Without a Value

 
const city; // ❌ Error: Missing initializer
city = "New York";
Fix: Always assign a value immediately when you declare a const.

 
const city = "New York"; // ✅
E. Conclusion
const is a great way to declare variables when the value should never change. It keeps your code clean and prevents accidental changes. Just remember: assign a value right away, don’t reassign it, and use it only when the value is constant.

- .................... let .................................
About Lesson
Introduction
Imagine you have a whiteboard where you can write something down, erase it, and write something new whenever you want. That’s how let works in JavaScript—it allows you to create variables that can change (be reassigned) later.

If const is like a permanent marker, let is your handy, flexible whiteboard marker!

B. Syntax
Here’s how to use let:

let myAge = 20;
console.log(myAge); // Output: 20
// You can change the value later
myAge = 21;
console.log(myAge); // Output: 21

Unlike const, you can declare a variable with let first and assign it a value later:

let favoriteColor;
favoriteColor = "blue";
console.log(favoriteColor); // Output: blue
C. Key Features
Can Be Reassigned: You can change the value of a let variable anytime.

 
let score = 100;
score = 150; // Works fine
Block Scoped: Like const, let variables only exist inside the block {} where they are declared.

 
{
    let fruit = "apple";
    console.log(fruit); // Output: apple
}
console.log(fruit); // ❌ Error: fruit is not defined
Can Be Declared Without Initializing: You can declare a let variable first and assign a value later.

 
let city;
city = "Paris";
console.log(city); // Output: Paris
D. Common Mistakes
Using a let Variable Before Declaring It

 
console.log(myName); // ❌ Error: Cannot access 'myName' before initialization
let myName = "Sarah";
Fix: Always declare a let variable before using it.

 
let myName = "Sarah";
console.log(myName); // ✅ Output: Sarah
Confusing let with const
If you don’t plan to change the value, use const instead of let.

 
let favoriteFood = "Pizza"; // ✅ Works, but const is better if it won’t change
Declaring the Same let Variable Twice in the Same Scope

 
let age = 25;
let age = 30; // ❌ Error: Identifier 'age' has already been declared
Fix: Use the variable name only once in the same scope.

 
let age = 25;
age = 30; // ✅ Works fine
E. Conclusion
let is your go-to tool for variables that need to change. It’s flexible, easy to use, and safer than older ways of declaring variables (like var).

When in doubt, ask yourself: “Will this value change?” If yes, use let!