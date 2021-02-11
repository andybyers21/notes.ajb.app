# Arithmetic in JavaScript
- - - -
**layout**: note
**title**: Arithmetic in JavaScript
**parent**: JavaScript
**grand_parent**: Home
- - - -



**# Arithmetic in JavaScript**
Note: You’ll sometimes see numbers involved in arithmetic referred to as operands.

An ****operand**** – is what operators are applied to. For instance, in the multiplication of 5 * 2 there are two operands: the left operand is 5 and the right operand is 2. These are also known as ****arguments****

An operator^[mathematical symbol [[Operators, Conditionals, Functions & Events]] is ****unary**** if it has a single operand. For example, the unary negation - reverses the sign of a number like `-1` “minus one”

An operator is ****binary**** if it has two operands. The same minus exists in binary form as well.

> See [~here~](~https://www.w3schools.com/js/js_arithmetic.asp~) for details on JavaScript Arithmetic  

**### Remainder `%`**
****The remainder operator `%`, despite its appearance, is not related to percents.**** The result of `a % b` is the remainder of the integer division of `a` by `b`. For example:

`alert( 5 % 2 );`   **// 1, a remainder of 5 divided by 2**
`alert( 8 % 3 );`    **// 2, a remainder of 8 divided by 3**

**### Exponentiation `**`**
The exponentiation operator `a ** b` multiplies `a` by itself `b` times (squared, cubed, etc. etc.. For instance:

`alert( 2 ** 2 );` **// 4  (2 multiplied by itself 2 times)**
`alert( 2 ** 3 );` **// 8  (2 * 2 * 2, 3 times)**
`alert( 2 ** 4 );` **// 16 (2 * 2 * 2 * 2, 4 times)**

This can also work in reverse (for **non-integer** numbers):

`alert( 4 ** (1/2) );` **// 2 (power of 1/2 is the same as a square root)**
`alert( 8 ** (1/3) );` **// 2 (power of 1/3 is the same as a cubic root)**

#tk/code
