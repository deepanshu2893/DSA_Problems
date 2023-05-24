# 17. Letter Combinations of a Phone Number :
  1. Difficulty - Medium
  2. [Question Link](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)
  3. Language - Java

***Solution***
```
class Solution {
    public List<String> letterCombinations(String digits) {
        List <String> AL = new ArrayList<String>(); 
        LC(digits, "", AL);
        return AL; 
    }
    public static void LC(String word, String combo, List <String> ans) {
		if (word.isEmpty()) {
		//	System.out.println(combo);
        if (combo.length() > 0){
 ans.add(combo); 
        }
       
			return;
		}
		char ch = word.charAt(0); 
		String op = options(ch); 
		String remain = word.substring(1); 
		for (int i = 0; i < op.length(); i++) {
			LC(remain, combo + op.charAt(i), ans); 
		}
		
	}

	public static String options(char ch) {
		if (ch == '2') {
			return "abc";

		} else if (ch == '3') {
			return "def";

		} else if (ch == '4') {
			return "ghi";

		} else if (ch == '5') {
			return "jkl";

		} else if (ch == '6') {
			return "mno";

		} else if (ch == '7') {
			return "pqrs";

		} else if (ch == '8') {
			return "tuv";

		} else if (ch == '9') {
			return "wxyz";

		} else {
			return ""; 
		}
    }
}
```
