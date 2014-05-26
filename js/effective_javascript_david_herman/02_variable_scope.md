# Item #13 Use Immediately Invoked Function Expressions to Create Local Scopes

The immediately invoked function expression or IIFE (pronounced “iffy”) is the for javascript lack of block scope vars.

### Things to Remember
* Understand the difference between binding and assignment.
* Closures capture their outer variables by reference, not by value.
* Use immediately invoked function expressions (IIFEs) to create local scopes.
* Be aware of the cases where wrapping a block in an IIFE can change its behavior.