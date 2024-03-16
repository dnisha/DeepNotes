## Excel Sheet Column Title
- Ref link1 - https://leetcode.com/problems/excel-sheet-column-title/description/
- Ref link2 - https://www.geeksforgeeks.org/find-excel-column-name-given-number/
## Sudo Code
```
while col > 0
    new_col = (col-1)
    tmp_string = new_col % 26 + 'A'
    col = new_col / 26

reverse(tmp_string)
```
## Code
```
col = 701
result = ""
while col > 0:
    new_number = col - 1
    modulo = int(new_number%26)
    result = result+chr(modulo+65)
    col = int(new_number/26)

print(result[-1::-1])

# Solution
# Substract the number by 1 then add with 'A' Mod the new_number by 26 since there are 26 alphabet then divide the number by 26
# Reverse the string
```
## Time Complexity
``
Time Complexity: O(col)
``
- Since the loop iterates until col becomes 0, the number of iterations depends on the magnitude of col.

## Space Complexity
``
Space Complexity: O(col)
``
- The size of tmp grows as the loop progresses, but it never exceeds the value of col.