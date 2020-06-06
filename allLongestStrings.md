Given an array of strings, return another array containing all of its longest strings.

Example

For inputArray = ["aba", "aa", "ad", "vcd", "aba"], the output should be
allLongestStrings(inputArray) = ["aba", "vcd", "aba"].

Input/Output

[execution time limit] 3 seconds (java)

[input] array.string inputArray

A non-empty array.

Guaranteed constraints:
1 ≤ inputArray.length ≤ 10,
1 ≤ inputArray[i].length ≤ 10.

[output] array.string

Array of the longest strings, stored in the same order as in the inputArray.

### Solution
```
String[] allLongestStrings(String[] inputArray)
{
    List<String>s=new ArrayList<String>();
    int maxLength=0;
    int i;
    for(i=0;i<inputArray.length;i++)
    {
        String g=inputArray[i];
        if(maxLength<g.length())
        {
            maxLength=g.length();
        }
    }
    for(i=0;i<inputArray.length;i++)
    {
        if(inputArray[i].length()==maxLength)
        {
            s.add(inputArray[i]);
        }
    }
    String[]p=new String[s.size()];
    for (i =0; i < s.size(); i++)
    {
    p[i] = s.get(i);
    }
    return p;
}
```
