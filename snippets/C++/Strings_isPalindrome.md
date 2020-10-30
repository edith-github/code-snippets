# Checking Palindrome in strings

For checking palindromic strings, chracters equidistance from 1st position and last position must be equal.

```cpp
#include<iostream>
using namespace std;
int main() {
    string str;
    cin >> str;

    const char* strArr = str.c_str();
    bool isPalindrom = true;

    //Checking the palindrome string.
    for (int i = 0; i < str.length(); i++) {
        if(str[i]!=str[str.length()-i-1]){
            isPalindrom=false;
            break;
        }
    }
    if(isPalindrom){
        cout << "true" << endl;
    }else{
        cout << "false" << endl;
    }
    return 0;
}
```
