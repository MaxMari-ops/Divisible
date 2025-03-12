#include<iostream>
using namespace std;

int main()
{
	int liczba_testow;
	cout<< "Podaj liczbe testow:"<<endl;
	cin>> liczba_testow;
	cout<< " " <<endl;
	
	for(int i=0; i< liczba_testow; i++)
	{
		cout<<"Test" <<" "<< i+1 <<endl;
		int l_kolumn;
		cout<< "Podaj liczbe kolumn mniejsza niz 20:"<<endl;
		cin>> l_kolumn;
		
		if(l_kolumn<20)
		{
		  int l_klockow[l_kolumn];
		  int suma_klockow = 0;
		
		  cout<< "Podaj liczbe klockow w kolumnach:"<<endl;
		  for(int j=0; j<l_kolumn; j++)
		  {
			cin>> l_klockow[j];
			suma_klockow += l_klockow[j];
	      }
			
		  if(suma_klockow % l_kolumn==0)
		  {
			int klocki_do_przeloz=0;
			for(int j=0; j<l_kolumn; j++)
			{
			  if(l_klockow[j] > (suma_klockow/l_kolumn))
			  klocki_do_przeloz+= (l_klockow[j]- (suma_klockow/l_kolumn));
		    }
		    cout<< "Minimalna liczba klockow do przelozenia :" << " " << klocki_do_przeloz<<endl;
		  }
		  else cout<< "Suma klockow jest niepodzielna przez liczbe kolumn"<< endl;
	    }
	    else cout<< "Liczba kolumn jest za duza"<<endl;
	    
	cout<< " " <<endl;
	
    }
    return 0;
}
