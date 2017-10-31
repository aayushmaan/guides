---
title: Naive String Pattern Searching Algorithm
---
## Naive String Pattern Searching Algorithm

We encounter string searching almost regularly while searching words in a text document or in the browser and many other applications.

The most basic solution to string matching is to slide the pattern over the text and wait for a match. If a match is found, increment the pattern by 1 and continue matching.

Time complexity: 

> The best case occurs when the first character of the pattern is not present in text at all.

str[]  = "AABCCDEAE"
pat[] = "FAA"

Time complexity in best case: O(n).

> The worst case of Naive Pattern Searching occurs in following scenarios.
  > When all characters of the text and pattern are same.

  str[] = "AAAAAAAAA"
  pat[] = "AAAAA".

  > Worst case also occurs when only the last character is different.

  txt[] = "AAAAAAAAAAAAAAAAAB"
  pat[] = "AAAAB"

Time complexity in worst case: O(m*(n-m+1))

## Pseudo Code
N - size of string
M - size of pattern

```C
for loop i from 0 to N-M //N-M as we dont need to check further is the first character doesn't match
{
        // For current index i, check for pattern match
        for loop j from 0 to M-1
            if str[i+j] != pattern[j]
                break
 
        if j == M  // if pat[0...M-1] = txt[i, i+1, ...i+M-1]
           print "Pattern found at index i"
}
```


