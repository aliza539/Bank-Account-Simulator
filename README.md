# Bank-Account-Simulator

A modular **JavaScript banking simulation** project that demonstrates **core and advanced JavaScript concepts** 

The application models real banking operations such as **depositing funds, withdrawing money, transferring balances, calculating interest, and applying transaction fees**. It highlights JavaScript concepts like **closures, prototypal inheritance, factory patterns, currying, and dynamic function binding**.

The project is intentionally implemented using **constructor functions and prototypes** .

## Project Objective

The project aims to demonstrate practical knowledge of **JavaScript object-oriented and functional programming concepts** by building a small banking simulation.

It focuses on:

* Encapsulating sensitive data using closures
* Structuring reusable logic through prototypal inheritance
* Creating accounts dynamically using a factory function
* Demonstrating functional programming techniques like currying
* Using call, apply, and bind for dynamic context control
* Implementing an event-like callback system for low balance alerts

This mirrors patterns used in real-world JavaScript applications while reinforcing **core language fundamentals**.

## Features

**Closure-Based Private Balance**
Balances are stored in closures to prevent direct access. All balance updates happen only through **deposit** and **withdraw** methods.

**Prototypal Inheritance**
A base Account constructor is extended to create:

* **Savings Account** – supports interest calculation
* **Checking Account** – supports overdraft limits

Both inherit shared functionality while allowing specialized behavior.

**Method Overriding**
CheckingAccount overrides **withdraw** to enforce overdraft limits, showing how child objects can customize inherited functionality.

**Account Transfer System**
Funds can be transferred between accounts using **call()** to dynamically execute methods on different account objects.

**Currying for Fee Calculation**
Includes a curried fee calculator that locks a transaction rate and returns a reusable function for calculating fees, demonstrating **higher-order functions**.

**Low Balance Callback System**
Triggers alerts when account balances fall below a threshold, simulating **event-driven behavior**.

**Dynamic Function Context**
Demonstrates function context manipulation using:

* `call()`
* `apply()`
* `bind()`

**accountFactory.js** – core banking logic: base account, specialized accounts, inheritance, withdraw overriding, curried fee calculator, factory function.
**demo.js** – demonstrates usage: account creation, deposits/withdrawals, transfers, interest application, fees, dynamic context, and error handling.


## Technologies Used

* JavaScript (ES6+)
* ES Modules
* Closures
* Prototypal Inheritance
* Functional Programming (Currying)
* Factory Pattern
* Dynamic Context Binding
* Node.js runtime

---

## Running the Project

1. Clone the repository:

```bash
git clone <repository-url>
```

2. Navigate to the project directory:

```bash
cd bank-account-simulator
```

3. Run the demo:

```bash
node src/demo.js
```

## Expected Behavior

* Savings and checking accounts are created
* Deposits and withdrawals update account balances
* Funds can be transferred between accounts
* Interest is applied to savings accounts
* Transaction fees calculated using a curried function
* Low balance alerts trigger correctly
* Function context manipulation demonstrated using `call`, `apply`, and `bind`

---

## Learning Outcomes

* JavaScript closures and encapsulation
* Prototype-based inheritance
* Constructor functions and prototype chains
* Method overriding
* Functional programming (currying)
* Dynamic function context manipulation
* Modular JavaScript architecture

---

## License

This project is intended for **educational purposes**, demonstrating key JavaScript concepts through a structured banking simulation.
