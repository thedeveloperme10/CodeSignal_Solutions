Given a rectangular matrix of characters, add a border of asterisks(*) to it.

Example

For

picture = ["abc",
           "ded"]
the output should be

addBorder(picture) = ["^^^^^",
                      "^abc^",
                      "^ded^",
                      "^^^^^"]
Input/Output

[execution time limit] 3 seconds (java)

[input] array.string picture

A non-empty array of non-empty equal-length strings.

Guaranteed constraints:
1 ≤ picture.length ≤ 100,
1 ≤ picture[i].length ≤ 100.

[output] array.string

The same matrix of characters, framed with a border of asterisks of width 1.

### Solution
```
String[] addBorder(String[] picture) {
String[] framedPicture = new String[picture.length + 2];

    for(int i = 0 ; i < picture.length ; i++) {
        framedPicture[i+1] = '^' + picture[i] + '^';
    }
    
    framedPicture[0] = framedPicture[picture.length + 1] = framedPicture[1].replaceAll(".","^");
    
    return framedPicture;
}
```
