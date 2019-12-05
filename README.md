#include<stdio.h>


void get_m(int *p,int n);
void put_m(int *p,int n);
void sort_m(int *p,int n);

int main()
{
	int n;
	scanf("%d",&n);
	int a[n];
	int *p;
	p=a;
	get_m(p,n);
	sort_m(p,n);
	put_m(p,n);
	
}		
void get_m(int *p,int n){
	for(int i=0;i<n;i++)scanf("%d",(p+i));
}
void put_m(int *p,int n){
	for(int i=0;i<n;i++)printf("%d ",*(p+i));
}
void sort_m(int *p,int n){
	int s;
	for(int j=0;j<n-1;j++){
	    for(int i=0;i+j<n-1;i++){
    	    if (*(p+i)>*(p+i+1)){
	        	s=*(p+i);
	        	*(p+i)=*(p+i+1);
    	    	*(p+i+1)=s;
        	}
        }
	}
}

