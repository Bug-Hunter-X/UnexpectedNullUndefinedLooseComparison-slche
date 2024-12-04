# Unexpected Behavior with Loose Comparison of null and undefined

This example demonstrates a common JavaScript pitfall involving loose comparison (==) of null and undefined.  In many cases, developers intend to treat null and undefined similarly, but loose comparison does not reliably achieve this.

## The Problem

The `foo` function attempts to handle null values gracefully.  However, when called with `undefined`, it unexpectedly returns `NaN` instead of a more predictable result (perhaps 0).

## The Solution

To fix this, use strict equality (===) or explicitly check for both null and undefined using OR operator.