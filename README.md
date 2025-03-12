# Divisible
#include <iostream>
#include <string>
using namespace std;

int main() {
    int testnumb;
    cin >> testnumb;
    cin.ignore();  // Ignorowanie znaku nowej linii po liczbie

    string numbers;
    getline(cin, numbers);

    int suma = 0;
    int digitCount = 0;

    for (char ch : numbers) {
        if (ch != ' ') {
            int num = ch - '0';  // Konwersja z char na int
            if (num != 0 && testnumb % num == 0) {  // Sprawdzamy, czy nie dzielimy przez 0
                suma++;
            }
            digitCount++;
        }
    }

    if (suma == digitCount) {
        cout << "divisible by all";
    } else {
        cout << "not divisible by all";
    }

    return 0;
}
