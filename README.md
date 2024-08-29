# exercise-superhero-battle-simulator

## Learning Goals

Upon completing this exercise, you will be able to:

•	Implement classes using ES6 syntax

•	Use constructors to initialize objects

•	Create and use methods within classes

•	Understand and apply inheritance in JavaScript

•	Utilize public and private class fields

## Introduction

Welcome to the Superhero Battle Simulator! 🦸‍♀️🦸‍♂️

In this exercise, you'll be creating your very own superhero characters using JavaScript's powerful Object-Oriented Programming features. You'll define their unique abilities, secret identities, and even simulate epic battles between them.

From flying heroes soaring through the skies to strong heroes lifting incredible weights, you'll bring these characters to life with code. As you work through the tasks, you'll be applying key OOP concepts like classes, inheritance, and encapsulation.

So, put on your coding cape, flex those JavaScript muscles, and get ready to watch the superhero battles unfold... 🍿 

It's time to see which hero reigns supreme in your virtual superhero universe!

## Getting Started

1. Fork the repository
2. Clone the repository to your computer
3. Open the repository in VS Code
4. Start the Live Server in VS Code
5. Follow instructions

## Instructions

Welcome to the superhero coding arena. 🦸🏻💻.

Your mission, should you choose to accept it, begins with a single `index.js` file.

Create this file, then tackle the tasks below, writing your heroic solutions within.

Ready to bring superheroes to life with code? Let’s power up and begin!


### Task 1: Create the Base Superhero Class

Create a `class` called `Superhero` with the following specifications:

1.	Public fields:

- `name` (string)
- `powerLevel` (number)

2.	Private field:

- `#secretIdentity` (string)

3.	Constructor:

- Should accept `name`, `powerLevel`, and `secretIdentity` as parameters

4.	Methods:

- `introduce()`: Returns a string introducing the hero, 
e.g., "I am `name`, with a power level of `powerLevel`!")
- `getPowerLevel()`: Returns the hero's power level
- `train()`: Increases the hero's power level by 1

### **Task 2: Create Subclasses**

Create two subclasses that inherit from Superhero:

1. `FlyingHero`:
    - Create an additional public field called `flightSpeed` (number)
    - Override the `introduce()` method to include all the information from the parent class plus the flight speed
    - Create a new method `fly()` which returns a string:
    ”`name` is flying at `flightSpeed` mph!"

2.	`StrongHero`:

- Create an additional public field called `strengthLevel` (number)
- Override the `introduce()` method to include all the information from the parent class plus the strength level
- Create a new method called `lift()` which returns a string:
 “`name` is lifting [`strengthLevel` * 100] pounds!"

### **Task 3: Create Instances**

Create the following superhero instances:

1.	A `FlyingHero` named "Wind Rider" with:	

- Power level: 8
- Secret identity: "Snoop Dogg"
- Flight speed: 200

2.	A StrongHero named "Mega Lift" with:

- Power level: 7
- Secret identity: "Paddington Bear"
- Strength level: 10

### **Task 4: Implement Battle System**

Create a `battle()` function that simulates a battle between two superheroes:

- The function should accept two Superhero objects as parameters.
- Compare the power levels of the two heroes.
- The hero with the higher power level wins.
- If the power levels are equal, it's a tie.
- Return a string announcing the winner or tie.

### **Task 5: Simulate Battles**

Use your `battle()` function to simulate the following scenarios:

1.	Wind Rider vs Mega Lift

2.	Wind Rider vs Wind Rider 

(Create a second instance of Wind Rider with the same attributes)

Print the results of each battle to the console!

## Submission

When you've completed the exercise:

1.	Commit your changes:

```jsx
git add .
git commit -m "Completed Superhero Battle Simulator Exercise"
git push origin main
```

2.	Create a Pull Request
3.	Submit the URL of your Pull Request

<Submission>

Please submit the URL of your Pull Request below:

## **Bonus Challenge**

If you’re up for an extra challenge, you can try the following:

### **Task 6: Slight Advantage**

Enhance the `battle()` function to give a slight advantage to `FlyingHero` against `StrongHero`. If a `FlyingHero` battles a `StrongHero` and their power levels are within 2 points of each other, the `FlyingHero` wins.

### **Task 7: Special Abilities**

Enhance your Superhero classes with special abilities:

1. Add a new method `useSpecialAbility()`  to the base `Superhero` class. This method should return a string: "`name` is using their special ability!"
2. Override this method in both `FlyingHero` and `StrongHero` classes:
    - For `FlyingHero`, it should return: "`name` creates a whirlwind!"
    - For `StrongHero`, it should return: "`name` causes an earthquake!"
3. Add a new method `getSpecialAbilityType()` to the base `Superhero` class. This method should return null.
4. Override `getSpecialAbilityType()` in the subclasses:
    - For `FlyingHero`, it should return "whirlwind”
    - For `StrongHero`, it should return "earthquake"
5. Modify the `battle()` function to incorporate these special abilities:
    - At the start of each battle, both heroes use their special ability 
    (print the result of `useSpecialAbility()` for each hero).
    - Check the special ability type of each hero using `getSpecialAbilityType()`:
        - If it's "whirlwind", apply a 20% boost to their power level for this battle.
        - If it's "earthquake", apply a 15% boost to their power level for this battle.
6. Create a new battle scenario using the updated `battle()` function and test it with your existing superhero instances.
7. Print out the detailed battle results, including the use of special abilities and any power boosts applied.

## Frequently Asked Questions (FAQs)

- **What's the difference between public and private fields in a class?**
    
    Public fields are accessible both inside and outside the class, while private fields (denoted with a # prefix) are only accessible within the class itself.
    

- **How do I call a parent class's method in a subclass?**
    
    You can use the super keyword. For example, super.introduce() in a subclass method will call the introduce() method of the parent class.
    
- **Why do we use the** # **symbol for the** `secretIdentity` **field?**
    
    The # symbol denotes a private field in JavaScript classes (introduced in ES2022). It ensures that secretIdentity can only be accessed or modified within the Superhero class, maintaining encapsulation.
    
- **How do I create a new instance of a subclass like `FlyingHero`?**
    
    You can create a new instance using the `new` keyword, like this: `new FlyingHero(...)`.
    

- **How do I implement different behaviors for different subclasses?**
    
    You can use method overriding to implement different behaviors for subclasses. Define a method in the base class, then override it in each subclass with specific implementations.
    
    For example, the `useSpecialAbility()` and `getSpecialAbilityType()` methods are defined in the `Superhero` class and can then be overridden in `FlyingHero` and `StrongHero` to provide unique behaviors.
