// complement-of-base-10
class Solution {
public:
    int bitwiseComplement(int n) {
        
        int i = 0 , ans = 0;
        
        if(n==0){
            return 1;
        }
        while(n != 0){
            int bit = ~n & 1;
            if(bit==1){
            ans = ans + pow(2, i);}
            n = n >> 1;
            i++;
        }  
        return ans;
    }
};
