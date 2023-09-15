# Communication System Project (Assignment 1)

## Introduction

This project involves implementing a simple communication system with Customers, Operators, and Bills. Customers can perform various communication actions like talking, messaging, and connecting to the internet, with corresponding costs managed by Operators and tracked by Bills.

## Classes and Implementation Details

### Main Class
- Handles input and output operations.
- Reads directions from an input file (JSON or hard-coded).
- Contains three arrays: `Customer[] customers`, `Operator[] operators`, and `Bill[] bills` for storing data.

### Customer Class
- Fields:
  - `int ID`
  - `String name`
  - `int age`
  - `Operator[] operators`
  - `Bill[] bills`
- Methods:
  - Constructor with five parameters: `int ID`, `String name`, `int age`, `Operator[] operators`, `Bill[] bills`, `double limitingAmount`.
  - `void talk(int minute, Customer other)` for customers to talk via the operator.
  - `void message(int quantity, Customer other)` for customers to send messages.
  - `void connection(double amount)` for customers to connect to the internet.
  - Getter and setter methods for `age`, `operators`, and `bills`.

### Operator Class
- Fields:
  - `int ID`
  - `double talkingCharge`
  - `double messageCost`
  - `double networkCharge`
  - `int discountRate`
- Methods:
  - Constructor with five parameters: `ID`, `talkingCharge`, `messageCost`, `networkCharge`, `discountRate`.
  - `double calculateTalkingCost(int minute, Customer customer)` for calculating the cost of talking.
  - `double calculateMessageCost(int quantity, Customer customer, Customer other)` for calculating the cost of messaging.
  - `double calculateNetworkCost(double amount)` for calculating the cost of internet usage.
  - Getter and setter methods for `talkingCharge`, `messageCost`, `networkCharge`, `discountRate`.

### Bill Class
- Fields:
  - `double limitingAmount`
  - `double currentDebt`
- Methods:
  - Constructor with one parameter: `limitingAmount`.
  - `boolean check(double amount)` to check if the limiting amount is exceeded.
  - `void add(double amount)` to add debts to the bill.
  - `void pay(double amount)` to pay the bills.
  - `void changeTheLimit(double amount)` to change the limiting amount.
  - Getter methods for `limitingAmount` and `currentDebt`.

## Input Format
- Set the number of customers `N` and the number of operators `M` (where `M != N`).
- Implement and test various operations including customer creation, operator creation, communication actions, bill payment, operator change, and bill limit change.

## Instructions
- Implement most calculations within the Customer, Operator, and Bill classes.
- Apply discounts based on age and operator for talking and messaging costs.
- Check bill limits before performing actions.
- Assume customers have enough money to pay their bills.
- Start IDs from 0 for Customers, Operators, and Bills.
- You can declare extra fields or methods, but the given ones must exist with the same parameters and names.

## References
Scott W. Ambler. The Object Primer 3rd Ed: Agile Model Driven Development
(AMDD) with UML 2.
Robert Martin. Clean Code: A Handbook of Agile Software Craftsmanship.
Robert Martin. Agile Software Development, Principles, Patterns, and Practices.
https://www.geeksforgeeks.org/introduction-of-object-oriented-programming/
https://www.learncpp.com/cpp-tutorial/welcome-to-object-oriented-programming/
https://realpython.com/python-property/
https://docs.python.org/3/tutorial/datastructures.html#dictionaries
https://www.w3schools.com/python/python_dictionaries.asp
https://docs.python.org/3/tutorial/datastructures.html#
