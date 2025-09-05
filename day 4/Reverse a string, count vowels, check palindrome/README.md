# String Operations: Reverse, Count Vowels, Palindrome Check

Let's clarify and practice three useful string operations in Python: **reversing a string**, **counting vowels**, and **checking for a palindrome**.

***

## 1. **Reversing a String**
You can reverse a string in Python in two common ways:

- **Using slicing:**
  ```python
  s = "GeeksforGeeks"
  reversed_s = s[::-1]   # Reads from end to start
  print(reversed_s)       # Output: skeeGrofskeeG
  ```

- **Using `reversed()` and `join()`:**
  ```python
  s = "Hello, World!"
  reversed_s = "".join(reversed(s))
  print(reversed_s)       # Output: !dlroW ,olleH
  ```
**Check:**  Can you explain why slicing with `[::-1]` always reverses the string?

***

## 2. **Counting Vowels**
Count vowels by iterating through the string, using `.lower()` for case-insensitivity:

```python
message = "Hello World from Python"
vowel_count = 0
for char in message:
    if char.lower() in ('a','e','i','o','u'):
        vowel_count += 1
print(f"Number of vowels: {vowel_count}")  # Output: 6
```

Or, using a concise function:
```python
def count_vowels(sentence):
    return sum(sentence.lower().count(vowel) for vowel in 'aeiou')
```
**Try:**  Write your own message and count the vowels in it. Does your function report the expected value?

***

## 3. **Checking for a Palindrome**
A palindrome is a string that reads the same forwards and backwards. The simplest check:

```python
input_string = "Madam"
normalized = input_string.lower()
if normalized == normalized[::-1]:
    print(f"'{input_string}' is a palindrome.")
else:
    print(f"'{input_string}' is not a palindrome.")
```

For a more robust check (using two pointers):
```python
def is_palindrome(word):
    word = word.lower()
    start, end = 0, len(word) - 1
    while start < end:
        if word[start] != word[end]:
            return False
        start += 1
        end -= 1
    return True
```
Try: Test with 'noon', 'racecar', and 'hello'. What do you notice?

***

## **Mini Review**
- **Reversing:** Slicing and built-ins are fast and easy.
- **Counting vowels:** Loop or use functional style.
- **Palindrome check:** Compare normalized string to its reverse, or use two pointers.

[1](https://unstop.com/blog/palindrome-in-python)
[2](https://www.geeksforgeeks.org/python/python-program-check-string-palindrome-not/)
[3](https://www.shiksha.com/online-courses/articles/how-to-check-if-a-python-string-is-a-palindrome/)
[4](https://stackoverflow.com/questions/74252349/checking-for-a-palindrome-using-for-loop-in-python-and-print-output-only-once)
[5](https://ai.thestempedia.com/example/check-palindrome-string-python/)
[6](https://www.sanfoundry.com/python-program-check-string-palindrome/)
[7](https://www.programiz.com/python-programming/examples/palindrome)
[8](https://www.wscubetech.com/resources/python/programs/palindrome)
[9](https://prepinsta.com/python-program/to-check-whether-a-string-is-a-palindrome-or-not/)
