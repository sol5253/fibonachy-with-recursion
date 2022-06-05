# fibonachy-with-recursion
#include<bits/stdc++.h>
using namespace std;
// this is fibbonchi with recursion
//fibonachi is a series in which each series index have its own value
// given in fibo that 0 th series number 0 
// 1 th position have 1 cause fibo is sum of position -1 + position -2  means only 1 is there
// 2 th have 1 +0
// 3 th have second th + 1 th = (0+1) + 1
// 4 th have third + second = 2 + 1
// 5 th have fouth + third = 2 + 1
int fun(int N);
int main(){
    cout<<"enter the position till you want to print fiboo ";
    int n;
    cin>>n;
    for(int i=1;i<=n;i++){
       cout<< fun(i);
    }
}
int fun(int N){
   if(N==1 || N==2){
       return 1;  // this is base case
   }
   else{
       int fibo1=fun(N-1);
       int fibo2=fun(N-2);   // small case and recursion
       int fibooos=fibo1+fibo2;  
       return fibooos;  
   }
}
