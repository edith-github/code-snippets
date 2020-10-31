# Linear Search in Array

```cpp
#include <iostream>
using namespace std;
void linear_search(int a[],int c,int n){
		for(int i=0;i<n;i++){ 
			if(a[i]==c){
				cout<<"The element is found at index "<<i<<".\n";
				return;
			}
	  }
	  cout<<"The element is not found.\n";
	  return;
}
int main(){
	int n;
	int c=0;
	cout<<"Enter the size of array:\n";
	cin>>n;
	int a[n];
	cout<<"Enter the numbers of the array:\n";
	for(int i=0;i<n;i++){
		cin>>a[i];
	}
	cout<<"Enter the element you want to find:\n";
	cin>>c;
	linear_search(a,c,n);
	return 0;
}

```
