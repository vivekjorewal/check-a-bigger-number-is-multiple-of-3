# check-a-bigger-number-is-multiple-of-3

#include <stdio.h>
//#include <math.h>
void check(long long int x,int y,int z){
    if((y + z) == 10){
	        if(((y + z) % 3) == 0){
	            printf("YES\n");
	        }
	        else printf("NO\n");
	    }
	else if((y+z) == 5 || (y+z) == 15){
	        printf("NO\n");
	    }
    else {
    long long int a = 0;
    //int q=0;
    a = y+z;
    int p = (y+z)%10;
    if(x == 2){
        if(a%3 == 0) printf("YES\n");
        else printf("NO\n");
    }
    else{
    a += p;
    long long int nog = (x-3)/4;
    int rnod = (x-3)%4;
    a += (20*nog);
    for(int j=0;j<rnod;j++){
        p = (2 * p)%10;
        a += p;
    }
    
    if(a%3 == 0){
        printf("YES\n");
    }
    else printf("NO\n");
    }
}
}
int main(void) {
	// your code goes here
	int t;
	scanf("%d",&t);
	for(int i=0;i<t;i++){
	    long long int k;
	    int d0,d1;
	    scanf("%lld ",&k);
	    scanf("%d %d",&d0,&d1);
	    //printf("%d %d",d0,d1);
	    check(k,d0,d1);
	}
	return 0;
}
