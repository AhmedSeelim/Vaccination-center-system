#include<iostream>
using namespace std;


//struct(data type) have attrbuts

struct patient //data type defined for patient
{
	string fname,lname;
	char gender;
	int age;
};




struct node     //to create linked list
{
	patient obj;//Obj - in struct node for data field of node in linked List.
	node *next;
};
node *head,*tail = NULL; // create null linked list it is constructor




class vaccine
{
	public:
	int a;//**
	
	
	
	
	void data_modification()  //function to add new entries, delete .
	{
		system("cls");
		int m;
		cout << "1. Add New Patient" << endl << "2. Delete Patient " << endl;	
	    cout << "Enter your Choice : ";
		cin >> m;                                          // created menu to add data
		
		switch(m)
		{
			case 1: 
		    if ( a > 0)    //checks vaccine count 
        		{
		        	add_new_patient();
			        a--;
	        	}
    		else
        		{ 
        			cout << "Vaccines are not Available" << endl;
        			addvaccine();
        		}
			break;
			case 2: 
			if(head == NULL)             //checks condition for emptiness 
     		{
    			cout << "No Data Available!" << endl;
    		}
    		else
    		{
    			delete_patient();
    		}
			
			break;
			default: 
			cout << "Error" << endl;
		}
		wait();
	}         
	
	
	
	
	void add_new_patient()  //function to add new entries called under add_data()
    	{
    	system("cls");
		patient p;//P- to deal with operation
		node *new_node,*last ;
		new_node= new node ;                           //declared pointer of type node
        cout << "Enter Full Name(Name and Surname) : ";
		cin >> p.fname >> p.lname;
		cout << "Enter Gender(M/F) : ";
		cin >> p.gender;
		cout << "Enter Age : ";
		cin >> p.age;

		
		new_node -> obj = p;                                  //added data to obj patient                              //set next null to set temp as last node in list
		
		if(head == NULL)                                  //checks null list and set head and tail as 1st node of list
			{
				head = new_node;
				new_node -> next = NULL;
			}
			else                                  //if not empty, set next field of tail to temp it will pass address of new node to tail node
			{
				last = head;
				while(last -> next !=NULL){
					last=last -> next; }
				last -> next =	new_node;
				new_node ->next = NULL;
			}
			cout << "Patient Added Succesfully........" << endl;
    	}
    
    
    
    
	void delete_patient()  
	{
		system("cls");
		patient a;
		cout << "Enter Full Name(Name and Surname) : ";
		cin >> a.fname ;
		node *current,*previous;              //defined to node pointers
		current = head;
		previous=head;
		if(current -> obj.fname == a.fname)         //condition for one node
		{
			head = current -> next ;
			cout << "Deleted patient is : " << current -> obj.fname << endl;
			delete(current);
		}
		else
		{
			while(current -> obj.fname != a.fname)     //loop to traverse through list till last node arrives
			{
			previous = current;                 
			current = current -> next;       //moves temp node to next node
		    }
		    previous -> next = current -> next;        //second last node will point to null
		    cout << "Deleted patient is : " << current -> obj.fname << " " << current -> obj.lname << endl;
		    delete(current);
		}
		wait();
	}	
    	
	
	
	
	void view_data()  //function to view stock of vaccines, full patients data.
	{
		int v;
		system("cls");
		cout << "Press" << endl;
		cout << "1. Add New Vaccines" << endl << "2. View available number of vaccines" << endl << "3. View all Data" << endl;	
	    cout << "Enter your Choice : ";
		cin >> v;
		switch(v)
		{
			case 1: addvaccine();
			break;
			case 2: viewvaccine();
			break;
			case 3: display();
			break;
			default: 
			cout << "Error" << endl;
		}
		wait();	
	}  
	
	
	
	
	void viewvaccine()  //function to view vaccine stock.
	{
		system("cls");
		cout << "Available Number of Vaccines: " << a << endl;

	} 
	
	
	
	
	void addvaccine()  //function to add vaccine stock.
	{
		system("cls");
		a = 0;
		cout << "Enter Number of Vaccines: ";
		cin >> a;
		cout << "Available Vaccines are: " << a << endl;
	}
	
	
	
	
	void wait()  //function for creating "press any key to continue.."
	{
		char x;
		cout << "Press any key to continue : " << endl;
		cin >> x;
		switch(x)
		{
			default:
			system("cls");	
		}
	}
	
	
	
	
	void display()  //function to display full patients data.
    	{
    	system("cls");
		cout <<"\tName"<<"\t\t\tGENDER"<<"\t AGE"<< endl;
		node *current;
			if(head == NULL)
			{
				cout << "List is Empty!!!" << endl;
			}
			else
			{
			    current = head;
				while(current != NULL)     //loop to traverse through list till it arrives last node
				{
					cout <<"\t" << current -> obj.fname << " " << current -> obj.lname;
					cout << "\t\t"<< current -> obj.gender << "" ;
					cout << "\t"<< current -> obj.age << ""<< endl ;
					current = current -> next;
				}
				cout << endl;
			}
    	}     
	
	
	
	
	void search_data()  //function to search patients data.
   {
     system("cls");
     cout<<"Enter the patient name: ";
     string name;
     cin>>name;
     node* current=head;
     int position=1;
     while(current !=NULL)
      {
	    if(current->obj.fname == name)
        cout<< position<<" /n";
        current=current->next;
        position+=1;
      }
      wait();
    }
};



int main()
{
	vaccine a;                 //object of class
	int choice,i;
	a.addvaccine();            //to add vaccine at start


	while(1)
	{
		system("cls");
		cout << endl;
		cout << "Press: " << endl;
		cout << "1. data_modification" << endl << "2. View Data" << endl << "3. Search" << endl << "4. Exit" << endl;	
	    cout << "Enter your Choice : ";
		cin >> choice;
		
		switch(choice)
		{
			case 1: a.data_modification();
			break;
			case 2: a.view_data();
			break;
			case 3: a.search_data();
			break;
			default:
				exit(0);
		}
    }
	return 0;
}

