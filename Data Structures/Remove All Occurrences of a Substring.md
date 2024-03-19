## Remove characters from the first string which are present in the second string
- Ref link1 - https://www.geeksforgeeks.org/remove-characters-from-the-first-string-which-are-present-in-the-second-string/
- Ref link2 - https://leetcode.com/problems/remove-all-occurrences-of-a-substring/description/

## Sudo Code
```
1) create array of size ascii code , ie of size 256 with default value zero loop string 2 and change the index corresponding to the char into 1
2) store string 1 to list
3) compare for value 0 and update result_track value accordingly 
4) trim final_string till index result_track
```
## Code
```
# Take array of size equal to 256 the size of all ascii codes
ARR_SIZE = 256

# Below function changes all the ascii value index to 1
def str_to_arr(mask_string):
    # Initialize array with zero of size 256
    arr = [0]*ARR_SIZE
    for c in mask_string:
        arr[ord(c)] = 1
    return arr

# Get the list from string
def str_to_list(string):
    tmp = []
    for c in string:
        tmp.append(c)
    return tmp

# Get string from list
def list_to_str(list):
    str = ""
    return str.join(list)

def removeDirtyChars(string , mask_string):
    arr = str_to_arr(mask_string)
    list_str = str_to_list(string)

    # Index to track the resultant list
    result_track = 0

    # Loop through list of main string
    for idx in range(len(list_str)):
        # get value from list str 1 and store in tmp
        tmp = arr[ord(list_str[idx])]
        if tmp == 0:
            list_str[result_track] = list_str[idx]
            result_track += 1
    # convert list to string
    final_string =  list_to_str(list_str)
    # trim the final_string from 0 to result_track
    return final_string[0:result_track]

mask_string = "mask"
string = "geeksforgeeks"

print("final string : %s " % removeDirtyChars(string, mask_string))
```

## Time Complexity
```
O(m+n) 
```
- Where m is the length of the mask string and n is the length of the input string. 

## Space Complexity
``
Space Complexity: O(n)
``
- Since we took array of size n also we havn't took O(m) because the size of mask array will alway be 256 , it doesnot depends on input size.