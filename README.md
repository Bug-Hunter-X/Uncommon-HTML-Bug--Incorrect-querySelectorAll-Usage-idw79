# Uncommon HTML Bug: Incorrect querySelectorAll Usage

This repository demonstrates a subtle bug related to the `querySelectorAll` method in JavaScript within an HTML context.
The bug occurs due to an incorrect usage of `querySelectorAll` and an attempt to use array methods on the returned NodeList, which is not an array.

## Bug Description
The primary issue lies in using `querySelectorAll('div[id=myDiv]')`  with the intention of selecting an element by its ID. While functionally selecting the element, the NodeList returned doesn't directly support the `forEach` method. This results in a runtime error.

## Solution
The solution involves converting the NodeList to an array before using array methods like `forEach`. This can be accomplished efficiently using `Array.from()`.