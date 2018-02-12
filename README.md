#include <iostream>

using namespace std;

int main()
{
    cout << "\t\t\t\t\t\tWelcome to the 100 Game\t\t\t\t\t" << endl;
    int P1;
    int P2;
    string P1Name;
    string P2Name;
    int score;
    score = 0;

    cout << "Player 1,please enter your name:" << endl;
    cin >> P1Name;
    cout << "Player 2,please enter your name:"<<endl;
    cin >> P2Name;

    while (score != 100 ){
        cout << P1Name <<" :enter a number between 1 and 9" << endl;
        cin >> P1;
        while( true ){
            if ( P1 >= 10 ){
                cout << "Invalid number \nPlease enter a number between 1 and 9" << endl;
                cin >> P1;
            }
            else{
                break;
            }
        }

        score = score+P1;
        if (score == 100){
            cout << P1Name << ": YOU WON!" << endl;
            break;
        }else{
            cout << P2Name << " :enter a number between 1 and 9" << endl;
            cin >> P2;
            while (true){
                if (P2>=10){
                cout << "Invalid number \nPlease enter a number between 1 and 9" << endl;
                cin >> P2;
                }
                else{
                    break;
                }
            }
        }
        score = score+P2;
        if (score == 100){
            cout << P2Name << ": YOU WON!" << endl;
            break;
        }
        if ( score > 100 ){
            cout<<"GAME OVER! \nYou passed the goal \nThere's no winner!!";
            break;
        }
    }
    return 0;
}
