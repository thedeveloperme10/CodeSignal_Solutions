Given the string, check if it is a palindrome.

Example

For inputString = "aabaa", the output should be
checkPalindrome(inputString) = true;
For inputString = "abac", the output should be
checkPalindrome(inputString) = false;
For inputString = "a", the output should be
checkPalindrome(inputString) = true.
Input/Output

[execution time limit] 3 seconds (java)

[input] string inputString

A non-empty string consisting of lowercase characters.

Guaranteed constraints:
1 ≤ inputString.length ≤ 105.

[output] boolean

true if inputString is a palindrome, false otherwise.

### Solution
```
boolean checkPalindrome(String inputString)
{
    String rev="";
    int i;
    for(i=inputString.length()-1;i>=0;i--)
    {
        rev=rev+inputString.charAt(i);
    }
    if(rev.equals(inputString))
    {
        return true;
    }
    return false;
}
```
