# Recursive-Program-to-find-Largest-Element-of-the-array-in-CPP

Largest Element of  the array using Recursion in C++
Here, in this page we will discuss the program to find the largest element of the array using recursion in C++ programming language. We are given with an array and we need to print the largest element among the elements of the array.

Example :

Input : arr[6] = {13, 89, 76, 43, 7, 90}
Output : Largest Element is 90
We will discuss both approaches to find largest element using recursion and iteratively.

Largest Element of the array using Recursion in C++
Method 1(Using Recursion) :
Create a recursive function say, largest_element (int n, int arr[]).
Base Condition : If(n==1) return arr[0].
Else, return max(arr[n-1], largest_element(n-1, arr))
 
Time and Space Complexity :
Time Complexity : O(n)
Space Complexity : O(1)
to find largest element of the array using recursion
Code in C++
Run
#include<bits/stdc++.h>
using namespace std;

//Recursive function
int largest_element(int n, int arr[]){

   if(n==1) return arr[0];  // Base condition

   return max(arr[n-1], largest_element(n-1, arr));
}
//Driver code
 int main(){ int arr[] = {10, 45, 78, 34, 67};
 int n = sizeof(arr)/sizeof(arr[0]); 
cout<<"Largest Element is : "<<largest_element(n, arr); }
Output
Largest Element is : 78
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Smallest element in an array

Power of a Number

Prime Number

Method 2 (Non Recursive Approach ) :
Create a variable say max_element and initialize with INT_MIN.
Run a loop from 0 to N and set max_element = max(arr[i], max_element).
After complete iteration print max_element. 
 
Time and Space Complexity :
Time Complexity : O(n)
Space Complexity : O(1)
Code in C++
Run
#include<bits/stdc++.h>
using namespace std;

int largest_element(int n, int arr[]){

   int max_element = INT_MIN;

   for(int i=0; i<n; i++){
      max_element = max(arr[i], max_element);
   }

   return max_element;
}

int main(){

   int arr[] = {10, 45, 78, 34, 67};
   int n = sizeof(arr)/sizeof(arr[0]);
   cout<<"Largest Element is : "<<largest_element(n, arr);
}
Output
Largest Element is : 78
Prime Course Trailer

Related Banners
Get Prime
