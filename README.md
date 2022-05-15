#include<iostream>
using namespace std;
int calculator(int t,int s,char r);
bool agn(char a);
int main()
{
	int t,s;
	char r,a;
	cout<<"Hello\n"<<"This is calculator\n";
	a:
	cout<<"choose (+),(-)or(/) only\n";
	cin>>r;
	if(r=='+'||r=='-'||r=='/')
	{
		cout<<"Enter first number\n";
	    cin>>t;
	    cout<<"Enter second number\n";
	    cin>>s;
	    cout<<"Solution is: "<<calculator(t,s,r);
	    cout<<"\nDo you want onther operation\n";
	    cout<<"Yes=y  No=any key\n";
	    cin>>a;
	    if(agn(a))
	    goto a;
	    else
	    {
	    	cout<<"\n\nGoooood-bye\n\n";
	    	return 0;
		}
	}
	else
	goto a;
}
int calculator(int t,int s,char r)
{
	if(r=='+')
	return t+s;
	if(r=='-')
	return t-s;
	if(r=='/')
	return t/s;
}
bool agn(char a)
{
	if(a=='y')
	return true;
	else
	return false;
}

