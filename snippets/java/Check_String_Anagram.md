# Check if String is Anagram

```java
class CheckStringAnagram{
  public static void main(String[] args) {
    String str1 = "catsi#&lentrrr";
    String str2 = "#actlistenrrr";

    int a[] = new int[256];
    boolean p = false;
    int k=0;

    if(str1.length() == str2.length()) {
      p=true;
      for(int i=0;i<str1.length();i++) {
        k=(int)str1.charAt(i);
        a[k]++;
      }
      for(int i=0;i<str2.length();i++) {
        k=(int)str2.charAt(i);
        a[k]--;
      }

      for(int i=0;i<256;i++) {
        if(a[i]!=0) {
          p=false;	
          break;
        }
      }
    }
        if(p==true) {
          System.out.println("is Anagram");
        }
        else {
          System.out.println("not Anagram");
        }
    }
}
	

```
	
