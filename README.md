// TASK 1
#include <iostream>
#include <ranges>
using namespace std;
string repeat (int a) {
    if (a > 0) {
        string s = " + 1";
        string rez;
        for (int i = 0; i < a; i++){
            rez += s;
        }
        return rez;
    }
    if ( a ==0 ){return " ";}
}


int schet(int a) {
    int c = a;
    while (a > 0) {
        for (int i = 0; i != a; i++) {
            int h = c - i;
            cout << h <<repeat(i) << endl;
        }
    return 0;}
}

int main() {
    int n ;
    cout << "Enter a number : ";
    cin>>n;
    schet(n);

}
