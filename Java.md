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
  int-->float, long-->float, and long-->double can result in inexact conversions   
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
  If an expression uses a variable, say x, more than once, and one has an increment or decrement, the expression becomes 
  confusing for the reader, even though it isn't to the compiler   

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

System.out.println     
System.out is an object   
println is a method  
System.out.printf("%6.2f", price)  
  The format specifier %6.2f says to output a floating-point number in a field (number of spaces) of width 6 (room for six   characters) and to show exactly two  digits after the decimal point.    
  dose not advance the output to the next line   
  ![image](https://user-images.githubusercontent.com/109948257/182512566-ff346d79-8db8-459d-bd14-241e76d19339.png)   
  !d here means decimal not double!
  When the value output does not fill the field width specified, blanks are added in front of the value output. The output   is then said to be right justified. If you add a hyphen after the %, any extra blank space is placed after the value       output, and the output is said to be left justified.   
  ![image](https://user-images.githubusercontent.com/109948257/182515749-321e7ff4-6b70-410f-bd2d-e68ba098489a.png)  
  ![image](https://user-images.githubusercontent.com/109948257/182515796-f2916a32-0083-45e5-af8a-e143edc0d715.png)  
  %n is equal to \n here   

NumberFormat moneyFormatter = NumberFormat.getCurrencyInstance();       
![image](https://user-images.githubusercontent.com/109948257/182516848-9eac7d61-60a4-4445-9195-0292db531361.png)    
![image](https://user-images.githubusercontent.com/109948257/182516864-b6091094-e65c-415b-ab40-0ebb0e847bf1.png)   

import packages and classes   
packages:   
  java.text  
  java.util  
  
![image](https://user-images.githubusercontent.com/109948257/182853875-fc37a3df-b592-4264-a567-54e0101fd70a.png)   
If the above program is run from the command line as follows:  
java YourProgram Do Be Do   
the output produced by the program will be   
Be Do Be   
Each argument is treated as a string. But you can convert the string input to int or a double, for example using:   
int argument = Integer.parseInt(args[0]);   
double arg0 = Double.parseDouble(args[0]);   

Scanner class   
import java.util.Scanner   
Scanner object_name = new Scanner(System.in); //receiving data entered from keyboard   
  object_name usually would be keyboard   
int number_putin = objective_name.nextInt(); //reads one int value typed on the keyboard    
  The numbers typed in must be separated by whitespace, such as one or more spaces, a line break, or other whitespace.    
double d = object_name.nextDouble(); //reads one double   
String word = object_name.next(); //reads one word       
String line = object_name.nextLine();   
![image](https://user-images.githubusercontent.com/109948257/182758840-7dbfc467-077f-467e-bdbe-d26dcc83fbe9.png)    
![image](https://user-images.githubusercontent.com/109948257/182759159-ac78db11-7b74-4dd4-880a-0b2d58fe3105.png)    

File input     
import java.io.FileInputStream;     
import java.io.FileNotFoundException;          
![image](https://user-images.githubusercontent.com/109948257/183363209-8406af2b-e94e-4602-b8fe-4c94b987f32e.png)    

Boolean    
() in if-else expression, a Boolean must be enclosed in parenthese  
{} to execute more than one statement each in an if-else statement  
  placement of braces  
  indenting   
multiway if-else statement; Boolean expressions are evaluated in order until a true Boolean is found   
switch statement is the only other kind of Java statement tha timplements multiway branches   
  the controlling expressions for a switch a statement must be: char, int, short, byte, String   
![image](https://user-images.githubusercontent.com/109948257/183368534-0edbc2bd-bc1a-49cc-ae87-626648d847d5.png)   
conditional operator (ernary operator, arithmetic if)   
  (n1>n2) ? n1 : n2 -- if Boolean is true, then the first expression n1 will be returned, otherwise n2    
and operator: &&    
or operator: ||   
negate any Boolean expression operator: !   
  ! (savings < debt) -- savings is not less than debt   
   
when testing strings for equality, do not use == :  (== used for primitive types)   
String.equals(Other_String);  
String.equalsIgnoreCase(Other_String);   
String.compareTo(Other-String): lexicographic oedering (all upper letters come before lowercase letters)   
  compareToIgnoreCase()
  returns a negative number if s1 comes before s2 in lexicographic ordering   
  returns zero if the two strings are equal   
  returns a positive number if s2 comes before s1    

loops statements:   
while    
  a while loop can iterate its body zero times  
  Boolean is checked before the loop body is executed
do-while   
  a do-while loop always iterates its body at least one time   
  Boolean is checked after the loop body is executed first   
![image](https://user-images.githubusercontent.com/109948257/183795180-d110086f-eb78-45bf-a50c-e99e6e9cd59e.png)    
for (initialization; Boolean_Expression; update)    
    Body   
a for loop can contain multiple initialization by using commas    
to label a loop: "identifier :"   
In a loop: break, countine, System.exit()   

debugging    
loop bugs   
  unitended infinite loops    
  off-by-one: "==" is not reliable for floating-point numbers for they are approximate quantities, 
  and "==" tests for exact match    
general dubugging techniques












  


 
  



  



























  
  
  

  
  
