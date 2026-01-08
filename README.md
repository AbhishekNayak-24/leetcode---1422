# leetcode---1422
Maximum Score After Splitting a String 
code in java

kkkk

llll



public class Solution {
    public int maxScore(String s) {
        int maxScore = 0;
        for (int i = 1; i < s.length(); i++) {
            String left = s.substring(0, i);
            String right = s.substring(i);
            int score = countZeros(left) + countOnes(right);
            maxScore = Math.max(maxScore, score);
        }
        return maxScore;
    }lll

    private int countZeros(String s) {
        int count = 0;
        for (char c : s.toCharArray()) {
            if (c == '0') {
                count++;
            }
        }
        return count;
    }
    lll

    private int countOnes(String s) {
        int count = 0;
        for (char c : s.toCharArray()) {
            if (c == '1') {
                count++;
            }
        }
        return count;
    }
}

