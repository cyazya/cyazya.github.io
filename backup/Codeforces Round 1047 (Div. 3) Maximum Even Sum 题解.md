我们看一下题目所给的样例，试着自己推一下k的值是多少，不难推出，1 8对应的是2，7 7对应的是7，2 6对应的是3，9 16对应的是8，4 6对应的是3。可以发现，当b为偶数时，k的值为b的一半，b为奇数时，k为b本身。那么就有一个问题了，1 8对应的2这个不符合我们的结论，是不是错了呢？别急，试着把k=4代进去，可以发现，k=4时也是符合的，结论正确。以下是我的代码：#include <bits/stdc++.h>
#define int long long
#define endl "\n"
#define IOS ios::sync_with_stdio(0);cin.tie(0);cout.tie(0)
using namespace std;
signed main() {
    IOS;
    int T = 1;
    cin >> T;
    while (T--) {
        int a,b;
        int k,r;
        cin>>a>>b;
        if(b%2==0){
        	k=b/2;
        	r=2+a*k;
		}else{
			k=b;
			r=1+a*k;
		}
		if(r%2==0){
			cout<<r<<endl;
		}else{
			cout<<-1<<endl;
		}
    }
    return 0;
}