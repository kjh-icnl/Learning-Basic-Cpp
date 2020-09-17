# 4 Lecture(4) : Flow Control
## 4.1 Before You Start
:) In Lecture (2), I said like this **Whenever the programming lines end, you must write ;(semi-colon). At this time, you should be able to distinguish `code line` and `code block`**. Before the beginning, I'll explain this. 
  * **Code Block** can inclue `Code Block` and `Code Line`
  * **Code Line** belong to only `Code Block`  
  
:) Then, how can we recognize "Code Block" and "Code Line"? `Code Block` is distinguished by mid-bracket {} on C/C++. If there is {}, the parts are called as "Code Block". Then "Code Line"? In one code block, `everything` except for any code blocks: this is `code line`. Take a look at the following example.

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

:) Hello?

## 4.3 Loop Statement


## 4.4 Results of Examples

