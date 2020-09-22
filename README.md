# Dictionary-to-find-Phone-Number
Given  names and phone numbers, assemble a phone book that maps friends' names to their respective phone numbers. You will then be given an unknown number of names to query your phone book for. For each  queried, print the associated entry from your phone book on a new line in the form name=phoneNumber; if an entry for  is not found, print Not found instead.
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include<map>

using namespace std;
int main()
{
    int n;
    string name;
    long num;
    cin >> n;
    cin.ignore();
    map <string,long> pbook;
    for (int i=0;i<n;i++)
    {
        cin >> name;
        cin >> num;
        pbook[name] = num;
    }
    while(cin>>name) 
    {
        if (pbook.find(name)!=pbook.end())
            cout<<name<<"="<<pbook.find(name)->second<<endl;
        else
            cout<<"Not found"<<endl;
    }
    return 0;
}
