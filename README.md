#include<iostream>
using namespace std;
int n;
string s[20] = { "zero","one","two","three","four","five","six","seven","eight","nine" };
string t[20] = { "ten","eleven","twelve","thirteen","fourteen" };
string s2[20] = { "twen","thir","for","fif","six","seven","eigh","nine" };
int main()
{
	cin >> n;
	if (n < 10)
		cout << s[n];
	else if (n < 15)
		cout << t[n - 10];
	else if (n < 20)
		cout << s2[n - 12] << "teen";
	else if (n % 10 == 0)
		cout << s2[(n / 10) - 2] << "ty";
	else   if (n % 10 != 0)
		cout << s2[(n / 10) - 2] << "ty-" << s[n % 10]; 
	return 0;
}
