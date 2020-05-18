#include <iostream>
using namespace std;
const int MAX = 1000000;
int prime[MAX];
static bool check[MAX+1];
int pn;

int main()
{
    /* Turn off sync to boost speed */
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    cout.tie(NULL);
    
    /*Get all the prime numbers by the sieve*/
    check[0]=check[1]=true;
    for (int i=2 ; i*i<=MAX;i++) {
        if (check[i]==false){
            prime[pn++]=i;
            for (int j=i+i; j<=MAX;j+=i){
                check[j]=true;
            }
        }
    }
    
    
    while (1){
        int input;
        cin >> input;
        
        if (input == 0){
            return 0;
        }
        for(int i = 1; i < pn;i++){
            if (check[input-prime[i]] == false){
                cout << input << " = " << prime[i] << " + " << input - prime[i] << '\n';
                break;
            }
        }
    }
    return 0;
}
