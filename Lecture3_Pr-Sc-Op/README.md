# 3 Lecture(3) : Print/Scan/Operator

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
// Example 1
#include <iostream>

int main()
{
    int iVal = 2;
    std::cout << iVal << std::endl;
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```
At this time, `endl` means "end line". However, if you don't write `std::endl`, you can't go next line because basically `std::cout` doesn't change line when it coompletes its own process.


## 3.2 Operator
