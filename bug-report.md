# Bug 1

1. **The incorrect original code or code snippit that you wrote:**

``` cpp
// assignment-5.cpp : This file contains the 'main' function. Program execution begins and ends there.
//

#include <iostream>
using namespace std;

int doSomething(int *x, int *y) 
{
    int temp = *x;
    *x = *y * 5;
    *y = temp * 3;
    return *x + *y;
}
int main() 
{
    int x = 10, y = 5;
    cout << "values before calling doSomething(), x: " << x << ", y: " << y << endl;
    int result = doSomething(&x, &y);
    cout << "doSomething returned " << result << endl;
    cout << "values after calling doSomething(), x: " << x << ", y: " << y << endl;
    return 0;
}
```

2. **What bug does the original code have?**

  in the pointers we have to take care of the * and & , here the * is misplaced while declaration.

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**
   sometimes we miss small details about writing a code.
4. **How to correct the bug?**
   we must check out our work once we are complete and also take care while we are doing it
5. **The corresponding bug-free code or code snippet is:**

```cpp
// assignment-5.cpp : This file contains the 'main' function. Program execution begins and ends there.
//

#include <iostream>
using namespace std;

int doSomething(int* x, int* y) 
{
    int temp = *x;
    *x = *y * 5;
    *y = temp * 3;
    return *x + *y;
}
int main() 
{
    int x = 10, y = 5;
    cout << "values before calling doSomething(), x: " << x << ", y: " << y << endl;
    int result = doSomething(&x, &y);
    cout << "doSomething returned " << result << endl;
    cout << "values after calling doSomething(), x: " << x << ", y: " << y << endl;
    return 0;
}
		


```

6. **What is the take-away message from this bug?**

be carefull for the small small details too while writting the code.

# Bug 2

1. **The incorrect original code or code snippit that you wrote:**

``
// question16 assignment-5.cpp : This file contains the 'main' function. Program execution begins and ends there.
//

#include<iostream>

using namespace std;


int* reversedcopied(int array[], int size)
{
   
    int* copy = new int[size];
   
    for (int i = 0; i < size; i++)
    {
        copy[i] = array[size - 1 - i];
    }
   
    return copy;
}

int main 
{
    const int size = 5;
   
    int array[size] =  {191,65,98,478,99};

   
    int* copy = reversedcopied(array, size);

   
    cout << "the Original array is: ";
    for (int i = 0; i < size; i++)
        cout << array[i] << " ";
    cout << endl;

    cout << "Copied array with reverse order is: ";
    
        cout << copy[i] << endl;
    

      
    return 0;
}
```

2. **What bug does the original code have?**

  the () are missing in the front of the int main function, usualyy this appears automatically so we can sometimes forget to add these, however these are mandatory.

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**
   this bug was there due to lack of concentration only
4. **How to correct the bug?**
   be carefull and check the code once you are done
5. **The corresponding bug-free code or code snippet is:**

```


```

6. **What is the take-away message from this bug?**
   be carefull all the time you do the assignment

---

# Bug 3

1. **The incorrect original code or code snippit that you wrote:**

```
#include <iostream>
using namespace std;


int main()
{
	int CAD;
	int USD;
	int A;
	int B;
	int currency{};

	cout << "press 1 to convert USD to CAD" << endl;
	cout << "press 2 to convert CAD to USD" << endl;
	cin >> currency;

	switch (currency) {
	case 1 :
		cout << " Enter the amount you want to enter ";
		cin >> currency;
		CAD = currency / 1.32;
		cout << " Your USD equals " << endl;
		cout << CAD << endl;
		break;
	case 2 :
		cout << " Enter the amount you want to enter ";
		USD = currency * 0.75;
		cin >> currency;
		cout << " Your CAD equals " << endl;
		cout << USD << endl;
		break;
	default:
		cout << " The currency exchange is... ";
	}

	return ;

		
}

```

2. **What bug does the original code have?**

  at the end of the code, on the return line we must add 0, here it is missing.

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**
   lack of concentration only.
4. **How to correct the bug?**
   be carefull while you perform the code 
5. **The corresponding bug-free code or code snippet is:**

```
#include <iostream>
using namespace std;


int main()
{
	int CAD;
	int USD;
	int A;
	int B;
	int currency{};

	cout << "press 1 to convert USD to CAD" << endl;
	cout << "press 2 to convert CAD to USD" << endl;
	cin >> currency;

	switch (currency) {
	case 1:
		cout << " Enter the amount you want to enter ";
		cin >> currency;
		CAD = currency / 1.32;
		cout << " Your USD equals " << endl;
		cout << CAD << endl;
		break;
	case 2:
		cout << " Enter the amount you want to enter ";
		USD = currency * 0.75;
		cin >> currency;
		cout << " Your CAD equals " << endl;
		cout << USD << endl;
		break;
	default:
		cout << " The currency exchange is... ";
	}

	return 0;


}


```

6. **What is the take-away message from this bug?**
   be carefull while u do the assignment
