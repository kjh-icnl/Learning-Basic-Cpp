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
The reason why I declared as `cVal[10]` is related with a concept of array. Acutally, "[10]" means the length of the data type, especially "char" in this case.


## 3.2 Operator


## 3.3 Execution Result of Examples
