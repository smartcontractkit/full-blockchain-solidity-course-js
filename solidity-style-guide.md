# Style Guide — Solidity 0.8.17 documentation
Introduction[](#introduction "Permalink to this heading")
----------------------------------------------------------

This guide is intended to provide coding conventions for writing Solidity code. This guide should be thought of as an evolving document that will change over time as useful conventions are found and old conventions are rendered obsolete.

Many projects will implement their own style guides. In the event of conflicts, project specific style guides take precedence.

The structure and many of the recommendations within this style guide were taken from python’s [pep8 style guide](https://www.python.org/dev/peps/pep-0008/).

The goal of this guide is _not_ to be the right way or the best way to write Solidity code. The goal of this guide is _consistency_. A quote from python’s [pep8](https://www.python.org/dev/peps/pep-0008/#a-foolish-consistency-is-the-hobgoblin-of-little-minds) captures this concept well.

Note

A style guide is about consistency. Consistency with this style guide is important. Consistency within a project is more important. Consistency within one module or function is most important.

But most importantly: **know when to be inconsistent** – sometimes the style guide just doesn’t apply. When in doubt, use your best judgment. Look at other examples and decide what looks best. And don’t hesitate to ask!

Code Layout[](#code-layout "Permalink to this heading")
--------------------------------------------------------

### Indentation[](#indentation "Permalink to this heading")

Use 4 spaces per indentation level.

### Tabs or Spaces[](#tabs-or-spaces "Permalink to this heading")

Spaces are the preferred indentation method.

Mixing tabs and spaces should be avoided.

### Blank Lines[](#blank-lines "Permalink to this heading")

Surround top level declarations in Solidity source with two blank lines.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgQSB7CiAgICAvLyAuLi4KfQoKCmNvbnRyYWN0IEIgewogICAgLy8gLi4uCn0KCgpjb250cmFjdCBDIHsKICAgIC8vIC4uLgp9)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract A {
    // ...
}


contract B {
    // ...
}


contract C {
    // ...
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgQSB7CiAgICAvLyAuLi4KfQpjb250cmFjdCBCIHsKICAgIC8vIC4uLgp9Cgpjb250cmFjdCBDIHsKICAgIC8vIC4uLgp9)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract A {
    // ...
}
contract B {
    // ...
}

contract C {
    // ...
}

```


Within a contract surround function declarations with a single blank line.

Blank lines may be omitted between groups of related one-liners (such as stub functions for an abstract contract)

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKYWJzdHJhY3QgY29udHJhY3QgQSB7CiAgICBmdW5jdGlvbiBzcGFtKCkgcHVibGljIHZpcnR1YWwgcHVyZTsKICAgIGZ1bmN0aW9uIGhhbSgpIHB1YmxpYyB2aXJ0dWFsIHB1cmU7Cn0KCgpjb250cmFjdCBCIGlzIEEgewogICAgZnVuY3Rpb24gc3BhbSgpIHB1YmxpYyBwdXJlIG92ZXJyaWRlIHsKICAgICAgICAvLyAuLi4KICAgIH0KCiAgICBmdW5jdGlvbiBoYW0oKSBwdWJsaWMgcHVyZSBvdmVycmlkZSB7CiAgICAgICAgLy8gLi4uCiAgICB9Cn0=)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

abstract contract A {
    function spam() public virtual pure;
    function ham() public virtual pure;
}


contract B is A {
    function spam() public pure override {
        // ...
    }

    function ham() public pure override {
        // ...
    }
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC42LjAgPDAuOS4wOwoKYWJzdHJhY3QgY29udHJhY3QgQSB7CiAgICBmdW5jdGlvbiBzcGFtKCkgdmlydHVhbCBwdXJlIHB1YmxpYzsKICAgIGZ1bmN0aW9uIGhhbSgpIHB1YmxpYyB2aXJ0dWFsIHB1cmU7Cn0KCgpjb250cmFjdCBCIGlzIEEgewogICAgZnVuY3Rpb24gc3BhbSgpIHB1YmxpYyBwdXJlIG92ZXJyaWRlIHsKICAgICAgICAvLyAuLi4KICAgIH0KICAgIGZ1bmN0aW9uIGhhbSgpIHB1YmxpYyBwdXJlIG92ZXJyaWRlIHsKICAgICAgICAvLyAuLi4KICAgIH0KfQ==)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

abstract contract A {
    function spam() virtual pure public;
    function ham() public virtual pure;
}


contract B is A {
    function spam() public pure override {
        // ...
    }
    function ham() public pure override {
        // ...
    }
}

```


### Maximum Line Length[](#maximum-line-length "Permalink to this heading")

Maximum suggested line length is 120 characters.

Wrapped lines should conform to the following guidelines.

1.  The first argument should not be attached to the opening parenthesis.
    
2.  One, and only one, indent should be used.
    
3.  Each argument should fall on its own line.
    
4.  The terminating element, `);`, should be placed on the final line by itself.
    

Function Calls

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=dGhpc0Z1bmN0aW9uQ2FsbElzUmVhbGx5TG9uZygKICAgIGxvbmdBcmd1bWVudDEsCiAgICBsb25nQXJndW1lbnQyLAogICAgbG9uZ0FyZ3VtZW50MwopOw==)

```
thisFunctionCallIsReallyLong(
    longArgument1,
    longArgument2,
    longArgument3
);

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=dGhpc0Z1bmN0aW9uQ2FsbElzUmVhbGx5TG9uZyhsb25nQXJndW1lbnQxLAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICBsb25nQXJndW1lbnQyLAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICBsb25nQXJndW1lbnQzCik7Cgp0aGlzRnVuY3Rpb25DYWxsSXNSZWFsbHlMb25nKGxvbmdBcmd1bWVudDEsCiAgICBsb25nQXJndW1lbnQyLAogICAgbG9uZ0FyZ3VtZW50MwopOwoKdGhpc0Z1bmN0aW9uQ2FsbElzUmVhbGx5TG9uZygKICAgIGxvbmdBcmd1bWVudDEsIGxvbmdBcmd1bWVudDIsCiAgICBsb25nQXJndW1lbnQzCik7Cgp0aGlzRnVuY3Rpb25DYWxsSXNSZWFsbHlMb25nKApsb25nQXJndW1lbnQxLApsb25nQXJndW1lbnQyLApsb25nQXJndW1lbnQzCik7Cgp0aGlzRnVuY3Rpb25DYWxsSXNSZWFsbHlMb25nKAogICAgbG9uZ0FyZ3VtZW50MSwKICAgIGxvbmdBcmd1bWVudDIsCiAgICBsb25nQXJndW1lbnQzKTs=)

```
thisFunctionCallIsReallyLong(longArgument1,
                              longArgument2,
                              longArgument3
);

thisFunctionCallIsReallyLong(longArgument1,
    longArgument2,
    longArgument3
);

thisFunctionCallIsReallyLong(
    longArgument1, longArgument2,
    longArgument3
);

thisFunctionCallIsReallyLong(
longArgument1,
longArgument2,
longArgument3
);

thisFunctionCallIsReallyLong(
    longArgument1,
    longArgument2,
    longArgument3);

```


Assignment Statements

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=dGhpc0lzQUxvbmdOZXN0ZWRNYXBwaW5nW2JlaW5nXVtzZXRdW3RvU29tZVZhbHVlXSA9IHNvbWVGdW5jdGlvbigKICAgIGFyZ3VtZW50MSwKICAgIGFyZ3VtZW50MiwKICAgIGFyZ3VtZW50MywKICAgIGFyZ3VtZW50NAopOw==)

```
thisIsALongNestedMapping[being][set][toSomeValue] = someFunction(
    argument1,
    argument2,
    argument3,
    argument4
);

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=dGhpc0lzQUxvbmdOZXN0ZWRNYXBwaW5nW2JlaW5nXVtzZXRdW3RvU29tZVZhbHVlXSA9IHNvbWVGdW5jdGlvbihhcmd1bWVudDEsCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICBhcmd1bWVudDIsCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICBhcmd1bWVudDMsCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICBhcmd1bWVudDQpOw==)

```
thisIsALongNestedMapping[being][set][toSomeValue] = someFunction(argument1,
                                                                   argument2,
                                                                   argument3,
                                                                   argument4);

```


Event Definitions and Event Emitters

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZXZlbnQgTG9uZ0FuZExvdHNPZkFyZ3MoCiAgICBhZGRyZXNzIHNlbmRlciwKICAgIGFkZHJlc3MgcmVjaXBpZW50LAogICAgdWludDI1NiBwdWJsaWNLZXksCiAgICB1aW50MjU2IGFtb3VudCwKICAgIGJ5dGVzMzJbXSBvcHRpb25zCik7CgpMb25nQW5kTG90c09mQXJncygKICAgIHNlbmRlciwKICAgIHJlY2lwaWVudCwKICAgIHB1YmxpY0tleSwKICAgIGFtb3VudCwKICAgIG9wdGlvbnMKKTs=)

```
event LongAndLotsOfArgs(
    address sender,
    address recipient,
    uint256 publicKey,
    uint256 amount,
    bytes32[] options
);

LongAndLotsOfArgs(
    sender,
    recipient,
    publicKey,
    amount,
    options
);

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZXZlbnQgTG9uZ0FuZExvdHNPZkFyZ3MoYWRkcmVzcyBzZW5kZXIsCiAgICAgICAgICAgICAgICAgICAgICAgIGFkZHJlc3MgcmVjaXBpZW50LAogICAgICAgICAgICAgICAgICAgICAgICB1aW50MjU2IHB1YmxpY0tleSwKICAgICAgICAgICAgICAgICAgICAgICAgdWludDI1NiBhbW91bnQsCiAgICAgICAgICAgICAgICAgICAgICAgIGJ5dGVzMzJbXSBvcHRpb25zKTsKCkxvbmdBbmRMb3RzT2ZBcmdzKHNlbmRlciwKICAgICAgICAgICAgICAgICAgcmVjaXBpZW50LAogICAgICAgICAgICAgICAgICBwdWJsaWNLZXksCiAgICAgICAgICAgICAgICAgIGFtb3VudCwKICAgICAgICAgICAgICAgICAgb3B0aW9ucyk7)

```
event LongAndLotsOfArgs(address sender,
                        address recipient,
                        uint256 publicKey,
                        uint256 amount,
                        bytes32[] options);

LongAndLotsOfArgs(sender,
                  recipient,
                  publicKey,
                  amount,
                  options);

```


### Source File Encoding[](#source-file-encoding "Permalink to this heading")

UTF-8 or ASCII encoding is preferred.

### Imports[](#imports "Permalink to this heading")

Import statements should always be placed at the top of the file.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKaW1wb3J0ICIuL093bmVkLnNvbCI7Cgpjb250cmFjdCBBIHsKICAgIC8vIC4uLgp9CgoKY29udHJhY3QgQiBpcyBPd25lZCB7CiAgICAvLyAuLi4KfQ==)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

import "./Owned.sol";

contract A {
    // ...
}


contract B is Owned {
    // ...
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgQSB7CiAgICAvLyAuLi4KfQoKCmltcG9ydCAiLi9Pd25lZC5zb2wiOwoKCmNvbnRyYWN0IEIgaXMgT3duZWQgewogICAgLy8gLi4uCn0=)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract A {
    // ...
}


import "./Owned.sol";


contract B is Owned {
    // ...
}

```


### Order of Functions[](#order-of-functions "Permalink to this heading")

Ordering helps readers identify which functions they can call and to find the constructor and fallback definitions easier.

Functions should be grouped according to their visibility and ordered:

*   constructor
    
*   receive function (if exists)
    
*   fallback function (if exists)
    
*   external
    
*   public
    
*   internal
    
*   private
    

Within a grouping, place the `view` and `pure` functions last.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwpjb250cmFjdCBBIHsKICAgIGNvbnN0cnVjdG9yKCkgewogICAgICAgIC8vIC4uLgogICAgfQoKICAgIHJlY2VpdmUoKSBleHRlcm5hbCBwYXlhYmxlIHsKICAgICAgICAvLyAuLi4KICAgIH0KCiAgICBmYWxsYmFjaygpIGV4dGVybmFsIHsKICAgICAgICAvLyAuLi4KICAgIH0KCiAgICAvLyBFeHRlcm5hbCBmdW5jdGlvbnMKICAgIC8vIC4uLgoKICAgIC8vIEV4dGVybmFsIGZ1bmN0aW9ucyB0aGF0IGFyZSB2aWV3CiAgICAvLyAuLi4KCiAgICAvLyBFeHRlcm5hbCBmdW5jdGlvbnMgdGhhdCBhcmUgcHVyZQogICAgLy8gLi4uCgogICAgLy8gUHVibGljIGZ1bmN0aW9ucwogICAgLy8gLi4uCgogICAgLy8gSW50ZXJuYWwgZnVuY3Rpb25zCiAgICAvLyAuLi4KCiAgICAvLyBQcml2YXRlIGZ1bmN0aW9ucwogICAgLy8gLi4uCn0=)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;
contract A {
    constructor() {
        // ...
    }

    receive() external payable {
        // ...
    }

    fallback() external {
        // ...
    }

    // External functions
    // ...

    // External functions that are view
    // ...

    // External functions that are pure
    // ...

    // Public functions
    // ...

    // Internal functions
    // ...

    // Private functions
    // ...
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwpjb250cmFjdCBBIHsKCiAgICAvLyBFeHRlcm5hbCBmdW5jdGlvbnMKICAgIC8vIC4uLgoKICAgIGZhbGxiYWNrKCkgZXh0ZXJuYWwgewogICAgICAgIC8vIC4uLgogICAgfQogICAgcmVjZWl2ZSgpIGV4dGVybmFsIHBheWFibGUgewogICAgICAgIC8vIC4uLgogICAgfQoKICAgIC8vIFByaXZhdGUgZnVuY3Rpb25zCiAgICAvLyAuLi4KCiAgICAvLyBQdWJsaWMgZnVuY3Rpb25zCiAgICAvLyAuLi4KCiAgICBjb25zdHJ1Y3RvcigpIHsKICAgICAgICAvLyAuLi4KICAgIH0KCiAgICAvLyBJbnRlcm5hbCBmdW5jdGlvbnMKICAgIC8vIC4uLgp9)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;
contract A {

    // External functions
    // ...

    fallback() external {
        // ...
    }
    receive() external payable {
        // ...
    }

    // Private functions
    // ...

    // Public functions
    // ...

    constructor() {
        // ...
    }

    // Internal functions
    // ...
}

```


### Whitespace in Expressions[](#whitespace-in-expressions "Permalink to this heading")

Avoid extraneous whitespace in the following situations:

Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=c3BhbShoYW1bMV0sIENvaW4oe25hbWU6ICJoYW0ifSkpOw==)

```
spam(ham[1], Coin({name: "ham"}));

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=c3BhbSggaGFtWyAxIF0sIENvaW4oIHsgbmFtZTogImhhbSIgfSApICk7)

```
spam( ham[ 1 ], Coin( { name: "ham" } ) );

```


Exception:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gc2luZ2xlTGluZSgpIHB1YmxpYyB7IHNwYW0oKTsgfQ==)

```
function singleLine() public { spam(); }

```


Immediately before a comma, semicolon:

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gc3BhbSh1aW50IGksIENvaW4gY29pbikgcHVibGljOw==)

```
function spam(uint i, Coin coin) public;

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gc3BhbSh1aW50IGkgLCBDb2luIGNvaW4pIHB1YmxpYyA7)

```
function spam(uint i , Coin coin) public ;

```


More than one space around an assignment or other operator to align with another:

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=eCA9IDE7CnkgPSAyOwpsb25nVmFyaWFibGUgPSAzOw==)

```
x = 1;
y = 2;
longVariable = 3;

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=eCAgICAgICAgICAgID0gMTsKeSAgICAgICAgICAgID0gMjsKbG9uZ1ZhcmlhYmxlID0gMzs=)

```
x            = 1;
y            = 2;
longVariable = 3;

```


Don’t include a whitespace in the receive and fallback functions:

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=cmVjZWl2ZSgpIGV4dGVybmFsIHBheWFibGUgewogICAgLi4uCn0KCmZhbGxiYWNrKCkgZXh0ZXJuYWwgewogICAgLi4uCn0=)

```
receive() external payable {
    ...
}

fallback() external {
    ...
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=cmVjZWl2ZSAoKSBleHRlcm5hbCBwYXlhYmxlIHsKICAgIC4uLgp9CgpmYWxsYmFjayAoKSBleHRlcm5hbCB7CiAgICAuLi4KfQ==)

```
receive () external payable {
    ...
}

fallback () external {
    ...
}

```


### Control Structures[](#control-structures "Permalink to this heading")

The braces denoting the body of a contract, library, functions and structs should:

*   open on the same line as the declaration
    
*   close on their own line at the same indentation level as the beginning of the declaration.
    
*   The opening brace should be preceded by a single space.
    

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgQ29pbiB7CiAgICBzdHJ1Y3QgQmFuayB7CiAgICAgICAgYWRkcmVzcyBvd25lcjsKICAgICAgICB1aW50IGJhbGFuY2U7CiAgICB9Cn0=)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract Coin {
    struct Bank {
        address owner;
        uint balance;
    }
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKY29udHJhY3QgQ29pbgp7CiAgICBzdHJ1Y3QgQmFuayB7CiAgICAgICAgYWRkcmVzcyBvd25lcjsKICAgICAgICB1aW50IGJhbGFuY2U7CiAgICB9Cn0=)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract Coin
{
    struct Bank {
        address owner;
        uint balance;
    }
}

```


The same recommendations apply to the control structures `if`, `else`, `while`, and `for`.

Additionally there should be a single space between the control structures `if`, `while`, and `for` and the parenthetic block representing the conditional, as well as a single space between the conditional parenthetic block and the opening brace.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=aWYgKC4uLikgewogICAgLi4uCn0KCmZvciAoLi4uKSB7CiAgICAuLi4KfQ==)

```
if (...) {
    ...
}

for (...) {
    ...
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=aWYgKC4uLikKewogICAgLi4uCn0KCndoaWxlKC4uLil7Cn0KCmZvciAoLi4uKSB7CiAgICAuLi47fQ==)

```
if (...)
{
    ...
}

while(...){
}

for (...) {
    ...;}

```


For control structures whose body contains a single statement, omitting the braces is ok _if_ the statement is contained on a single line.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=aWYgKHggPCAxMCkKICAgIHggKz0gMTs=)

No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=aWYgKHggPCAxMCkKICAgIHNvbWVBcnJheS5wdXNoKENvaW4oewogICAgICAgIG5hbWU6ICdzcGFtJywKICAgICAgICB2YWx1ZTogNDIKICAgIH0pKTs=)

```
if (x < 10)
    someArray.push(Coin({
        name: 'spam',
        value: 42
    }));

```


For `if` blocks which have an `else` or `else if` clause, the `else` should be placed on the same line as the `if`’s closing brace. This is an exception compared to the rules of other block-like structures.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=aWYgKHggPCAzKSB7CiAgICB4ICs9IDE7Cn0gZWxzZSBpZiAoeCA+IDcpIHsKICAgIHggLT0gMTsKfSBlbHNlIHsKICAgIHggPSA1Owp9CgoKaWYgKHggPCAzKQogICAgeCArPSAxOwplbHNlCiAgICB4IC09IDE7)

```
if (x < 3) {
    x += 1;
} else if (x > 7) {
    x -= 1;
} else {
    x = 5;
}


if (x < 3)
    x += 1;
else
    x -= 1;

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=aWYgKHggPCAzKSB7CiAgICB4ICs9IDE7Cn0KZWxzZSB7CiAgICB4IC09IDE7Cn0=)

```
if (x < 3) {
    x += 1;
}
else {
    x -= 1;
}

```


### Function Declaration[](#function-declaration "Permalink to this heading")

For short function declarations, it is recommended for the opening brace of the function body to be kept on the same line as the function declaration.

The closing brace should be at the same indentation level as the function declaration.

The opening brace should be preceded by a single space.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gaW5jcmVtZW50KHVpbnQgeCkgcHVibGljIHB1cmUgcmV0dXJucyAodWludCkgewogICAgcmV0dXJuIHggKyAxOwp9CgpmdW5jdGlvbiBpbmNyZW1lbnQodWludCB4KSBwdWJsaWMgcHVyZSBvbmx5T3duZXIgcmV0dXJucyAodWludCkgewogICAgcmV0dXJuIHggKyAxOwp9)

```
function increment(uint x) public pure returns (uint) {
    return x + 1;
}

function increment(uint x) public pure onlyOwner returns (uint) {
    return x + 1;
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gaW5jcmVtZW50KHVpbnQgeCkgcHVibGljIHB1cmUgcmV0dXJucyAodWludCkKewogICAgcmV0dXJuIHggKyAxOwp9CgpmdW5jdGlvbiBpbmNyZW1lbnQodWludCB4KSBwdWJsaWMgcHVyZSByZXR1cm5zICh1aW50KXsKICAgIHJldHVybiB4ICsgMTsKfQoKZnVuY3Rpb24gaW5jcmVtZW50KHVpbnQgeCkgcHVibGljIHB1cmUgcmV0dXJucyAodWludCkgewogICAgcmV0dXJuIHggKyAxOwogICAgfQoKZnVuY3Rpb24gaW5jcmVtZW50KHVpbnQgeCkgcHVibGljIHB1cmUgcmV0dXJucyAodWludCkgewogICAgcmV0dXJuIHggKyAxO30=)

```
function increment(uint x) public pure returns (uint)
{
    return x + 1;
}

function increment(uint x) public pure returns (uint){
    return x + 1;
}

function increment(uint x) public pure returns (uint) {
    return x + 1;
    }

function increment(uint x) public pure returns (uint) {
    return x + 1;}

```


The modifier order for a function should be:

1.  Visibility
    
2.  Mutability
    
3.  Virtual
    
4.  Override
    
5.  Custom modifiers
    

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gYmFsYW5jZSh1aW50IGZyb20pIHB1YmxpYyB2aWV3IG92ZXJyaWRlIHJldHVybnMgKHVpbnQpICB7CiAgICByZXR1cm4gYmFsYW5jZU9mW2Zyb21dOwp9CgpmdW5jdGlvbiBzaHV0ZG93bigpIHB1YmxpYyBvbmx5T3duZXIgewogICAgc2VsZmRlc3RydWN0KG93bmVyKTsKfQ==)

```
function balance(uint from) public view override returns (uint)  {
    return balanceOf[from];
}

function shutdown() public onlyOwner {
    selfdestruct(owner);
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gYmFsYW5jZSh1aW50IGZyb20pIHB1YmxpYyBvdmVycmlkZSB2aWV3IHJldHVybnMgKHVpbnQpICB7CiAgICByZXR1cm4gYmFsYW5jZU9mW2Zyb21dOwp9CgpmdW5jdGlvbiBzaHV0ZG93bigpIG9ubHlPd25lciBwdWJsaWMgewogICAgc2VsZmRlc3RydWN0KG93bmVyKTsKfQ==)

```
function balance(uint from) public override view returns (uint)  {
    return balanceOf[from];
}

function shutdown() onlyOwner public {
    selfdestruct(owner);
}

```


For long function declarations, it is recommended to drop each argument onto its own line at the same indentation level as the function body. The closing parenthesis and opening bracket should be placed on their own line as well at the same indentation level as the function declaration.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gdGhpc0Z1bmN0aW9uSGFzTG90c09mQXJndW1lbnRzKAogICAgYWRkcmVzcyBhLAogICAgYWRkcmVzcyBiLAogICAgYWRkcmVzcyBjLAogICAgYWRkcmVzcyBkLAogICAgYWRkcmVzcyBlLAogICAgYWRkcmVzcyBmCikKICAgIHB1YmxpYwp7CiAgICBkb1NvbWV0aGluZygpOwp9)

```
function thisFunctionHasLotsOfArguments(
    address a,
    address b,
    address c,
    address d,
    address e,
    address f
)
    public
{
    doSomething();
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gdGhpc0Z1bmN0aW9uSGFzTG90c09mQXJndW1lbnRzKGFkZHJlc3MgYSwgYWRkcmVzcyBiLCBhZGRyZXNzIGMsCiAgICBhZGRyZXNzIGQsIGFkZHJlc3MgZSwgYWRkcmVzcyBmKSBwdWJsaWMgewogICAgZG9Tb21ldGhpbmcoKTsKfQoKZnVuY3Rpb24gdGhpc0Z1bmN0aW9uSGFzTG90c09mQXJndW1lbnRzKGFkZHJlc3MgYSwKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIGFkZHJlc3MgYiwKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIGFkZHJlc3MgYywKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIGFkZHJlc3MgZCwKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIGFkZHJlc3MgZSwKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIGFkZHJlc3MgZikgcHVibGljIHsKICAgIGRvU29tZXRoaW5nKCk7Cn0KCmZ1bmN0aW9uIHRoaXNGdW5jdGlvbkhhc0xvdHNPZkFyZ3VtZW50cygKICAgIGFkZHJlc3MgYSwKICAgIGFkZHJlc3MgYiwKICAgIGFkZHJlc3MgYywKICAgIGFkZHJlc3MgZCwKICAgIGFkZHJlc3MgZSwKICAgIGFkZHJlc3MgZikgcHVibGljIHsKICAgIGRvU29tZXRoaW5nKCk7Cn0=)

```
function thisFunctionHasLotsOfArguments(address a, address b, address c,
    address d, address e, address f) public {
    doSomething();
}

function thisFunctionHasLotsOfArguments(address a,
                                        address b,
                                        address c,
                                        address d,
                                        address e,
                                        address f) public {
    doSomething();
}

function thisFunctionHasLotsOfArguments(
    address a,
    address b,
    address c,
    address d,
    address e,
    address f) public {
    doSomething();
}

```


If a long function declaration has modifiers, then each modifier should be dropped to its own line.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gdGhpc0Z1bmN0aW9uTmFtZUlzUmVhbGx5TG9uZyhhZGRyZXNzIHgsIGFkZHJlc3MgeSwgYWRkcmVzcyB6KQogICAgcHVibGljCiAgICBvbmx5T3duZXIKICAgIHByaWNlZAogICAgcmV0dXJucyAoYWRkcmVzcykKewogICAgZG9Tb21ldGhpbmcoKTsKfQoKZnVuY3Rpb24gdGhpc0Z1bmN0aW9uTmFtZUlzUmVhbGx5TG9uZygKICAgIGFkZHJlc3MgeCwKICAgIGFkZHJlc3MgeSwKICAgIGFkZHJlc3MgegopCiAgICBwdWJsaWMKICAgIG9ubHlPd25lcgogICAgcHJpY2VkCiAgICByZXR1cm5zIChhZGRyZXNzKQp7CiAgICBkb1NvbWV0aGluZygpOwp9)

```
function thisFunctionNameIsReallyLong(address x, address y, address z)
    public
    onlyOwner
    priced
    returns (address)
{
    doSomething();
}

function thisFunctionNameIsReallyLong(
    address x,
    address y,
    address z
)
    public
    onlyOwner
    priced
    returns (address)
{
    doSomething();
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gdGhpc0Z1bmN0aW9uTmFtZUlzUmVhbGx5TG9uZyhhZGRyZXNzIHgsIGFkZHJlc3MgeSwgYWRkcmVzcyB6KQogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIHB1YmxpYwogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIG9ubHlPd25lcgogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIHByaWNlZAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIHJldHVybnMgKGFkZHJlc3MpIHsKICAgIGRvU29tZXRoaW5nKCk7Cn0KCmZ1bmN0aW9uIHRoaXNGdW5jdGlvbk5hbWVJc1JlYWxseUxvbmcoYWRkcmVzcyB4LCBhZGRyZXNzIHksIGFkZHJlc3MgeikKICAgIHB1YmxpYyBvbmx5T3duZXIgcHJpY2VkIHJldHVybnMgKGFkZHJlc3MpCnsKICAgIGRvU29tZXRoaW5nKCk7Cn0KCmZ1bmN0aW9uIHRoaXNGdW5jdGlvbk5hbWVJc1JlYWxseUxvbmcoYWRkcmVzcyB4LCBhZGRyZXNzIHksIGFkZHJlc3MgeikKICAgIHB1YmxpYwogICAgb25seU93bmVyCiAgICBwcmljZWQKICAgIHJldHVybnMgKGFkZHJlc3MpIHsKICAgIGRvU29tZXRoaW5nKCk7Cn0=)

```
function thisFunctionNameIsReallyLong(address x, address y, address z)
                                      public
                                      onlyOwner
                                      priced
                                      returns (address) {
    doSomething();
}

function thisFunctionNameIsReallyLong(address x, address y, address z)
    public onlyOwner priced returns (address)
{
    doSomething();
}

function thisFunctionNameIsReallyLong(address x, address y, address z)
    public
    onlyOwner
    priced
    returns (address) {
    doSomething();
}

```


Multiline output parameters and return statements should follow the same style recommended for wrapping long lines found in the [Maximum Line Length](#maximum-line-length) section.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gdGhpc0Z1bmN0aW9uTmFtZUlzUmVhbGx5TG9uZygKICAgIGFkZHJlc3MgYSwKICAgIGFkZHJlc3MgYiwKICAgIGFkZHJlc3MgYwopCiAgICBwdWJsaWMKICAgIHJldHVybnMgKAogICAgICAgIGFkZHJlc3Mgc29tZUFkZHJlc3NOYW1lLAogICAgICAgIHVpbnQyNTYgTG9uZ0FyZ3VtZW50LAogICAgICAgIHVpbnQyNTYgQXJndW1lbnQKICAgICkKewogICAgZG9Tb21ldGhpbmcoKQoKICAgIHJldHVybiAoCiAgICAgICAgdmVyeUxvbmdSZXR1cm5BcmcxLAogICAgICAgIHZlcnlMb25nUmV0dXJuQXJnMiwKICAgICAgICB2ZXJ5TG9uZ1JldHVybkFyZzMKICAgICk7Cn0=)

```
function thisFunctionNameIsReallyLong(
    address a,
    address b,
    address c
)
    public
    returns (
        address someAddressName,
        uint256 LongArgument,
        uint256 Argument
    )
{
    doSomething()

    return (
        veryLongReturnArg1,
        veryLongReturnArg2,
        veryLongReturnArg3
    );
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gdGhpc0Z1bmN0aW9uTmFtZUlzUmVhbGx5TG9uZygKICAgIGFkZHJlc3MgYSwKICAgIGFkZHJlc3MgYiwKICAgIGFkZHJlc3MgYwopCiAgICBwdWJsaWMKICAgIHJldHVybnMgKGFkZHJlc3Mgc29tZUFkZHJlc3NOYW1lLAogICAgICAgICAgICAgdWludDI1NiBMb25nQXJndW1lbnQsCiAgICAgICAgICAgICB1aW50MjU2IEFyZ3VtZW50KQp7CiAgICBkb1NvbWV0aGluZygpCgogICAgcmV0dXJuICh2ZXJ5TG9uZ1JldHVybkFyZzEsCiAgICAgICAgICAgIHZlcnlMb25nUmV0dXJuQXJnMSwKICAgICAgICAgICAgdmVyeUxvbmdSZXR1cm5BcmcxKTsKfQ==)

```
function thisFunctionNameIsReallyLong(
    address a,
    address b,
    address c
)
    public
    returns (address someAddressName,
             uint256 LongArgument,
             uint256 Argument)
{
    doSomething()

    return (veryLongReturnArg1,
            veryLongReturnArg1,
            veryLongReturnArg1);
}

```


For constructor functions on inherited contracts whose bases require arguments, it is recommended to drop the base constructors onto new lines in the same manner as modifiers if the function declaration is long or hard to read.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwovLyBCYXNlIGNvbnRyYWN0cyBqdXN0IHRvIG1ha2UgdGhpcyBjb21waWxlCmNvbnRyYWN0IEIgewogICAgY29uc3RydWN0b3IodWludCkgewogICAgfQp9CgoKY29udHJhY3QgQyB7CiAgICBjb25zdHJ1Y3Rvcih1aW50LCB1aW50KSB7CiAgICB9Cn0KCgpjb250cmFjdCBEIHsKICAgIGNvbnN0cnVjdG9yKHVpbnQpIHsKICAgIH0KfQoKCmNvbnRyYWN0IEEgaXMgQiwgQywgRCB7CiAgICB1aW50IHg7CgogICAgY29uc3RydWN0b3IodWludCBwYXJhbTEsIHVpbnQgcGFyYW0yLCB1aW50IHBhcmFtMywgdWludCBwYXJhbTQsIHVpbnQgcGFyYW01KQogICAgICAgIEIocGFyYW0xKQogICAgICAgIEMocGFyYW0yLCBwYXJhbTMpCiAgICAgICAgRChwYXJhbTQpCiAgICB7CiAgICAgICAgLy8gZG8gc29tZXRoaW5nIHdpdGggcGFyYW01CiAgICAgICAgeCA9IHBhcmFtNTsKICAgIH0KfQ==)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;
// Base contracts just to make this compile
contract B {
    constructor(uint) {
    }
}


contract C {
    constructor(uint, uint) {
    }
}


contract D {
    constructor(uint) {
    }
}


contract A is B, C, D {
    uint x;

    constructor(uint param1, uint param2, uint param3, uint param4, uint param5)
        B(param1)
        C(param2, param3)
        D(param4)
    {
        // do something with param5
        x = param5;
    }
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwoKLy8gQmFzZSBjb250cmFjdHMganVzdCB0byBtYWtlIHRoaXMgY29tcGlsZQpjb250cmFjdCBCIHsKICAgIGNvbnN0cnVjdG9yKHVpbnQpIHsKICAgIH0KfQoKCmNvbnRyYWN0IEMgewogICAgY29uc3RydWN0b3IodWludCwgdWludCkgewogICAgfQp9CgoKY29udHJhY3QgRCB7CiAgICBjb25zdHJ1Y3Rvcih1aW50KSB7CiAgICB9Cn0KCgpjb250cmFjdCBBIGlzIEIsIEMsIEQgewogICAgdWludCB4OwoKICAgIGNvbnN0cnVjdG9yKHVpbnQgcGFyYW0xLCB1aW50IHBhcmFtMiwgdWludCBwYXJhbTMsIHVpbnQgcGFyYW00LCB1aW50IHBhcmFtNSkKICAgIEIocGFyYW0xKQogICAgQyhwYXJhbTIsIHBhcmFtMykKICAgIEQocGFyYW00KSB7CiAgICAgICAgeCA9IHBhcmFtNTsKICAgIH0KfQoKCmNvbnRyYWN0IFggaXMgQiwgQywgRCB7CiAgICB1aW50IHg7CgogICAgY29uc3RydWN0b3IodWludCBwYXJhbTEsIHVpbnQgcGFyYW0yLCB1aW50IHBhcmFtMywgdWludCBwYXJhbTQsIHVpbnQgcGFyYW01KQogICAgICAgIEIocGFyYW0xKQogICAgICAgIEMocGFyYW0yLCBwYXJhbTMpCiAgICAgICAgRChwYXJhbTQpIHsKICAgICAgICAgICAgeCA9IHBhcmFtNTsKICAgICAgICB9Cn0=)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

// Base contracts just to make this compile
contract B {
    constructor(uint) {
    }
}


contract C {
    constructor(uint, uint) {
    }
}


contract D {
    constructor(uint) {
    }
}


contract A is B, C, D {
    uint x;

    constructor(uint param1, uint param2, uint param3, uint param4, uint param5)
    B(param1)
    C(param2, param3)
    D(param4) {
        x = param5;
    }
}


contract X is B, C, D {
    uint x;

    constructor(uint param1, uint param2, uint param3, uint param4, uint param5)
        B(param1)
        C(param2, param3)
        D(param4) {
            x = param5;
        }
}

```


When declaring short functions with a single statement, it is permissible to do it on a single line.

Permissible:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=ZnVuY3Rpb24gc2hvcnRGdW5jdGlvbigpIHB1YmxpYyB7IGRvU29tZXRoaW5nKCk7IH0=)

```
function shortFunction() public { doSomething(); }

```


These guidelines for function declarations are intended to improve readability. Authors should use their best judgment as this guide does not try to cover all possible permutations for function declarations.

### Mappings[](#mappings "Permalink to this heading")

In variable declarations, do not separate the keyword `mapping` from its type by a space. Do not separate any nested `mapping` keyword from its type by whitespace.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=bWFwcGluZyh1aW50ID0+IHVpbnQpIG1hcDsKbWFwcGluZyhhZGRyZXNzID0+IGJvb2wpIHJlZ2lzdGVyZWRBZGRyZXNzZXM7Cm1hcHBpbmcodWludCA9PiBtYXBwaW5nKGJvb2wgPT4gRGF0YVtdKSkgcHVibGljIGRhdGE7Cm1hcHBpbmcodWludCA9PiBtYXBwaW5nKHVpbnQgPT4gcykpIGRhdGE7)

```
mapping(uint => uint) map;
mapping(address => bool) registeredAddresses;
mapping(uint => mapping(bool => Data[])) public data;
mapping(uint => mapping(uint => s)) data;

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=bWFwcGluZyAodWludCA9PiB1aW50KSBtYXA7Cm1hcHBpbmcoIGFkZHJlc3MgPT4gYm9vbCApIHJlZ2lzdGVyZWRBZGRyZXNzZXM7Cm1hcHBpbmcgKHVpbnQgPT4gbWFwcGluZyAoYm9vbCA9PiBEYXRhW10pKSBwdWJsaWMgZGF0YTsKbWFwcGluZyh1aW50ID0+IG1hcHBpbmcgKHVpbnQgPT4gcykpIGRhdGE7)

```
mapping (uint => uint) map;
mapping( address => bool ) registeredAddresses;
mapping (uint => mapping (bool => Data[])) public data;
mapping(uint => mapping (uint => s)) data;

```


### Variable Declarations[](#variable-declarations "Permalink to this heading")

Declarations of array variables should not have a space between the type and the brackets.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=dWludFtdIHg7)

No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=dWludCBbXSB4Ow==)

### Other Recommendations[](#other-recommendations "Permalink to this heading")

*   Strings should be quoted with double-quotes instead of single-quotes.
    

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=c3RyID0gImZvbyI7CnN0ciA9ICJIYW1sZXQgc2F5cywgJ1RvIGJlIG9yIG5vdCB0byBiZS4uLiciOw==)

```
str = "foo";
str = "Hamlet says, 'To be or not to be...'";

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=c3RyID0gJ2Jhcic7CnN0ciA9ICciQmUgeW91cnNlbGY7IGV2ZXJ5b25lIGVsc2UgaXMgYWxyZWFkeSB0YWtlbi4iIC1Pc2NhciBXaWxkZSc7)

```
str = 'bar';
str = '"Be yourself; everyone else is already taken." -Oscar Wilde';

```


*   Surround operators with a single space on either side.
    

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=eCA9IDM7CnggPSAxMDAgLyAxMDsKeCArPSAzICsgNDsKeCB8PSB5ICYmIHo7)

```
x = 3;
x = 100 / 10;
x += 3 + 4;
x |= y && z;

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=eD0zOwp4ID0gMTAwLzEwOwp4ICs9IDMrNDsKeCB8PSB5JiZ6Ow==)

```
x=3;
x = 100/10;
x += 3+4;
x |= y&&z;

```


*   Operators with a higher priority than others can exclude surrounding whitespace in order to denote precedence. This is meant to allow for improved readability for complex statements. You should always use the same amount of whitespace on either side of an operator:
    

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=eCA9IDIqKjMgKyA1Owp4ID0gMip5ICsgMyp6Owp4ID0gKGErYikgKiAoYS1iKTs=)

```
x = 2**3 + 5;
x = 2*y + 3*z;
x = (a+b) * (a-b);

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=eCA9IDIqKiAzICsgNTsKeCA9IHkrejsKeCArPTE7)

```
x = 2** 3 + 5;
x = y+z;
x +=1;

```


Order of Layout[](#order-of-layout "Permalink to this heading")
----------------------------------------------------------------

Layout contract elements in the following order:

1.  Pragma statements
    
2.  Import statements
    
3.  Interfaces
    
4.  Libraries
    
5.  Contracts
    

Inside each contract, library or interface, use the following order:

1.  Type declarations
    
2.  State variables
    
3.  Events
    
4.  Modifiers
    
5.  Functions
    

Note

It might be clearer to declare types close to their use in events or state variables.

Naming Conventions[](#naming-conventions "Permalink to this heading")
----------------------------------------------------------------------

Naming conventions are powerful when adopted and used broadly. The use of different conventions can convey significant _meta_ information that would otherwise not be immediately available.

The naming recommendations given here are intended to improve the readability, and thus they are not rules, but rather guidelines to try and help convey the most information through the names of things.

Lastly, consistency within a codebase should always supersede any conventions outlined in this document.

### Naming Styles[](#naming-styles "Permalink to this heading")

To avoid confusion, the following names will be used to refer to different naming styles.

*   `b` (single lowercase letter)
    
*   `B` (single uppercase letter)
    
*   `lowercase`
    
*   `UPPERCASE`
    
*   `UPPER_CASE_WITH_UNDERSCORES`
    
*   `CapitalizedWords` (or CapWords)
    
*   `mixedCase` (differs from CapitalizedWords by initial lowercase character!)
    

Note

When using initialisms in CapWords, capitalize all the letters of the initialisms. Thus HTTPServerError is better than HttpServerError. When using initialisms in mixedCase, capitalize all the letters of the initialisms, except keep the first one lower case if it is the beginning of the name. Thus xmlHTTPRequest is better than XMLHTTPRequest.

### Names to Avoid[](#names-to-avoid "Permalink to this heading")

*   `l` - Lowercase letter el
    
*   `O` - Uppercase letter oh
    
*   `I` - Uppercase letter eye
    

Never use any of these for single letter variable names. They are often indistinguishable from the numerals one and zero.

### Contract and Library Names[](#contract-and-library-names "Permalink to this heading")

*   Contracts and libraries should be named using the CapWords style. Examples: `SimpleToken`, `SmartBank`, `CertificateHashRepository`, `Player`, `Congress`, `Owned`.
    
*   Contract and library names should also match their filenames.
    
*   If a contract file includes multiple contracts and/or libraries, then the filename should match the _core contract_. This is not recommended however if it can be avoided.
    

As shown in the example below, if the contract name is `Congress` and the library name is `Owned`, then their associated filenames should be `Congress.sol` and `Owned.sol`.

Yes:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwoKLy8gT3duZWQuc29sCmNvbnRyYWN0IE93bmVkIHsKICAgIGFkZHJlc3MgcHVibGljIG93bmVyOwoKICAgIGNvbnN0cnVjdG9yKCkgewogICAgICAgIG93bmVyID0gbXNnLnNlbmRlcjsKICAgIH0KCiAgICBtb2RpZmllciBvbmx5T3duZXIgewogICAgICAgIHJlcXVpcmUobXNnLnNlbmRlciA9PSBvd25lcik7CiAgICAgICAgXzsKICAgIH0KCiAgICBmdW5jdGlvbiB0cmFuc2Zlck93bmVyc2hpcChhZGRyZXNzIG5ld093bmVyKSBwdWJsaWMgb25seU93bmVyIHsKICAgICAgICBvd25lciA9IG5ld093bmVyOwogICAgfQp9)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

// Owned.sol
contract Owned {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    modifier onlyOwner {
        require(msg.sender == owner);
        _;
    }

    function transferOwnership(address newOwner) public onlyOwner {
        owner = newOwner;
    }
}

```


and in `Congress.sol`:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjAgPDAuOS4wOwoKaW1wb3J0ICIuL093bmVkLnNvbCI7CgoKY29udHJhY3QgQ29uZ3Jlc3MgaXMgT3duZWQsIFRva2VuUmVjaXBpZW50IHsKICAgIC8vLi4uCn0=)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

import "./Owned.sol";


contract Congress is Owned, TokenRecipient {
    //...
}

```


No:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC43LjAgPDAuOS4wOwoKLy8gb3duZWQuc29sCmNvbnRyYWN0IG93bmVkIHsKICAgIGFkZHJlc3MgcHVibGljIG93bmVyOwoKICAgIGNvbnN0cnVjdG9yKCkgewogICAgICAgIG93bmVyID0gbXNnLnNlbmRlcjsKICAgIH0KCiAgICBtb2RpZmllciBvbmx5T3duZXIgewogICAgICAgIHJlcXVpcmUobXNnLnNlbmRlciA9PSBvd25lcik7CiAgICAgICAgXzsKICAgIH0KCiAgICBmdW5jdGlvbiB0cmFuc2Zlck93bmVyc2hpcChhZGRyZXNzIG5ld093bmVyKSBwdWJsaWMgb25seU93bmVyIHsKICAgICAgICBvd25lciA9IG5ld093bmVyOwogICAgfQp9)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

// owned.sol
contract owned {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    modifier onlyOwner {
        require(msg.sender == owner);
        _;
    }

    function transferOwnership(address newOwner) public onlyOwner {
        owner = newOwner;
    }
}

```


and in `Congress.sol`:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5IF4wLjcuMDsKCgppbXBvcnQgIi4vb3duZWQuc29sIjsKCgpjb250cmFjdCBDb25ncmVzcyBpcyBvd25lZCwgdG9rZW5SZWNpcGllbnQgewogICAgLy8uLi4KfQ==)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.7.0;


import "./owned.sol";


contract Congress is owned, tokenRecipient {
    //...
}

```


### Struct Names[](#struct-names "Permalink to this heading")

Structs should be named using the CapWords style. Examples: `MyCoin`, `Position`, `PositionXY`.

### Event Names[](#event-names "Permalink to this heading")

Events should be named using the CapWords style. Examples: `Deposit`, `Transfer`, `Approval`, `BeforeTransfer`, `AfterTransfer`.

### Function Names[](#function-names "Permalink to this heading")

Functions should use mixedCase. Examples: `getBalance`, `transfer`, `verifyOwner`, `addMember`, `changeOwner`.

### Function Argument Names[](#function-argument-names "Permalink to this heading")

Function arguments should use mixedCase. Examples: `initialSupply`, `account`, `recipientAddress`, `senderAddress`, `newOwner`.

When writing library functions that operate on a custom struct, the struct should be the first argument and should always be named `self`.

### Local and State Variable Names[](#local-and-state-variable-names "Permalink to this heading")

Use mixedCase. Examples: `totalSupply`, `remainingSupply`, `balancesOf`, `creatorAddress`, `isPreSale`, `tokenExchangeRate`.

### Constants[](#constants "Permalink to this heading")

Constants should be named with all capital letters with underscores separating words. Examples: `MAX_BLOCKS`, `TOKEN_NAME`, `TOKEN_TICKER`, `CONTRACT_VERSION`.

### Modifier Names[](#modifier-names "Permalink to this heading")

Use mixedCase. Examples: `onlyBy`, `onlyAfter`, `onlyDuringThePreSale`.

### Enums[](#enums "Permalink to this heading")

Enums, in the style of simple type declarations, should be named using the CapWords style. Examples: `TokenGroup`, `Frame`, `HashStyle`, `CharacterLocation`.

### Avoiding Naming Collisions[](#avoiding-naming-collisions "Permalink to this heading")

*   `singleTrailingUnderscore_`
    

This convention is suggested when the desired name collides with that of an existing state variable, function, built-in or otherwise reserved name.

NatSpec[](#natspec "Permalink to this heading")
------------------------------------------------

Solidity contracts can also contain NatSpec comments. They are written with a triple slash (`///`) or a double asterisk block (`/** ... */`) and they should be used directly above function declarations or statements.

For example, the contract from [a simple smart contract](https://docs.soliditylang.org/en/v0.8.17/introduction-to-smart-contracts.html#simple-smart-contract) with the comments added looks like the one below:

[open in Remix](https://remix.ethereum.org/?language=solidity&version=0.8.17&code=Ly8gU1BEWC1MaWNlbnNlLUlkZW50aWZpZXI6IEdQTC0zLjAKcHJhZ21hIHNvbGlkaXR5ID49MC40LjE2IDwwLjkuMDsKCi8vLyBAYXV0aG9yIFRoZSBTb2xpZGl0eSBUZWFtCi8vLyBAdGl0bGUgQSBzaW1wbGUgc3RvcmFnZSBleGFtcGxlCmNvbnRyYWN0IFNpbXBsZVN0b3JhZ2UgewogICAgdWludCBzdG9yZWREYXRhOwoKICAgIC8vLyBTdG9yZSBgeGAuCiAgICAvLy8gQHBhcmFtIHggdGhlIG5ldyB2YWx1ZSB0byBzdG9yZQogICAgLy8vIEBkZXYgc3RvcmVzIHRoZSBudW1iZXIgaW4gdGhlIHN0YXRlIHZhcmlhYmxlIGBzdG9yZWREYXRhYAogICAgZnVuY3Rpb24gc2V0KHVpbnQgeCkgcHVibGljIHsKICAgICAgICBzdG9yZWREYXRhID0geDsKICAgIH0KCiAgICAvLy8gUmV0dXJuIHRoZSBzdG9yZWQgdmFsdWUuCiAgICAvLy8gQGRldiByZXRyaWV2ZXMgdGhlIHZhbHVlIG9mIHRoZSBzdGF0ZSB2YXJpYWJsZSBgc3RvcmVkRGF0YWAKICAgIC8vLyBAcmV0dXJuIHRoZSBzdG9yZWQgdmFsdWUKICAgIGZ1bmN0aW9uIGdldCgpIHB1YmxpYyB2aWV3IHJldHVybnMgKHVpbnQpIHsKICAgICAgICByZXR1cm4gc3RvcmVkRGF0YTsKICAgIH0KfQ==)

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.16 <0.9.0;

/// @author The Solidity Team
/// @title A simple storage example
contract SimpleStorage {
    uint storedData;

    /// Store `x`.
    /// @param x the new value to store
    /// @dev stores the number in the state variable `storedData`
    function set(uint x) public {
        storedData = x;
    }

    /// Return the stored value.
    /// @dev retrieves the value of the state variable `storedData`
    /// @return the stored value
    function get() public view returns (uint) {
        return storedData;
    }
}

```


It is recommended that Solidity contracts are fully annotated using [NatSpec](https://docs.soliditylang.org/en/v0.8.17/natspec-format.html#natspec) for all public interfaces (everything in the ABI).

Please see the section about [NatSpec](https://docs.soliditylang.org/en/v0.8.17/natspec-format.html#natspec) for a detailed explanation.