#include <iostream>
using namespace std;
typedef long long ll;

int numberOf5sinRange(ll n)
{
	if (n < 5)
		return 0;
	int result = 0;
	ll power10 = 1;
	while (power10 * 10 < n)
		power10 *= 10;
	ll msb = n / power10;
	ll remainder = n % power10;
	if (msb > 5)
		result += power10;
	if (msb == 5)
		result += remainder + 1;
	result += msb * numberOf5sinRange(power10);
	result += numberOf5sinRange(remainder);
	return result;
}

int main() {
	ll num;
	cout << "Ingrese el n" << char(163) << "mero: ";
	cin >> num;
	cout << numberOf5sinRange(num) << endl;
	return 0;
}
