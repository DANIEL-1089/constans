#include <iostream>
#include <cstdlib>
#include <ctime>
#include <wchar.h>
#include <Windows.h>
#include <algorithm>
#include <vector>
#include <string>
#include <conio.h>



using namespace std;
class Distance {
private:
    int feet;
    float inches;
public:
    Distance(int ft, float in) : feet(ft), inches(in)
    {}
    void getdist() //method not constant
    {
        cout << "\nEnter a number of feet: ";cin >> feet;
        cout << "\nEnter a number of inches: ";cin >> inches;
    }
    void showdist() const {
        cout << feet << "\'-" << inches << '\'';
    }
};


int main()
{
    const Distance football(300, 0);
    //football.getdist()  //mistake: method getdist() isn`t constant
    cout << "The field lenght is: ";
    football.showdist();
    cout << endl;


    return 0;
}
