Thanks to [Tutorialspoint] (https://www.tutorialspoint.com/java/index.htm)
# String
  - a sequence of chars
  -  `String greeting = "Hello world!"; `
  - functions:
    1. `char charAt(int index)` Returns the character at the specified index.
    2. `int compareTo(Object o)` Compares this String to another Object.
    3. `int compareTo(String anotherString)` Compares two strings lexicographically.
    4. `int compareToIgnoreCase(String str)` Compares two strings lexicographically, ignoring case differences.
    5. `String concat(String str)` Concatenates the specified string to the end of this string.
    6. `boolean contentEquals(StringBuffer sb)` Returns true if and only if this String represents the same sequence of characters as the specified StringBuffer.
      
      - note:  *String* is used to manipulate character strings that cannot be changed (read-only and immutable). *StringBuffer* is used to represent characters that can be modified. 
      
    7. `static String copyValueOf(char[] data)` Returns a String that represents the character sequence in the array specified.
    8. `static String copyValueOf(char[] data, int offset, int count)` Returns a String that represents the character sequence in the array specified.
    9. `boolean endsWith(String suffix)` Tests if this string ends with the specified suffix.
    10. `boolean equals(Object anObject)` Compares this string to the specified object.
    11. `boolean equalsIgnoreCase(String anotherString)` Compares this String to another String, ignoring case considerations.
    12. `byte getBytes()` Encodes this String into a sequence of bytes using the platform's default charset, storing the result into a new byte array.
    13. `byte[] getBytes(String charsetName)` Encodes this String into a sequence of bytes using the named charset, storing the result into a new byte array.
    14. `void getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin)` Copies characters from this string into the destination character array.
    15. `int hashCode()` Returns a hash code for this string.
    16. `int indexOf(int ch)` Returns the index within this string of the first occurrence of the specified character.
    17. `int indexOf(int ch, int fromIndex)` Returns the index within this string of the first occurrence of the specified character, starting the search at the specified index.
    18. `int indexOf(String str)` Returns the index within this string of the first occurrence of the specified substring.
    19. `int indexOf(String str, int fromIndex)` Returns the index within this string of the first occurrence of the specified substring, starting at the specified index.
    20. `String intern()` Returns a canonical representation for the string object.
    21. `int lastIndexOf(int ch)` Returns the index within this string of the last occurrence of the specified character.
    22. `int lastIndexOf(int ch, int fromIndex)` Returns the index within this string of the last occurrence of the specified character, searching backward starting at the specified index.
    23. `int lastIndexOf(String str)` Returns the index within this string of the rightmost occurrence of the specified substring.
    24. `int lastIndexOf(String str, int fromIndex)` Returns the index within this string of the last occurrence of the specified substring, searching backward starting at the specified index.
    25. `int length()` Returns the length of this string.
    26. `boolean matches(String regex)` Tells whether or not this string matches the given regular expression.
    27. `boolean regionMatches(boolean ignoreCase, int toffset, String other, int ooffset, int len)` Tests if two string regions are equal.
    28. `boolean regionMatches(int toffset, String other, int ooffset, int len)` Tests if two string regions are equal.
    29. `String replace(char oldChar, char newChar)` Returns a new string resulting from replacing all occurrences of oldChar in this string with newChar.
    30. `String replaceAll(String regex, String replacement` Replaces each substring of this string that matches the given regular expression with the given replacement.
    31. `String replaceFirst(String regex, String replacement)` Replaces the first substring of this string that matches the given regular expression with the given replacement.
    32. `String[] split(String regex)` Splits this string around matches of the given regular expression.
    33. `String[] split(String regex, int limit)` Splits this string around matches of the given regular expression.
    34.  `boolean startsWith(String prefix)` Tests if this string starts with the specified prefix.
    35. `boolean startsWith(String prefix, int toffset)` Tests if this string starts with the specified prefix beginning a specified index.
    36. `CharSequence subSequence(int beginIndex, int endIndex)` Returns a new character sequence that is a subsequence of this sequence.
    37. `String substring(int beginIndex)` Returns a new string that is a substring of this string.
    38. `String substring(int beginIndex, int endIndex)` Returns a new string that is a substring of this string.
    39. `char[] toCharArray()` Converts this string to a new character array.
    40. `String toLowerCase()` Converts all of the characters in this String to lower case using the rules of the default locale.
    41.  `String toLowerCase(Locale locale)` Converts all of the characters in this String to lower case using the rules of the given Locale.
    42. `String toString()` This object (which is already a string!) is itself returned.
    43. `String toUpperCase()` Converts all of the characters in this String to upper case using the rules of the default locale.
    44. `String toUpperCase(Locale locale)` Converts all of the characters in this String to upper case using the rules of the given Locale.
    45. `String trim()` Returns a copy of the string, with leading and trailing whitespace omitted.
    46. `static String valueOf(primitive data type x)` Returns the string representation of the passed data type argument.
    
# Array

Declaring an array variable, creating an array, and assigning the reference of the array to the variable can be combined in one statement, as shown below −

`dataType[] arrayRefVar = new dataType[arraySize];`

alternative way - `dataType[] arrayRefVar = {value0, value1, ..., valuek};`

Functions:

1 	

`public static int binarySearch(Object[] a, Object key)`

Searches the specified array of Object ( Byte, Int , double, etc.) for the specified value using the binary search algorithm. The array must be sorted prior to making this call. This returns index of the search key, if it is contained in the list; otherwise, it returns ( – (insertion point + 1)).

2 	

`public static boolean equals(long[] a, long[] a2)`

Returns true if the two specified arrays of longs are equal to one another. Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. This returns true if the two arrays are equal. Same method could be used by all other primitive data types (Byte, short, Int, etc.)

3 	

`public static void fill(int[] a, int val)`

Assigns the specified int value to each element of the specified array of ints. The same method could be used by all other primitive data types (Byte, short, Int, etc.)

4 	

`public static void sort(Object[] a)`

Sorts the specified array of objects into an ascending order, according to the natural ordering of its elements. The same method could be used by all other primitive data types ( Byte, short, Int, etc.)

**Date and Time**

*Date* class available in *java.util*

1 	

`Date( )`

This constructor initializes the object with the current date and time.

2 	

`Date(long millisec)`

This constructor accepts an argument that equals the number of milliseconds that have elapsed since midnight, January 1, 1970.

Functions:

1 	

`boolean after(Date date)`

Returns true if the invoking Date object contains a date that is later than the one specified by date, otherwise, it returns false.

2 	

`boolean before(Date date)`

Returns true if the invoking Date object contains a date that is earlier than the one specified by date, otherwise, it returns false.

3 	

`Object clone( )`

Duplicates the invoking Date object.

4 	

`int compareTo(Date date)`

Compares the value of the invoking object with that of date. Returns 0 if the values are equal. Returns a negative value if the invoking object is earlier than date. Returns a positive value if the invoking object is later than date.

5 	

`int compareTo(Object obj)`

Operates identically to compareTo(Date) if obj is of class Date. Otherwise, it throws a ClassCastException.

6 	

`boolean equals(Object date)`

Returns true if the invoking Date object contains the same time and date as the one specified by date, otherwise, it returns false.

7 	

`long getTime( )`

Returns the number of milliseconds that have elapsed since January 1, 1970.

8 	

`int hashCode( )`

Returns a hash code for the invoking object.

9 	

`void setTime(long time)`

Sets the time and date as specified by time, which represents an elapsed time in milliseconds from midnight, January 1, 1970.

10 	

`String toString( )`

Converts the invoking Date object into a string and returns the result.

**Date Formatting Using SimpleDateFormat**

Example:

```
mport java.util.*;
import java.text.*;

public class DateDemo {

   public static void main(String args[]) {
      Date dNow = new Date( );
      SimpleDateFormat ft = 
      new SimpleDateFormat ("E yyyy.MM.dd 'at' hh:mm:ss a zzz");

      System.out.println("Current Date: " + ft.format(dNow));
   }
}
```
**Simple DateFormat Format Codes**

**Character|Description|Example**
-----------|-----------|----------
G| 	          Era designator 	          |AD
y| 	          Year in four digits 	    |2001
M| 	          Month in year 	          |July or 07
d| 	          Day in month 	            |10
h| 	          Hour in A.M./P.M.(1~12)   |12
H| 	          Hour in day (0~23) 	      |22
m| 	          Minute in hour 	          |30
s| 	          Second in minute 	        |55
S|  	        Millisecond 	            |234
E| 	          Day in week 	            |Tuesday
D| 	          Day in year 	            |360
F| 	          Day of week in month 	    |2 (second Wed. in July)
w| 	          Week in year 	            |40
W| 	          Week in month 	          |1
a| 	          A.M./P.M. marker 	        |PM
k| 	          Hour in day (1~24) 	      |24
K| 	          Hour in A.M./P.M. (0~11) 	|10
z|	          Time zone 	              |Eastern Standard Time
'| 	          Escape for text 	        |Delimiter
"| 	          Single quote 	            |`

**Java code -> Javac -> Bytecode -> Java VM -> Machine code**

**Compile: `javac nameOfYourFile.java` in terminal**

**Execute: `java nameOfYourFile` in terminal**

