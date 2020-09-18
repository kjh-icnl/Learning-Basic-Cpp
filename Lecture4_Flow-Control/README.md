# 4 Lecture(4) : Flow Control
## 4.1 Before You Start
:) In Lecture (2), I said like this **Whenever the programming lines end, you must write ;(semi-colon). At this time, you should be able to distinguish `code line` and `code block`**. Before the beginning, I'll explain this. 
  * **Code Block** can inclue `Code Block` and `Code Line`
  * **Code Line** belong to only `Code Block`  
  
:) Then, how can we recognize "Code Block" and "Code Line"? `Code Block` is distinguished by mid-bracket {} on C/C++. If there is {}, the parts are called as "Code Block". Then "Code Line"? In one code block, `everything` except for any code blocks: this is `code line`. Take a look at the following example.

  * **Problem 4-1 :** Now, you wanna make a program to calculate a circumference with a radius if you enter a radius. Also, unless you enter number 0, you wanna let your program continuously be executing. Then, why don't you make a code that has these functions?

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
        cout << "Enter the radius? ";
        cin >> iValue;
        if (iValue == 0)
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


## 4.2 Conditional Statement
### 4.2.1 if STATEMENT
:) **`if statement`** is really important and typical C++ grammar. It's better to watch the grammar structure once than to explain it one-hundred time in texts. Let's take a look!
```
**Structure**
if ( Condition 1 )
{
    Statement 1
}
else if ( Condition 2 )
{
    Statement 2
}
else if ( Condition 3 )
{
    Statement 3
}

...

else if ( Condition N )
{
    Statement N
}
else
{
    Statement N+1
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


### 4.2.2 Tenary Operator
:) Indeed, you don't have to know this grammar in detail. Because there are few people who use this structure. However, the reason why you need to know this is related to communications with other people(programmers). Okay, then let's see the structure first.
```
( Condition ) ? True_Statement : False_Statement;
```
 > **NOTE** : True_Statement means that the statement will be executed when the condition is true, while False_Statement means that the statement will be executed when the condition is false.  

:) Okay, then seeing one example, learn the logic. And anticipate the result of this code.

```
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


:) Yes, it's quite simple comparing with `if statement`. However, it has also weakness when you make some more complicated program. So, in my case, I don't have a good memory so that I don't use this `Tenary Operator`. Even though I don't use it, you can use it if you feel comfortable when you use tenary operator. Then, let' solve really easy problem together!

  * **Problem 4-3** : 



## 4.3 Loop Statement


## 4.4 Results of Examples

