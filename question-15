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
