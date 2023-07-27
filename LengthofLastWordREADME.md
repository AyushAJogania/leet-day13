# leet-day13

# Length of Last Word

## Problem Description

Given a string `s` consisting of words and spaces, you need to return the length of the last word in the string.

A word is a maximal substring consisting of non-space characters only.

## Examples

### Example 1:

Input: `s = "Hello World"`
Output: `5`
Explanation: The last word is "World" with length 5.

### Example 2:

Input: `s = "   fly me   to   the moon  "`
Output: `4`
Explanation: The last word is "moon" with length 4.

### Example 3:

Input: `s = "luffy is still joyboy"`
Output: `6`
Explanation: The last word is "joyboy" with length 6.

## Constraints

- 1 <= `s.length` <= 10^4
- `s` consists of only English letters and spaces ' '.
- There will be at least one word in `s`.

## Approach and Code

To solve this problem, we can iterate through the string in reverse and find the last word's length. We start from the end and skip any trailing spaces. Once we encounter a non-space character, we start counting the characters until we reach the next space or the beginning of the string. The code for this approach is implemented in C++ as follows:


## Complexity Analysis

The time complexity of this approach is O(n), where n is the length of the input string `s`. The space complexity is O(1) since we use constant extra space for variables.
