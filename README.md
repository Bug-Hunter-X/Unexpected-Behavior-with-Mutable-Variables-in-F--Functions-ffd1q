# F# Mutable Variable Swap Bug

This repository demonstrates a common pitfall when working with mutable variables in F# functions: changes made to mutable variables within a function do not affect the original variables passed as arguments.  This is due to F#'s pass-by-value nature. The example showcases how to correctly swap mutable variables by returning the updated values or using references.

## Bug Description
The `swap` function attempts to swap the values of two mutable variables. However, because F# passes variables by value, the function only modifies local copies of the variables. The original variables remain unchanged.

## Solution
To correctly swap the values, you must either return the swapped values as a tuple or use references.