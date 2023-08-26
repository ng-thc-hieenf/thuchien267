//de: tim bcnn 2 so
//sd vong for chay tu i den n gan kq = bcnn kq va a[i] cout kq

#include <bits/stdc++.h>
#define ll long long
using namespace std;
int BCNN(int a, int b)
{
	return (a*b)/__gcd(a,b);
}
int BCNN_Mang(int a[],int n){
		int k = BCNN(a[0], a[1] );
		for(int i=2;i<n;i++){
			k = BCNN(k, a[i]);	
		}
		return k;
}
void xuly()
{
		int n; cin>>n;
    	int a[105];
    	for (int i=1; i<=n; i++) cin>>a[i];
		cout<<BCNN_Mang(a,n);
		cout<<endl;
}
int main(){
//	freopen("LCMLIST.INP","r",stdin);
//	freopen("LCMLIST.OUT","w",stdout);
	int T; cin>>T;
	while(T--){
		xuly();
	}
    return 0;
}
