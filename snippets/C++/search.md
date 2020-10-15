# BINARY SEARCH

```cpp
#include <iostream>
using namespace std;

int main()
{   system("clear");
	int count, i, arr[30], num, first, last, middle;
	cout<<"Number of elements :"; 
        cin>>count;

	for (i=0; i<count; i++)
	{
		cout<<"Enter number "<<(i+1)<<": "; 
                cin>>arr[i];
	}
	cout<<"Enter the number that you want to search :"; 
        cin>>num;
	first = 0;
	last = count-1;
	middle = (first+last)/2;
	while (first <= last)
	{
	   if(arr[middle] < num)
	   {
		first = middle + 1;

	   }
	   else if(arr[middle] == num)
	   {
		cout<<endl<<num<<" found in the array at the location "<<middle+1<<"\n"; 
                break; 
           } 
           else { 
                last = middle - 1; 
           } 
           middle = (first + last)/2; 
        } 
        if(first > last)
	{
	   cout<<endl<<num<<" not found in the array";
	}
    cout<<endl;
	return 0;
}
```


# LINEAR SEARCH

```cpp

#include <iostream> 
using namespace std; 
  
int search(int arr[], int n, int x) 
{ 
    int i; 
    for (i = 0; i < n; i++) 
        if (arr[i] == x) 
            return i; 
    return -1; 
} 
  
int main() 
{   system("clear");
    int arr[] = { 2, 3, 4, 10, 40, 50, 60 }; 
    cout<<"Enter the element to be searched : ";
    int x ;
    cin>>x;
    cout<<endl;
    int n = sizeof(arr) / sizeof(arr[0]);
    cout<<"CURRENT ARRAY"<<endl<<endl;
    for(int i=0;i<n;i++) 
    {
        cout<<arr[i]<<" ";
    }
    cout<<endl<<endl;
    int result = search(arr, n, x); 
   if (result == -1)
   {
       cout<<"Element " << x<< " is not present in array"<<endl ;
   } 
    else 
    {
        cout<<"Element is present at index : " <<result; 
    }
   cout<<endl<<endl;
   return 0; 

   
```
