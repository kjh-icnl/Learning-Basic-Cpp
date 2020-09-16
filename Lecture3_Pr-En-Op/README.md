# 3 Lecture(3) : Print/Enter/Operator

## 3.1 Print and Scan
### 3.1.1 BASIC Starting Code!!!
:) When you codes on C++, almost you'll follow this format.  

```
#include <iostream>

int main()
{
    "Here Your Codes"

    return 0;
}
```

### 3.1.2 Print Something
:) You can print something about text, number and so on using `std::cout`. If you become familiar with this format about print, you can make codes easily.  

See this example.

```
// Example 1
#include <iostream>

int main()
{
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```
Let's see another example.  

```
// Example 2
#include <iostream>

int main()
{
    int iVal = 2;
    std::cout << iVal << std::endl;
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```
**IMPORTANT** : At this time, `endl` means "end line". However, if you don't write `std::endl`, you can't go next line because basically `std::cout` doesn't change line when it coompletes its own process.  

### 3.1.3 Enter Something
:) You can enter something about text, number and so on using `std::cin`. It's same with 3.1.2. You should be familiar.  

See this example.  

```
// Example 3
#include <iostream>

int main()
{
    int iVal;
    char cVal[10];
    
    std::cout << "Enter your word: ";
    std::cin >> cVal;
    
    std::cout << "Enter your number: ";
    std::cin >> iVal;
    
    std::cout << "Your word is " << cVal << std::endl;
    std::cout << "Your number is " << iVal << std::endl;
    
    return 0;
}
```
The reason why I declared as `cVal[10]` is related with a concept of array. Acutally, "[10]" means the length of the data, especially "char" in this case. Thus, it let us know about that we can input only a word has lower 10 letters. What if I input a word `relationship`? Take a look `3.3 Execution Result of Examples`.


## 3.2 Operator
:) **Arithmetic Operator** : `+`, `-`, `*`, `/` and `%`, where % means a remainder after division. About other operators, I won't explain 'em.  

:) **Assignment Operator** : `=`, `+=`, `-=`, `*=`, `/=` and `%=`. There is really IMPORTANT point: in programming, "=" doesn't mean "equal", but indeed "=" means "substitution". Generally, Assignment operator is made by cobining "=" with Arithmetic operators(AO). However, here is a simple formula.  
  * `Val AO= Num` is equal to `Val = Val A0 Num`  
  > **NOTE** : Normally, "Val" is Variables, "AO" is Arithmetic Operators and "Num" is a number.  

See a following example
```
// Example 4
#include <iostream>

int main()
{
    int iVal_1, iVal_2, iVal_3;
    
    iVal_1 = 1;
    iVal_2 = 2;
    iVal_3 = 3;
    
    iVal_1 += 4; // iVal_1 should be 5
    iVal_2 -= 5; // iVal_2 should be -3
    iVal_3 *= 6; // iVal_3 should be 18
    
    std::cout << iVal_1 << std::endl;
    std::cout << iVal_2 << std::endl;
    std::cout << iVal_3 << std::endl; // Printing results
    
    return 0;
}
```

:) **Increment and decrement operator** : `++` and `--`. This operator is a really easy concept. They mean adding 1 or subtracting 1. If you refer a following example, you can understand this concept totally.
```
// Example 5
#include <iostream>

int main()
{
    int iVal_1, iVal_2;
    
    iVal_1 = 1;
    iVal_2 = 2;
    
    iVal_1 = ++iVal_1; // iVal_1 should be 2
    iVal_2 = --iVal_2; // iVal_2 should be 1
    
    std::cout << iVal_1 << std::endl;
    std::cout << iVal_2 << std::endl; // Printing results
    
    return 0;
}
```
:) **Comparison Operators** : `==`, `!=`, `>`, `<`, `>=` and `<=`. Here "==" means "equal". Explanation skipped.  

:) **Logical Operators** : `&&`, `||` and `!`. If you've studied python, you'd be familiar with "and", "or" and so on. On C++, they have same functions with "and", "or" and so on. Thus "&&" is "and", "||" is "or" and "!" is "is not". Explanation Completed.


## 3.3 Execution Result of Examples
  * Example **1**  Result (example)
  ```
  Hello, World
  
  ...Press Any Button to exit console.
  ```
  You can ignore some texts such as "...Pres ~". Important part is `Hello, World`. From now, I won't write this line.  
  
  * Example **2**  Result (example)
  ```
  2
  Hello, World
  
  ```

  * Example **3**  Result(1) (example)
  ```
  Enter your word: apple
  Enter your number: 20
  Your word is apple
  Your number is 20
  
  ```

  * Example **3**  Result(2) (example)
  ```
  Enter your word: relationship
  Enter your number: 20
  Your word is relationship
  Your number is 20
  
  ```
  or
  ```
  Enter your word: relationship
  Enter your number: 20
  Your word is relationsh
  Your number is 20
  
  ```
  You can get any result like this. This expression means that a length of the entered word is over a previous set array length (indeed 10).  
  
  * Example **4**  Result (example)
  ```
  5
  -3
  18
  
  ```
  
  * Example **5**  Result (example)
  ```
  2
  1
  
  ```




