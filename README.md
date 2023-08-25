# anagram

class Solution {
public:
    vector<vector<string>> groupAnagrams(vector<string>& strs) {
        vector<vector<string>>ans;
        unordered_map<string, vector<string>>umap;
        for(auto x:strs)//put all values of strs in x
        {
            string temp=x;//temp=unsorted string
            sort(x.begin(), x.end());
            umap[x].push_back(temp);//x=key        temp=value
        }
        
        for(auto x:umap){
            ans.push_back(x.second);
        }
        return ans;
    }
};
