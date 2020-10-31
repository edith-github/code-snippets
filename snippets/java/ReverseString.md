# Reverse String

```java

class ReverseString {

	public static void main(String[] args){
    String s="The sky is blue!  ";
    int j=0;
        String ans="";
        int i=s.length()-1;
        while(i >= 0){
            while(i>=0 && s.charAt(i)==' ') i--;
            j=i;
            if(i<0) break;//for leading spaces
            while(i>=0 && s.charAt(i)!=' ' )i--;
            
            if(ans.isEmpty()){
                ans = ans.concat(s.substring(i+1,j+1));
            }else{
                ans = ans.concat(" "+s.substring(i+1,j+1));
            }
                   
        }
        System.out.println(ans);
	   }
	}	
  
  ```
