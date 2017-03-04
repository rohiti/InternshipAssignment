#include<bits/stdc++.h>
using namespace std;
#define ll long long
#define mod 1000000007
void multiply(ll F[2][2],ll M[2][2])
{
  ll x =  (F[0][0]*M[0][0] + F[0][1]*M[1][0])%mod;
  ll y =  (F[0][0]*M[0][1] + F[0][1]*M[1][1])%mod;
  ll z =  (F[1][0]*M[0][0] + F[1][1]*M[1][0])%mod;
  ll w =  (F[1][0]*M[0][1] + F[1][1]*M[1][1])%mod;
  F[0][0] = x;
  F[0][1] = y;
  F[1][0] = z;
  F[1][1] = w;
}
ll pwr(ll n)
{
    ll res[2][2] = {1,0,0,1};
    ll F[2][2] = {1,1,1,0};
    while(n)
    {
        if(n&1)
        {
            multiply(res,F);
        }
        multiply(F,F);
        n/=2;
    }
    return res[0][0];
}
int main()
{
    ll t;
    scanf("%lld",&t);
    while(t--)
    {
        ll n;
        scanf("%lld",&n);
        printf("%lld\n",pwr(n+1));
    }
    return 0;
}
