# Main_Lecture(2) : Data Type and Variables
## 2.1 What are the Data Types and Variables on C++?

### 2.1.1 Data Types (Basic)
When we make some programs or codes through coding(programming), a concept of `data type` is really important. I'll regard people in this page as those who have experienced any other programming language such as C, Go, Python and so on. So, I'll explain the concept on this page. However, I wanna emphasize the importance of this concept, so that I'll add here one website explaining about a concept of data type: <여기는 자료형에 대한 설명이 나온 웹페이지 주소>  


#### 2.1.1.a Integer Type 
:) `Integer Type` represent integer number such as -2, -1, 0, 1 and 2. However, this type includes a lot of details along ranges able to express, sizes able to do and so on. Typically, `(signed) short (or shor int)`, `unsigned short`, `(signed) int`, `unsigned int`, `(signed) long` and `unsigned long` belong to Integer Type.  


:) Before you learn about Data Type, you should know one thing: 1Byte = 8bit And, 1 bit can be expressed as 0 or 1. Thus, 1Byte is 8bit, so the number of signs, that a computer can express, is 2x2x2x2x2x2x2x2 = 2^8 (=256).  


:) First, I'll explain about differences between `signed` and `unsigned`. Basically, if there is nothing in front of data type, it's a sign of "signend", which is skipped. A sign of `signed` means that it'll express and compute both negative and postive numbers. For example, data type `short` has a memory size of 2 Bytes, which has 2^16 as data length. For negative and positive numbers, this data length should be divided as 2. Then, through the data type "short", we can express `-2^15 ~ 2^15-1` becasue zero belongs to positive number on C++. (Actually,  2^15 = 32768, so it's not that big.) And then, `unsigned` means that it'll express and compute only positive numbers. For example, data type `unsigned short` has a same memory size of 2 Bytes with previous example. Thus, through the data type "unsigned short", we can express `0 ~ 2^16-1`(Actually, 2^16 = 65536, so it's not that big)  


:) Second, I'll explain about the typical(big-subset) kinds of Basic Types. Therefore, this paragraph includes `short`, `int` and `long`. Along these typical kinds, these have each different memory sizes. "Short" has 2 Bytes, "int" does 4 Bytes(or 2 Bytes along the system) and "long" has 4 Bytes. Besides, if you use data type "long", your computer can express and compute data length of maximum 2^32 = 4294967296 (it became really big!!).  


:) Finally, you can think of some combinations between set {signed, unsigned} and set {short, int, long}. In result, you can make total 6 basic data types. Following table is really helpful!!!
<정수형 자료형 표 넣기>

#### 2.1.1.b Floating Point Type
:) Floating Point Type is needed to express real numbers including fraction. So, 


#### 2.1.1.c Character Type



#### 2.1.1.d Boolean Type