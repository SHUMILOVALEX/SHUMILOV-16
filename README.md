// TASK 1
#include <iostream>
using namespace std;

int proverka(int a) {
    bool flag = true;
    while (flag) {
        for (int i = 1; i < a; i++) {
            int otvet = a - i; //main natur
            cout << a << " = " << otvet << " + ";
            if (otvet != a + 1) {
                // ostatok if  a - main natur
                int ostat = a - otvet;
                cout << ostat;
                cout << endl;
                string rokstar = "";
                while (ostat != 1) {
                    ostat--;
                    string dobavka = " + 1";
                    rokstar += dobavka;
                    string blackstar = to_string(ostat) + rokstar;
                    cout << a << " = " << otvet << " + " << blackstar << endl;
                }
            }
        }
        flag = false;
    }
}

int main() {
    proverka(10);
}

// Task 2
#include <iostream>
using namespace std;

int main() {
    int a[] = {10, 9, 2, 5, 3, 7, 101, 1234, 18};
    int size = sizeof(a) / sizeof(a[0]);
    int schetchik = 2;
    int sum = 0;
    for (int i = 0; i < size; i++) {
        for (int j = 1; j < size; j++) {
            if ((a[i] < a[j]) && (a[j] < a[j + 1])) {
                schetchik++;
            }
        }
        if (schetchik > sum) {
            sum = schetchik;
            schetchik = 2;
        } else { schetchik = 2; }
    }
    cout << sum << endl;
}

// Task 3
#include <iostream>
using namespace std;

int razmen(int a) {
    bool flag = true;
    const int constanta = a;
    cout << a << " = ";
    while (flag) {
        if (a >= 0) {
            if (a - 5 > 0) {
                cout << "5 + ";
                a = a - 5;
            } else if (a - 5 == 0) {
                cout << "5 ";
                a = a - 5;
            } else if (a - 2 > 0) {
                cout << "2 + ";
                a = a - 2;
            } else if (a - 2 == 0) {
                cout << "2 ";
                a = a - 2;
            } else if (a - 1 > 0) {
                cout << "1 + ";
                a = a - 1;
            } else if (a - 1 == 0) {
                a = a - 1;
                cout << "1 ";
            }
        } else { flag = false; }
    }
}

int main() {
    int a = 11;
    razmen(a);
}
