# 4 Lecture(4) : Flow Control (1)
## 4.1 Before You Start
:) In Lecture (2), I said like this **Whenever the programming lines end, you must write ;(semi-colon). At this time, you should be able to distinguish `code line` and `code block`**. Before the beginning, I'll explain this. 
  * **Code Block** can inclue `Code Block` and `Code Line`
  * **Code Line** belong to only `Code Block`  
  
:) Then, how can we recognize "Code Block" and "Code Line"? `Code Block` is distinguished by mid-bracket {} on C/C++. If there is {}, the parts are called as "Code Block". Then "Code Line"? In one code block, `everything` except for any code blocks: this is `code line`. Take a look at the following example.

  * **Problem 4-1 :** Now, you wanna make a program to calculate a circumference with a radius if you enter a radius. Also, unless you enter number -1, you wanna let your program continuously be executing. Then, why don't you make a code that has these functions? And how could you make this program?

```
// Example 4-1
#include <iostream>
//#include <typeinfo> // if you use Dev-C++, Activate this line

#define PI 3.14
using namespace std;
int main()
{
    int iValue(2);
    double circum{0}; // Initialization of variables.
    for (;;) {
        cout << "Enter the radius(enter -1 for close): "
        cin >> iValue;
        if (iValue == -1)
        {
          break;
        }
        circum = iValue * 2 * PI;
        cout << "circumference with a radius of " << iValue << " : ";
        cout << circum << "(" << typeid(circum).name() << ")" << endl;
    }
    return 0;
}
```
:) I recommend to analyze this code. Okay, if you watch the code, you can see that **Code Block** `int main() { }` include **Code Block** `for(;;) { }`, which does **Code Block** `if( ~ ) { }`. Then, why don't you exclude these things? After that, you can see some lines from these codes, by the way they have something common. That's `;` at the end of the lines. Right, on C++, if `Code Line` ends, you should write the semi-colon at the end of every code lines.  

:) You can get something really valuable. **`새로 추가하기`**

  * using namespace std; 에 대해 설명하기
  * for 문에 대해 설명하기
  * typeid( ).name()에 대해 설명하기
  * 비트 연산자 << >> 에 대해 


## 4.2 Conditional Statement
### 4.2.1 if STATEMENT
:) **`if statement`** is really important and typical C++ grammar. It's better to watch the grammar structure once than to explain it one-hundred time in texts. Let's take a look!
```
**Structure**
if ( <Condition 1> )
{
    <Statement 1>
}
else if ( <Condition 2> )
{
    <Statement 2>
}
else if ( <Condition 3> )
{
    <Statement 3>
}

...

else if ( <Condition N> )
{
    <Statement N>
}
else
{
    <Statement N+1>
}
```

:) Like this example, you can write `if` and `else` only once and `else if` multiple times(almost infinite). Also, `if` and `if else` need "Condition". Then, let's watch a real example.  

  * **Problem 4-2 :** This time, you have to make a program that enables to estimate the grade along the scores. Your program says that it wants to decide "A" over 80 points, "B" from 60 points to 80 points, "C" from 40 points to 60 points and "F" under 40 points. Then how can you make this program? Write down your own code!

```
// Example 4-2
#include <iostream>

using namespace std;

int main()
{
    float fScore{0};
    
    cout << "Enter your score: ";
    cin >> fScore;
    
    cout << "Your Score: " << fScore << endl;
    
    if (fScore > 80)
    {
        cout << "Your grade is A";
    }
    else if (fScore > 60)
    {
        cout << "Your grade is B";
    }
    else if (fScore > 40)
    {
        cout << "Your grade is C";
    }
    else
    {
        cout << "You didn't pass this class: F" << endl;
    }
    
}
```

:) How about it? Is it alright? Could you understand its structure and appliciation? Also, you can simplify the codes like the following code.  
```
// Example 4-2 
#include <iostream>

using namespace std;

int main()
{
    float fScore{0};
    
    cout << "Enter your score: ";
    cin >> fScore;
    
    cout << "Your Score: " << fScore << endl;
    
    if (fScore > 80) cout << "Your grade is A";
    else if (fScore > 60) cout << "Your grade is B";
    else if (fScore > 40) cout << "Your grade is C";
    else cout << "You didn't pass this class: F" << endl;
}
```
:) However, this simplification could be performed when the `code line`s in the **`if` code blocks** is really simple. Then, go learn another "conditional statement"!  


### 4.2.2 Ternary Operator
:) Indeed, you don't have to know this grammar in detail. Because there are few people who use this structure. However, the reason why you need to know this is related to communications with other people(programmers). Okay, then let's see the structure first.
```
( <Condition> ) ? <True_Statement> : <False_Statement>;
```
 > **NOTE** : True_Statement means that the statement will be executed when the condition is true, while False_Statement means that the statement will be executed when the condition is false.  

  * **Problem 4-3 :** Okay, you've learned the structure so far. Then, watch one example and learn the logic. And anticipate the result of this code.

```
//Example 4-3
#include <iostream>

using namespace std;

int main()
{
    int max{0};
    int x{10}, y{20};
    
    max = (x > y) ? x : y;
    cout << max;
    
    return 0;
}
```

:) Yes, it's quite simple comparing with `if statement`. However, it has also weakness when you make some more complicated program. So, in my case, I don't have a good memory so that I don't use this `Ternary Operator`. Even though I don't use it, you can use it if you feel comfortable when you use ternary operator. Then, let' solve really easy problem together!

  * **Problem 4-4 :** Today, you entered a company. So, as an intern, you should treat some documents. By the way, the documents have been related to numbers. So, you've thought that you should make a program to calculate the numbers easily. A performance that you should do is only dividing some numbers after any number being entered(Actually, this logic will be connected to calculating something on a file such as txt, csv and etc. after including the file). So, you have to make a program like this: After you input two numbers, your program will print `Wrong Input` when second entered number is zero or negative. And, if the numbers are not wrong, your progrma will calculate them normally. Use "-1", which means `wrong input`. Hint: A fraction is not defined when a denominator is zero. [Example Answer is below, you can see the example results at `4.4`]  

```
//Example 4-4
#include <iostream>

using namespace std;

int main()
{
    float fNum1{1}, fNum2{1};
    float fResult{-1};
    
    cout << "Enter a first number: ";
    cin >> fNum1;
    
    cout << "Enter a second number: ";
    cin >> fNum2;
    
    fResult = ( fNum2 != 0) ? fNum1/iNum2 : -1;
    cout << "Result : " << fResult << endl;
    
    return 0;
}
```
:) Did you solve this well? Then, I guess that you're already a master of "if statement"!!! Cool! Then, let's learn about next subject: `switch`!!

### 4.2.3 switch
:) In fact, you'll utilize `switch` much more than `ternary operator`. Because this structure makes your codes more simple in a lot of cases. However, even though some people say "This is not good for the codes on C++", I think that if you apply this well, its power will be highly great. So, I suggest that you need to use this in appropriate situations. Then, watch the structure!

```
switch (<variables>)
{
    case <constant 1>:
        <statements 1>
        break;
        
    ...
        
    case <constant N>:
        <statements N>
        break;
    default:
        <statements N+1>
}
```
:) When you use this `switch`, you should write `break` (except for default) at the end of every case. If you don't write it down, your program will execute all the codes until "break" is found. So, what you express "break" is really important for `switch`. Then, think about the following problem.  

  * **Problem 4-5 :** Watch the one example, and think about the result. When you enter 2, anticipate the result. Simultaneously, if you think there are any parts need to be modified, modify the codes and execute the code again.  

```
//Example 4-5
#include <iostream>

using namespace std;

int main()
{
    int iNum;
    
    cout << "Which product do you want to know information about?" << endl;
    cout << "1. Airpods\t2. iPhone\t3. Galaxy Series\t4. Buds Plus" << endl;
    cout << "Enter your choice: ";
    cin >> iNum;
    
    switch (iNum)
    {
        case 1:
            cout << "This section is about 'Airpods'." << endl;
            break;
        case 2:
            cout << "This section is about 'iPhone'." << endl;
        
        case 3:
            cout << "This section is about 'Galaxy Series'." << endl;
        
        case 4:
            cout << "This section is about 'Buds Plus'." << endl;
            break;
        default:
            cout << "You've entered a wrong number. Could you enter a number again?" << endl;
    }
    
    return 0;
}

```
:) Could you be familiar with `Switch` statement? Then, stop expecting the result of the codes and let's make a program! Solve a following problem!

  * **Problem 4-6:** Your brother is a freshman of the university. So, you wanna let him know about the standard of the grade. For instance, for "A" grade, about what scores he should get, you'll make a program to do this thing. Then, how should you make the code? Write down your own ans codes.  

```
//Example 4-6
#include <iostream>

using namespace std;

int main()
{
    char cSel{'Z'};
    
    cout << "Which grade standard do you know about? ";
    cin >> cSel;
    
    cout << "For " << cSel << " grade....." << endl; 
    
    switch (cSel)
    {
        case 'A':
        case 'a':
            cout << "You should get 80-over-points." << endl;
            break;
        case 'B':
        case 'b':
            cout << "You should get the points between 60 and 80." << endl;
            break;
        case 'C':
        case 'c':
            cout << "You should get the points between 60 and 40." << endl;
            break;
        default:
            cout << "Your input has been wrong." << endl;
    }

    return 0;
}
```


## 4.3 Results of Examples
  * Example **4-1** Result (example)
  ```
  Enter the radius(enter -1 for close): 3
  circumference with a radius of 3 : 18.84(f)
  Enter the radius(enter -1 for close): -1
  
  ```

  * Example **4-2** Result (example)
  ```
  Enter your score: 55
  Your Score: 55
  Your grade is C
  
  ```
  
  * Example **4-3** Result (example)
  ```
  20
  
  ```
  
  * Example **4-4** Result(1) (example)
  ```
  Enter a first number: 19
  Enter a second number: 3
  6.33333
  
  ```
  
  * Example **4-4** Result(2) (example)
  ```
  Enter a first number: 19
  Enter a second number: 0
  -1
  
  ```
  
  
  * Example **4-5** Result(1) (example)
  ```
  Which product do you want to know information about?                                                                                  
  1. Airpods      2. iPhone       3. Galaxy Series        4. Buds Plus                                                                  
  Enter your choice: 3                                                                                                                  
  This section is about 'Galaxy Series'.                                                                                                
  This section is about 'Buds Plus'.         
  
  ```
  
  * Example **4-5** Result(2) (example)
  ```
  Which product do you want to know information about?                                                                                  
  1. Airpods      2. iPhone       3. Galaxy Series        4. Buds Plus                                                                  
  Enter your choice: 1                                                                                                               
  This section is about 'Airpods'.         
  
  ```
  
  * Example **4-6** Result (example)
  ```
  Which grade standard do you know about?: B
  For B grade.....
  You should get the points between 60 and 80.
  
  ```
  
