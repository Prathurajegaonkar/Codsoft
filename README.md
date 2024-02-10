# Codsoft
1st task :- Number Guessing Game using C++ programming language.

#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
   // Seed for random number generator
    srand(time(0)); 
    // Generate random number between 1 and 100
    int GuessNumber = rand() % 100 + 1; 
    int guess;
    int Number = 0;

    cout << "Welcome to the Guessing Game!" << endl;

    do {
        cout << "Enter Your Guess Number : ";
        cin >> guess;
        Number++;

        if (guess > GuessNumber) {
            cout << "Your Guessing Number is higher." << endl;
        } else if (guess < GuessNumber) {
            cout <<"Your Guessing Number is Lower." << endl;
        } else {
            cout << "You Win!!";
        }
    } while ( guess != GuessNumber );

    return 0;
}
