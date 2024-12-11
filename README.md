# Tcl == Operator Bug

This repository demonstrates an unexpected behavior of the `==` operator in Tcl when comparing numbers represented as strings.

## Problem

Tcl's `==` operator performs string comparison, not numerical comparison. This can lead to unexpected behavior when comparing numbers that are stored as strings. For example, `"10" == "100"` evaluates to `false` because the strings are lexicographically different, not numerically different. This is different from some other languages like Python, where numerical conversion will be done implicitly when comparing numbers represented as strings. 

The `bug.tcl` file contains a procedure that demonstrates this behavior.

## Solution

The provided solution uses the `expr` command to perform a numerical comparison.  `expr` converts strings to numbers if they represent numerical values before comparison. The `bugSolution.tcl` file shows the corrected procedure using this approach.
