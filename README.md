# LOGIC-BUILDING-QUESTION
#include <iostream>
using namespace std;
//code for checking palindrome number(the number whose reverse oder is same as the number you enter)
void palindrome(int n)
{
	int sum=0;
	int rem;
	int c=n;

	while(n>0)
	{
		rem=n%10;
		sum=rem+(sum*10);
		n=n/10;
	}

	if(c==sum)
	{
		cout<<"its a palindrome number";
	}
	else
	{
		cout<<"not a palindrome number";
	}
}
//code for check the factorial of input number
void factorial(int n)
{
	double fact=1;
	for(int i=1; i<=n; i++)
	{
		fact=fact*i;
	}
	cout<<fact;

}
//code for check the input number is armstrong (armstrong is number in which if we are doing of each number that is input and whose sum=input number )
void armstrong(int n)
{
	int rem;
	int arm=0;
	int c=n;
	while(n>0)
	{
		rem=n%10;
		arm=(rem*rem*rem)+arm;
		n=n/10;
	}
	if(c==arm)
	{
		cout<<" its a armstrong number";
	}
	else
	{
		cout<<" not a armstrong number";
	}
}
//code for reverse the given number
void reverse(int n)
{
	int rem;
	int sum=0;
	while(n>0)
	{
		rem=n%10;
		cout<<rem;
		n=n/10;
	}

}
//code for checking number is prime or not
void prime(int n)
{
	int  count=0;
	for(int i=1; i<=n; i++)
	{
		if(n%i==0)
		{
			++count;
		}
	}
	if(count==2)
	{
		cout<<" Its a prime number";
	}
	else
	{
		cout<<" not a prime number";
	}
}
//code for count a given number
void count(int n)
{
	int sum=0;
	while(n>0)
	{
		++sum;
		n=n/10;
	}
	cout<<sum;
}
//code for sum of given number
void sumofnumber(int n)
{
	int sum=0;
	while(n>0)
	{
		int lastdigit=n%10;
		sum=sum+lastdigit;
		n=n/10;
	}
	cout<<sum;
}

//main method
int main() {
	int n;
	cout<<" enter the value "<<endl;
	cin>>n;
	cout<<"1:-Number you want to check(palindrome or not) :-"<<n<<endl;
	palindrome(n);
	cout<<endl;
	cout<<"2:-Number you want to check factorial:-"<<n<<endl;
	factorial(n);
	cout<<endl;
	cout<<"3:-Number you want to check armstrong:-"<<n<<endl;
	armstrong(n);
	cout<<endl;
	cout<<"4:-Number you want to check (in reverse order):-"<<n<<endl;
	reverse(n);
	cout<<endl;
	cout<<"5:-Number you want to check (is prime or not):-"<<n<<endl;
	prime(n);
	cout<<endl;
	cout<<"6:-Number you want to check (how many number input):-"<<n<<endl;
	count(n);
	cout<<endl;
	cout<<"7:-Number you want to check (sum of  input):-"<<n<<endl;
	sumofnumber(n);
	return 0;
}
