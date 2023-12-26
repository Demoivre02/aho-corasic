# Aho-Corasick String Matching Algorithm

This is a Python implementation of the Aho-Corasick string matching algorithm, a powerful algorithm used for multiple string searches in a given text. It efficiently detects the occurrences of multiple keywords within a larger text.

## Description

The Aho-Corasick algorithm is particularly useful for finding all occurrences of a set of keywords in a text. It preprocesses the set of keywords to create an automaton that can quickly scan through the text, identifying all matches.

## Usage

1. **Initializing the Automaton:**
   ```python
   A = Automaton(["what", "hat", "ver", "er"])
   ```
   Initialize the automaton with a list of keywords.

2. **Searching in Text:**
   ```python
   result = A.search_in("whatever, err ... , wherever")
   ```
   Search for occurrences of keywords in the given text.

3. **Results:**
   The result is a dictionary where keys are the keywords, and values are lists of indices where each keyword occurs in the text.

   ```python
   {'what': [0], 'hat': [1], 'ver': [5, 25], 'er': [6, 10, 22, 26]}
   ```

## Example

```python
from __future__ import annotations
from collections import deque

# ... (rest of the code remains the same)

if __name__ == "__main__":
    import doctest

    doctest.testmod()
```

## How to Use

1. **Initialization:**
   Initialize the `Automaton` class with a list of keywords.

2. **Search:**
   Use the `search_in` method to find occurrences of keywords in a given text.

3. **Results:**
   Obtain results in the form of a dictionary, where each keyword is associated with a list of indices where it occurs in the text.

## Notes

- The algorithm efficiently processes multiple string searches in linear time, making it suitable for applications like text processing, pattern matching, and more.

- The provided example demonstrates the usage of the Aho-Corasick algorithm on a simple set of keywords and a text string.

