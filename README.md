// 
// 
// 04-06-2018
// Assignment #7
// This program demonstrates a virtual library database made with classes

#include <iostream>
#include <string>
#include <vector>
#include <fstream>

using namespace std;

class Name{
public:
    Name(); //constructor

    string GetFirst() {return First;} // accessor
    void SetFirst(string f){First = f;} // mutator

    string GetLast() {return Last;} // accessor
    void SetLast(string l) {Last = l;} // mutator

    ~Name() {}; // destroyer/deconstructor/destructor
private:
    string First;
    string Last;
};

class Date{
public:
    Date(); // default constructor
    int GetYear() const {return Year;} // accessor
    void SetYear(int y) {Year = y;} // mutator

    int GetMonth() const {return Month;} // accessor
    void SetMonth(int m) {Month = m;} // mutator

    int GetDay() const {return Day;} // accessor
    void SetDay(int d) {Day = d;} // mutator

    ~Date() {};
private:
    int Year;
    int Month;
    int Day;
};

class Book{
public:
    Book();
    Name GetAuthor() const {return Author;} // accessor
    void SetAuthor(Name a) {Author = a;} // mutator

    string GetTitle() const {return Title;} // accessor
    void SetTitle(string t) {Title = t;} // mutator

    int GetYear() const {return Year;} // accessor
    void SetYear(int y) {Year = y;} // mutator

    ~Book() {};
private:
    Name Author;
    string Title;
    int Year;
};

class libraryBook {
public:
    libraryBook() {}
    int GetId() const {return id;}
    void SetId(int i) {id = i;}
    
    Book GetBook() const {return book;}
    void SetBook(Book b) {book = b;}
    
    Name Getborrower() const {return borrower;}
    void Setborrower(Name bo) {borrower = bo;}
    
    Date Getborrowed() const {return borrowed;}
    void Setborrowed(Date bo) {borrowed = bo;}
    
    Date Getdue() const {return due;}
    void Setdue(Date d) {due = d;}
    
    bool GetisLoaned() const {return isLoaned;}
    void SetisLoaned(bool is) {isLoaned =is;}

    ~libraryBook() {};
private:
    int id;
    Book book;
    Name borrower;
    Date borrowed;
    Date due;
    bool isLoaned;
};




int main(){

    vector<libraryBook> bookList;
    string line;
    ifstream infile; 
    infile.open ("bookList");
    if(infile.good()){
    
    	int	i=1;
    	libraryBook lb;
    	Book book;
    	
    	while(getline(infile, line)){
    		
    		
    		switch(i)
    			case 1:
    					
    		
    		};
   
    }

return 0;
}
