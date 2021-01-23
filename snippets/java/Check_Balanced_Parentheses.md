# Check Balanced Parentheses

```java

import java.util.*;

public class Check_Balanced_Parentheses {
	
	static boolean CheckBalancedParentheses(String s) {
		Stack<Character> stack = new Stack<>();
		for (int i = 0; i < s.length(); i++) {
			char c = s.charAt(i);
			if (c == '(' || c == '[' || c == '{')  
            { 
                stack.push(c); 
            } 
			switch (c) {
			case '}' : if(stack.isEmpty()) return false; 														 
					   else if(stack.peek() == '{') stack.pop();
					   	break;
			case ')' : if(stack.isEmpty()) return false;
						else if(stack.peek() == '(') stack.pop();
						break;	
			case ']' : if(stack.isEmpty()) return false;
						else if(stack.peek() == '[') stack.pop();
						break;
			}
		}
		if(stack.isEmpty()) return true;
		return false;
	}
	
	public static void main(String[] args) throws Exception {
		boolean p = CheckBalancedParentheses("{[]}()}}");
		System.out.println(p);
	}
}

```


