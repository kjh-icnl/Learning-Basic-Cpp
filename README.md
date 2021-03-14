# Learning-Basic-Cpp

<여기엔 이미지 넣기>



## Properties Of This Lecture

 Hello, guys! Welcome to my "Learning C++" Repository!!
 First of all, I guess I should let you know me. Actually, I'm from Korea(I'm a NATIVE!). 
 My major is Physics and Computer Science. This Lecture(Repository) will teach you about `Basic C++`.
 - If you watch and study C++ lecture through my class constantly, you can become Basic C++ Master!!
 - This class will use English. Also, Kor Ver. will be made.
 - I won't teach you any useless grammar or key-word. By the way, just in case, I'll add extra C++ application at APPENDIX.
 - After studying these programming lectures completely, you can make some programs anywhere and anytime!
 

 
 ## Lecture List (futured)
 ※ This List will be able to be changed along the schedule or the quantity of a lecture.
  1. What is C++? Let's apply **IDE** (Integrated Development Environment)
  2. What are **Data Type and Variable** on C++?
  3. Now is Real-Practice! Let's learn **Super-Beginning Grammar!** (std::cout, std::cin, and so on)
  4. **Flow Control Part 1** : Conditional Statement
  5. **Flow Control Part 2** : Loop Statement
  6. Not Expected

  

 ## What if...
 Yes, you can face any difficult obstacles. It ain't special, it's normal. Don't worry. You have me.
 
 
   * What if you can't understand some C++ codes or you continuously face ERROR?
   * What if you wanna check your own code from me?
   * What if you have extra and detailed question?
   * And so on... what if?  


You can leave any comments on my lecture!! Or You can feel free to contact me through my e-mail : `kjh2159@dgist.ac.kr` or `jsk24j@gmail.com` !!!



 ## If I can think something to add, then I'll add 'em !!!!



```
#include "pbPlots.hpp"
#include "supportLib.hpp"
#include <math.h>


std::vector<double> createDomain(const double start, const double end, const double step){
    std::vector<double> domain;
    for (double i=start; i<end; i += step){
        domain.push_back(i);
    }
    return domain;
}

std::vector<double> sin_func(const std::vector<double> domain){
    std::vector<double> range;
    for (int i=0; i<domain.size() ;i++){
        range.push_back(sin(domain[i]));
    }
    return range;
}



int main() 
{
    RGBABitmapImageReference *imageRef = CreateRGBABitmapImageReference();

    //std::vector<double> x = {-2, -1, 0, 1, 2};
    //std::vector<double> y = {2, -1, -2, -1, 2};

    std::vector<double> x = createDomain(-5, 5, 0.3);
    std::vector<double> y = sin_func(x);

    DrawScatterPlot(imageRef, 1000, 1000, &x, &y);

    std::vector<double> *pngData = ConvertToPNG(imageRef->image);
    WriteToFile(pngData, "plot.png");
    DeleteImage(imageRef->image);

    return 0;
}
```
