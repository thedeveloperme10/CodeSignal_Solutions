Ticket numbers usually consist of an even number of digits. A ticket number is considered lucky if the sum of the first half of the digits is equal to the sum of the second half.

Given a ticket number n, determine if it's lucky or not.

Example

For n = 1230, the output should be
isLucky(n) = true;
For n = 239017, the output should be
isLucky(n) = false.
Input/Output

[execution time limit] 3 seconds (java)

[input] integer n

A ticket number represented as a positive integer with an even number of digits.

Guaranteed constraints:
10 ≤ n < 106.

[output] boolean

true if n is a lucky ticket number, false otherwise.

### Solution
```
boolean isLucky(int n)
{
    String a=Integer.toString(n);
    int len=a.length();
    String b="";
    String x="";
    for(int i=0;i<len/2;i++)
    {
        b=b+a.charAt(i);
    }
    for(int i=len/2;i<len;i++)
    {
        x=x+a.charAt(i);
    }
    int c=Integer.parseInt(b);
    int d=Integer.parseInt(x);
    int res=c%9;
    int res1=d%9;
    if(res==res1)
    {
        return true;
    }
    return false;
}
```
