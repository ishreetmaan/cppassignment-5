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

int main() 
{
    const int size = 5;
   
    int array[size] = { 191,65,98,478,99 };

   
    int* copy = reversedcopied(array, size);

   
    cout << "the Original array is: ";
    for (int i = 0; i < size; i++)
        cout << array[i] << " ";
    cout << endl;

    cout << "Copied array with reverse order is: ";
    for (int i = 0; i < size; i++)
        cout << copy[i] << endl;
    

       delete[] copy;
    return 0;
