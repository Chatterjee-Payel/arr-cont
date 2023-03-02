# arr-cont
class Solution{
    public:
    // Function to check whether the array contains
    // a set of contiguous integers
    bool areElementsContiguous(int arr[], int n)
    {
	// Complete the function
     map<int,int>mp;
     vector<int>v;
     int i=0;
     
     for(int i=0;i<n;i++){
         mp[arr[i]]++;
     }
     for(auto it:mp)
     {
         v.push_back(it.first);
     }
	int count=0;
	for(int i=0;i<v.size();i++){
	    if(v[i+1]-v[i]==1)
	    {
	        count++;
	    }
	    
	}
	if(count+1!=v.size()){
	    return 0;
	}
	return 1;
    }
};
