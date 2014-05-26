# Item #1 Which js mode are you using

Strict mode (introduced on ES5) disallows some of the more problematic/error-prone features of the full language, syntax is backwards compatible so that enviroments that doesn't implement the strict mode can still execute strict code, evaluating a string literal has no side effects, ES3 evaluates the string and then discards the value, therefore no strict checks are going to be done inside the code.

Works only at beggining of the code/function

"use strict";

function f(x) {
	"use strict";
}

Tip:
- Use iffy functions to keep the mode compatible and isolated from other code
example

(function() {
	"use strict";
	function f() {


	}
})();

### Things to Remember
* Decide which versions of JavaScript your application supports.
* Be sure that any JavaScript features you use are supported by all
environments where your application runs.
* Always test strict code in environments that perform the strict- mode checks.
* Beware of concatenating scripts that differ in their expectations about strict mode.

# Item #2 Understand javascript floating-poing numbers

Javascript handlers integers and float-point as numbers (as doubles, 64-bit numbers)

0.1 * 1.9 // 0.19
-99 + 100; // 1
21 - 12.3; // 8.7
2.5 / 5; // 0.5
21 % 8; // 5

Bitwise arithmetic operators are special (implicit converted to 32-bit integers)

8 | 1; // 9

(8).toString(2); // "1000"
(1).toString(2); // "0001"
parseInt("1001", 2); // 9

00000000000000000000000000001000
00000000000000000000000000000001
=
00000000000000000000000000001001

any bitwise operation means:
convert to Integers -> perform operation -> return value back to floating-point

Tip:

- Limits on floating-point numbers
0.1 + 0.2; // 0.30000000000000004

- Expected the same but floating error
(0.1 + 0.2) + 0.3; // 0.6000000000000001
0.1 + (0.2 + 0.3); // 0.6

- Try to work with integers when accurancy is a requirement
(10 + 20) + 30; // 60
10 + (20 + 30); // 60

### Things to Remember
* JavaScript numbers are double-precision floating-point numbers.
* Integers in JavaScript are just a subset of doubles rather than a
separate datatype.
* Bitwise operators treat numbers as if they were 32-bit signed integers.
* Be aware of limitations of precisions in floating-point arithmetic.

# item #3: Implicit Coercions

