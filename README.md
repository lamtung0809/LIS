 LIS
dãy con tăng dài nhất
#include<iostream>
#include<algorithm>
#include<stdio.h>
using namespace std;

typedef long long ll;
#define f first
#define s second
#define I cin
#define O cout
#define ff(i,a,b) for(ll i=a;i<=b;++i)
#define FF(i,a,b) for(ll i=a;i>=b;--i)


int main(){
    long int a[100001];
    long int m[100001];
    //int p[100001];
    //int ans[100001];
    
    long int n,L=0;
    
    scanf("%ld",&n);
    
    ff(i,1,n) scanf("%ld",&a[i]);
        
    ff(i,1,n){
    	long int lo=1;
    	long int hi=L;
    	while(lo<=hi){
    		int mid=(lo+hi)>>1;
    		if(a[m[mid]]<a[i]) lo=mid+1;
    		else hi=mid-1;
    	}
    	
    	int newL=lo;
    //	p[i]=m[newL-1];
    	m[newL]=i;
    	
    	if(newL>L) L=newL;
    }
    //int k=m[L];
    printf("%ld",L);
    
	/*
    FF(i,L,1){
    	ans[i]=a[k];
    	k=p[k];
    }
    ff(i,1,L) printf("%d\n",ans[i]);
    */
}
