# JavaScript Null vs. Undefined Handling Bug

This repository demonstrates a common, yet subtle, bug in JavaScript related to handling `null` and `undefined` values. The initial `foo` function seems to correctly manage nulls, but fails with `undefined`. The solution provides a more robust approach.

## Bug Description
The original `foo` function checks explicitly for `null` values.  However,  it doesn't handle `undefined` inputs, leading to unexpected behavior (NaN) if either input is undefined.

## Solution
The improved `foo` function employs a more comprehensive approach.  It uses loose equality (`==`) to check for both `null` and `undefined`, addressing the original bug.  The use of the OR operator also ensures that we only return 0 if either value is null or undefined, not both simultaneously.