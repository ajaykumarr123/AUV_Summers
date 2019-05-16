```#include <bits/stdc++.h> ```  //for everything
# vectors
```vector<int>v; ```      //creates an empty vector of integers)
int size=v.size();

v.push_back(x);   //Pushing an integer into a vector

v.pop_back();     //Popping the last element from the vector

sort(v.begin(),v.end()); //Sorting a vector


erase(int position)  //Removes the element present at position.  
       Ex: v.erase(v.begin()+4); (erases the fifth element of the vector v)

erase(int start,int end)  //Removes the elements in the range from start to end inclusive of the start and exclusive of the end.
       Ex:v.erase(v.begin()+2,v.begin()+5);   (erases all the elements from the third element to the fifth element.)



In C++, to set them all to -1, you can use something like std::fill_n (from <algorithm>):

std::fill_n(array, 100, -1);
