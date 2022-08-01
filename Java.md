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

integer and floating point division:    
  int: not rounded, the decimal part is discarded: 10/3-->3    
      % gives the remainder:14%3-->2    
  
  
