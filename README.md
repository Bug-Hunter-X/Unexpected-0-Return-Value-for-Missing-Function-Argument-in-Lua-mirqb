# Lua Function Argument Handling Bug

This repository demonstrates an uncommon error in Lua where a function unexpectedly returns 0 when called without arguments, instead of throwing an error or returning nil.

## Bug Description
The `foo` function is defined to return `x + 1` when the parameter `x` is passed, and nil when `x` is nil.
However, when called without arguments the function returns 0 instead of handling it as the nil case.

## Solution
The solution involves explicitly checking if the number of arguments is less than 1 which is a proper error handling for this case, or checking explicitly for `nil` for each argument. This ensures that the function handles the case of missing arguments correctly.  This change improves the robustness and predictability of the function.