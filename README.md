#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
	srand(time(0));
// variables for the number inputs and outputs
	int playerguess;
	int randomnubmer = rand() % 101;
	int guessCount = 0; // Counts the guesses

// input for the player at the start of the game
	cout << "Enter your guess\n";
	cin >> playerguess;
	guessCount++;     // Counts the first guess

	// code for the loop of the game, It'lrepeat until the player guesses the correctly
	while (playerguess != randomnubmer) {
		cout << "incorrect try again\n";
		cin >> playerguess;
		guessCount++; //Counting each guess
	}
	// When the player guesses the correct nubmer this message appears.
	cout << "Correct!!!!\n";
	cout << " It took you " << guessCount << " guesses.\n" ;

	return 0;
}
