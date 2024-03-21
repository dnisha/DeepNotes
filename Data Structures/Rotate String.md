## Rotate String
- Ref link1 - https://www.geeksforgeeks.org/a-program-to-check-if-strings-are-rotations-of-each-other/
- Ref link2 - https://leetcode.com/problems/rotate-string/description/

## Sudo Code 1
```
1) Iterate through string1
2) Slice string1 from index 1 to length , then append index 0 char
3) While iterating keep comparing both the strings
```
## Solution1
```
s1 = "ABCD"
s2 = "CDAB"

l1 = len(s1)
l2 = len(s2)

if l1 == l2:
    for i in range(l1):
        s1 = s1[1:l1]+s1[0]
        if s1 == s2:
            print("Strings are rotations of each other")
            break
else:
    print("Strings are not the rotations of each other")
```
## Time Complexity
```
O(n*n) 
```
## Space Complexity
```
O(1) 
```
- As no extra space is used

## Sudo Code 2
```
1) Create a tem string by concatinating two string
2) Iterate through tmp string
3) If s1 and s2 are rotation of each other then s2 will be the substring of tmp
```
## Solution2
```
s1 = "ABCD"
s2 = "CDAB"

l1 = len(s1)
l2 = len(s2)

tmp = s1+s2

if l1 == l2:
    for i in range(len(tmp)):
        end = i+l1
        if tmp[i:i+l1] == s2:
            print("Strings are rotations of each other")
        elif end == len(tmp):
            print("Strings are not the rotations of each other")
else:
    print("Strings are not the rotations of each other")

```