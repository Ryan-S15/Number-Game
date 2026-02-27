#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0));

    int randomNum = rand() % 101;
    double guess = 0;
    int guessCount = 0;

    while (true) {
        cout << "Guess the random number: ";
        cin >> guess;

        if (cin.fail()) {
            cin.clear();
            cin.ignore(10000, '\n');
            cout << "Invalid input. Please enter a number between 0 and 100.\n";
            continue; 
        }

        guessCount++;

        if (guess == randomNum) {
            cout << "Your answer was correct ";
            cout << "in " << guessCount << " guesses.\n";
            break;
        } else {
            cout << "Your answer was wrong. ";

            if (guess < randomNum) {
                cout << "Too low!\n";
            } else {
                cout << "Too high!\n";
            }
        }
    }
	
    return 0;
}

    return 0;
}
