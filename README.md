# Solidity Bug: Incorrect Variable Name in balanceOf Function

This repository demonstrates a common error in Solidity smart contracts: using an incorrect variable name.  The `balanceOf` function incorrectly references `balances` instead of `balanceOf`, leading to incorrect balance retrievals.

## Bug Description

The `balanceOf` function attempts to return the balance of an address. However, it uses the variable `balances` which is undefined, leading to a 0 balance being returned in all cases.  The correct variable to use is `balanceOf`, a mapping that stores the balance for each address.

## Solution

The solution involves simply correcting the variable name within the `balanceOf` function to use the correctly declared mapping variable.