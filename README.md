//# binary-compound-assignment-operators
//C++ Oop ,   binary compound assignment operators overloading for the reading pages and days.
#include<iostream>
#include<string>
using namespace std;
class Reading{
private:
	int days,pages;
public:
	void input(){
		cout<<"how many days  do you read : "<<endl;
		cin>>days;
		
		cout<<"how many pages do you read : "<<endl;
		cin>>pages;
	}
	void show(){
		cout<<"\tin \t "<<days<<"\tdays";cout<<"\tyou read "<<pages<<"\tpages"<<endl;	
		}
		
		void operator +=(Reading r){
		days=days+r.days;
		pages=pages+r.pages;	
		}
		
};


int main(){
	Reading r1,r2;
	r1.input();
	r2.input();
	
	r1.show();
	r2.show();
	
	r2+=r1;
	
	r2.show();
	
	return 0;
}
