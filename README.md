# assignment-algorithms-course
#include <iostream>
#include<chrono>
using namespace std;

long long factorialrec( long long n){
if(n==1)
    return 1;
else
    return n* factorialrec(n-1);
}
long long factorialitr(long long n){
long long sum=1;
for(int i=1; i<=n;i++){
    sum*=i;}
return sum;
}
int main() {

    auto start_time = std::chrono::high_resolution_clock::now();
    long long m;
    cout<<"please enter value of n:"<<endl;
    cin>>m;
cout<<"RECURSIVE FUN : "<<factorialrec(m)<<endl;
cout<<"ITERATIVE FUN : "<<factorialitr(m)<<endl;
    auto end_time = std::chrono::high_resolution_clock::now();


    auto duration = std::chrono::duration_cast<std::chrono::microseconds>(end_time - start_time);
    std::cout << "ex time: " << duration.count() << " ms" << std::endl;

return 0;
}
