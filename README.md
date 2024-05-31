# Pashupatiath1strepo
this is my first Repository
<br>
Author-> Pashupatinath soni

// find kth largest element without sorting array (leetcode-215)<br>
<br>



    int findKthLargest(vector<int>& nums, int k) { 
        map<int,int ,greater<int> >freq;
        for(int i=0;i<nums.size();i++){
            freq[nums[i]]++;
        }
        map<int, int>::iterator it;
        int  kthlargest ;
        for( it = freq.begin();it != freq.end();it++){
            if(it->second >= k) {
                kthlargest = it->first;
                return it->first;
                break;
            }
            k = k-it->second;
        }

        return (int)kthlargest;
    }
