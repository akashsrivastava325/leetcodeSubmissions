This is my leetcode daily submissions repository where i would share files of daily submissions that i submitted on leetcode platform.


DAY 2:

class Solution {
public:
    bool detectCapitalUse(string word) {
        int a = 0, b = 0, c = 0;

        for(int i = 0; i < word.length(); i++) {
            if(i == 0 && word[i] >= 'A' && word[i] <= 'Z') {
                c++;
            }
            if(word[i] >= 'A' && word[i] <= 'Z') {
                a++;
            }
            if(word[i] >= 'a' && word[i] <= 'z') {
                b++;
            }
        }

        int n = word.size();
        if(c == 1 && b == n - 1 || a == n || b == n) {
            return true;
        }
        else return false;
    }
};
