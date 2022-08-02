object  
method  
class  
JVM-java virtual machine-translating byte-code to the machine language (through interpreter or JIT compiler)    
  program.java ----compiling----program.class  

initialize a variable：   
  int firstnumber=1, secondnumber, lastnumber=3;  
  
primitive types    
![image](https://user-images.githubusercontent.com/109948257/182167136-08b2b214-cfa3-4d1d-9ce1-e20ad3228b42.png)

you can assign a value of any type in the following list to a variable of any type further down the list:  
  byte-->short-->int-->long-->float-->double  
    int intvar;  
    intvar=22;  
    double doublevar;  
    doublevar=intvar;  
  if not following the list, then need type cast:  
    int n;  
    int m;  
    double ans=n/(double)m;  
char-single quote  
string-double quote  

Variable Op(operator) = Expression --> Variable=Variable Op (Expression)  
  ![image](https://user-images.githubusercontent.com/109948257/182175498-b914ee41-690f-4ab4-99e7-9748019b715d.png)
incrementand decrement operator:  
  ++: increase the variable vale by one  
    n++:if the ++ is after the variable, the incrementing is done after the value is returned  
      int n=2;    
      int aftern=2*(n++);  
      return aftern 4  
      return n 3  
    ++n: if the ++ is before the variable, the incrementing is down bfore the value is returned  
      int n=2;  
      int beforen=2*(++n);  
      return beforen 6  
      return n 3    

integer and floating point division:    
  int: not rounded, the decimal part is discarded: 10/3-->3    
      % gives the remainder:14%3-->2    
      
String methods:  
  int string.length()  
  boolean  string.equals(other_string)  
  boolean string.equalsIgnoreCase(other_string) -- Upper and lower cases are treated as the same.  
  string string.toLowerCase()  
  string string.toUpperCase()  
  string string.trim() -- Remove the leading and trailing white spaces.  
  char string.charAt(position)
  string string.substring(start) -- Extract from the start to the end, the start is included  
  string string.substring(start,end) -- start is included, but end is not included  
  int string.indexOf(full_string) -- Return the index(position) of the first occurence  
    int string.indexOf(full_string,start)  
  int string.lastIndexOf(full_string)  
  int string.compareTo(other_string) -- Upper>lower  
  int string.compareToIgnoreCase(other_string)  

escape sequence (this is a single character,even though spelled in two symbols)  
  backslash  \\  
  single quote  \'  
  double quote  \"  
  new line  \n  
  carriage return  \r （go to the beginning of the current line） 
  tab  \t  
  
line comments: //  (only for the code writer)  
block comments: /*comments*/ (become part of the code)  




























  
  
  

  
  
