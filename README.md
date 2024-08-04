# Vending Machine Program

This C++ program simulates a vending machine that allows users to select from different drinks and specify the quantity they want to purchase. It calculates the total bill and updates the remaining stock of each drink.

## Code

```cpp
#include<iostream>
using namespace std;

int main() {
    int drink, quant, t_coke = 10, t_pepsi = 15, t_sprite = 15, t_7UP = 25, bill;
    
    cout << "---Welcome to the Vending Machine---";
    cout << "\nWhich drink do you want to buy?";
    cout << "\nOption 1: Coke";
    cout << "\nOption 2: Pepsi";
    cout << "\nOption 3: Sprite";
    cout << "\nOption 4: 7UP";
    cout << "\nEnter your desired drink:";
    cin >> drink;
    
    switch(drink) {
        case 1:
            {
                cout << "\nEnter your desired quantity:";
                cin >> quant;
                if (quant <= t_coke) {
                    cout << "\nTotal number of Coke you have ordered = " << quant;
                    bill = quant * 5;
                    cout << "\nTotal bill = " << bill << "$";
                    t_coke -= quant;
                    cout << "\nNumber of Coke left = " << t_coke;
                } else {
                    cout << "\nMaximum available quantity has been ordered";
                }
            }
            break;
        case 2:
            {
                cout << "\nEnter your desired quantity:";
                cin >> quant;
                if (quant <= t_pepsi) {
                    cout << "\nTotal number of Pepsi you have ordered = " << quant;
                    bill = quant * 7;
                    cout << "\nTotal bill = " << bill << "$";
                    t_pepsi -= quant;
                    cout << "\nNumber of Pepsi left = " << t_pepsi;
                } else {
                    cout << "\nMaximum available quantity has been ordered";
                }
            }
            break;
        case 3:
            {
                cout << "\nEnter your desired quantity:";
                cin >> quant;
                if (quant <= t_sprite) {
                    cout << "\nTotal number of Sprite you have ordered = " << quant;
                    bill = quant * 7;
                    cout << "\nTotal bill = " << bill << "$";
                    t_sprite -= quant;
                    cout << "\nNumber of Sprite left = " << t_sprite;
                } else {
                    cout << "\nMaximum available quantity has been ordered";
                }
            }
            break;
        case 4:
            {
                cout << "\nEnter your desired quantity:";
                cin >> quant;
                if (quant <= t_7UP) {
                    cout << "\nTotal number of 7UP you have ordered = " << quant;
                    bill = quant * 3;
                    cout << "\nTotal bill = " << bill << "$";
                    t_7UP -= quant;
                    cout << "\nNumber of 7UP left = " << t_7UP;
                } else {
                    cout << "\nMaximum available quantity has been ordered";
                }
            }
            break;
        default:
            cout << "\nInvalid input";
    }
    
    cout << "\nAvailable drinks =\n" << "Coke = " << t_coke << "\n" << "Pepsi = " << t_pepsi << "\n" << "Sprite = " << t_sprite << "\n" << "7UP = " << t_7UP;
}
