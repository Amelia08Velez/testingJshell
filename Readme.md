# Repository for testing jshell
jshell> int n = 68;  
n ==> 68  

jshell> byte b = 127;  
b ==> 127  

jshell> char c = 'B';  
c ==> 'B'  

jshell> b = n;  
|  Error:
|  incompatible types: possible lossy conversion from int to byte
|  b = n;  
|      ^

jshell> C = n;  
|  Error:
|  cannot find symbol  
|    symbol:   variable C  
|  C = n;  
|  ^
### after error fixed  
int n = 68;  
byte b = 127;  
char c = 'B';  
b = (byte)n;  
c = (char)n;  
c ==> 'D'  
b ==> 68  

