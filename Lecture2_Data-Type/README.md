# Main_Lecture(2) : Data Type and Variables
## 2.1 What are the Data Types and Variables on C++?

### 2.1.1 Data Types (Basic)
When we make some programs or codes through coding(programming), a concept of `data type` is really important. I'll regard people in this page as those who have experienced any other programming language such as C, Go, Python and so on. So, I won't explain the concept on this page. However, I wanna emphasize the importance of this concept, so that I'll add here one website explaining about a concept of data type: <여기는 자료형에 대한 설명이 나온 웹페이지 주소>  


#### 2.1.1.a Integer Type 
:) `Integer Type` represent integer number such as -2, -1, 0, 1 and 2. However, this type includes a lot of details along ranges able to express, sizes able to do and so on. Typically, `(signed) short (or shor int)`, `unsigned short`, `(signed) int`, `unsigned int`, `(signed) long` and `unsigned long` belong to Integer Type.  


:) Before you learn about Data Type, you should know one thing: 1Byte = 8bit And, 1 bit can be expressed as 0 or 1. Thus, 1Byte is 8bit, so the number of signs, that a computer can express, is 2x2x2x2x2x2x2x2 = 2^8 (=256).  


:) First, I'll explain about differences between `signed` and `unsigned`. Basically, if there is nothing in front of data type, it's a sign of "signend", which is skipped. A sign of `signed` means that it'll express and compute both negative and postive numbers. For example, data type `short` has a memory size of 2 Bytes, which has 2^16 as data length. For negative and positive numbers, this data length should be divided as 2. Then, through the data type "short", we can express `-2^15 ~ 2^15-1` becasue zero belongs to positive number on C++. (Actually,  2^15 = 32768, so it's not that big.) And then, `unsigned` means that it'll express and compute only positive numbers. For example, data type `unsigned short` has a same memory size of 2 Bytes with previous example. Thus, through the data type "unsigned short", we can express `0 ~ 2^16-1`(Actually, 2^16 = 65536, so it's not that big)  


:) Second, I'll explain about the typical(big-subset) kinds of Basic Types. Therefore, this paragraph includes `short`, `int` and `long`. Along these typical kinds, these have each different memory sizes. "Short" has 2 Bytes, "int" does 4 Bytes(or 2 Bytes along the system) and "long" has 4 Bytes. Besides, if you use data type "long", your computer can express and compute data length of maximum 2^32 = 4294967296 (it became really big!!).  


:) Finally, you can think of some combinations between set {signed, unsigned} and set {short, int, long}. In result, you can make total 6 basic data types. Following table is really helpful!!!
<정수형 자료형 표 넣기>

#### 2.1.1.b Floating Point Type
:) Floating Point Type is needed to express real numbers including fraction(decimal). So, for this processing, C++ has chosen three types: `float`, `double` and `long double`. First, I'll let you know about memory sizes of each types. Data type "float" has 4 Bytes, "double" does 8 Bytes and "long double" can do 8, 12 or 16 Bytes. In case of "long double", the memory size depends on the system, which means a kind of gcc or g++ compiler, a version of C++, the system of your computer and so on.  


:) In this part, you don't have to know details about floating point problems or expression methods. So, you need to know about the result. "flaot" has `3.4 x 10^-38 ~ 3.4 x 10^38` as a data length, "double" does `1.7 x 10-308 ~ 1.7 x 10^308` and "long double" can be more detailed than "dboulbe". Following below figure means on C++ how to express the floating point (fraction). Actually, this method is invented to represent lower fraction point numbers using only 4 Bytes.  


:) However, in this floating point type, there is a severe issue: `ACCURACY`. In previous paragraph, I explained that "float" can express `3.4 x 10^-38 ~ 3.4 x 10^38` and "double" can do `1.7 x 10^-308 ~ 1.7 x 10^308`, however the numeric digits for computer to express and the accuracy of number processing, they are not in a same place. I won't explain the principle of floating point accuracy. By the way, you should know about accuracy results. Data type "float" can guarantee computer's computation of the `sixth decimal place` and "double can do about `fifteenth decimal place`.  <정리된 표 넣기>


#### 2.1.1.c Character Type



#### 2.1.1.d Boolean Type
:) Boolean Type is really easy concept. I guess that you've heard that "Light On" is "1" and "Light Off" is "0". Like this, Light on and off are a really appropriate example. Like this, computer is able to, you know, read only "0" and "1". If you've tried `python`, to say "it's not false", you would've written "True" and in contrast case, "False". However, on C++, `1` means `True`. And `0` means `False`. So, if you wanna say 'it's true', then you should write down "1". Like this, boolean type is a data type for you to be able to express "True" or "False".  


:) Also, you can print not "1" but "True" using `boolalpha`. For this example, I'll add it at Appendix.  


### 2.1.2 Variables
#### 2.1.2.a How to declare variables
:) `[THIS SECTION IS ABOUT GENERAL METHOD]`
  1. Variables can't include any space( ) but can inlcude under bar (_)
     > For example, `int Val = 3;` or `int Val_a = 3;`
  2. A name of any variable can't start number.
     > For example, `int Val_1 = 3;`
  3. ^ Generally, programmers make variables include only `alphabet`, `under bar` and `number`.
  4. ^ Generally, programmers add one first letter(lower case) of data type in front of a name of any variable
     > For example, `int iVal = 3;` or `double dVal = 3.1f;`  
     
     
#### 2.1.2.b Declare Constant
:) In programming, `constant` means the fixed number once, which can't be altered by anything such as program.  


  * On C-Style
     > #define PI 3.14  
  
  
  * On C++ Style
     > const float PI = 3.14;  
     > &gt; &nbsp; **Note** : You can apply C-style on C++.
