## Configuration

#### Custom Objects and Field naming

Custom objects and fields will use **PascalCase** naming to follow the same patterns as the standard Salesforce objects. They will also avoid any kind of non-alphanumeric characters.

i.e. `MyObject__c`, `MyObject__c.MyField__c`

As a best practice, try to make the object's developer name be the same as the label.

The relationship name of an object will simply be the plural of the object's name itself also following PascalCase.

#### Workflows, processes, email templates and other configurations

All configuration names will also use PascalCase and avoid any kind of non-alphanumeric characters.

## Apex

### Naming

- lower camelcase for methods and variables.
- PascalCase for classes and interfaces.
- constants will be all in caps with underscores.
- `SObject` should be written as such.
- Test classes should have the word `Test` after the class it's testing's name, like `MyClassTest` and not like `TEST_MyClass`, `MyClass_Test` or any other variations.

### Structure

Always order the class properties and methods in the following way:

1. Constants
2. Public properties
3. Private properties
4. Constructors
5. Public instance methods
6. Public class methods
7. Private instance methods
8. Private class methods

#### Indentation

Code will be indented with 4 spaces, using spaces and not tabs so it looks the same on everyone's screen.

#### New lines and spaces

- Place comments in a line by themselves.
- Open braces should have a space before them and not a new line.
- All clauses like `if`, `else`, `for`, `try`, etc. must start in a new line.
- In method definitions, there should be no space before the open parenthesis, and one space after.
- In method calls and definitions, there should not be whitespace between the name of the method and the open parenthesis.
- A single space should separate binary operators from the surrounding elements.
- A colon inside a for each loop (e.g., `for (Contact cnt : contacts) {`) should have one space on either side.
- There should be no whitespace before commas, and one space after.

#### Explicit declarations

Always specify 
- Encapsulation modifiers such as `global`, `public` or `private`.
- Class modifiers such as `with sharing` or `without sharing`.
- `this` when calling instance methods.

#### Annotations

- Always use caps on the annotations.
- Break the line after the annotation.

#### Tests

- Prefer `@IsTest` over `testMethod`.
- Don't indent between `Test.startTest()` and `Test.stopTest()`.

## SOQL

- All SOQL keywords should be written in caps.
- Long queries should be broken down with a new line for each keyword.
- The Id field must always be included and it should be included first.
- Same rules for dynamic SOQL.