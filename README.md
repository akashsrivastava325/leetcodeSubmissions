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

DAY 3:
class Solution {
public:
    int minDeletionSize(vector<string>& strs) {
        int ans = 0;

        for(int i = 0; i < strs[0].size(); i++) {
            int c = 0;
            for(int j = 1; j < strs.size(); j++) {
                if(strs[j - 1][i] <= strs[j][i]) {
                    c++;
                }
                else {
                    c = -1;
                    break;
                }
            }
            if(c == -1) ans++;
        }
        return ans;
    }
};
