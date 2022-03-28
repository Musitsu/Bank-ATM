# Bank-ATM
import datetime

user1 = {"Username": {"1": "Hellen", "2": "Eugene", "3": "victor"},
         "PIN": {"1": 0000, "2": 1234, "3": 7896}, "balance": {"1": 50000, "2": 60000, "3": 2500}
         }
Trials = 3
pin1 = user1["PIN"]["1"]
pin2 = user1["PIN"]["2"]
global user_balance
global user_name
if pin1:
    user_balance = user1["balance"]["1"]
    user_name = user1["Username"]["1"]
if pin2:
    user_balance = user1["balance"]["2"]
    user_name = user1["Username"]["2"]


def withdrawing():
    global user_balance
    if pin1:
        user_balance = user1["balance"]["1"]
    withdraw = int(input('Enter the amount you wish to withdraw:\n '))
    user_balance -= withdraw
    print('Your account balance is {}'.format(user_balance))


def receipt():
    global user_name
    receipts = input("Would you like a receipt for your transaction?y/n:\n ")
    if receipts == "y":
        print(user_name)
        print('Your account balance is {}'.format(user_balance))
        print(datetime.datetime.now())


print("Welcome to Sierra Bank")
while Trials != 0:
    pin = int(input('Enter your pin number:\n '))
    if pin == pin1 or pin2:
        option = input('w: withdraw or b: balance:\n ')
        if option == 'w':
            withdrawing()

            option2 = input("Would you wish to withdraw again?y/n :\n")
            if option2 == "y":
                withdrawing()
                receipt()
                print("Thank you for using Sierra Bank")
                break
            else:
                receipt()
                print("Thank you for using Sierra Bank")
                break
        else:
            print('Your account balance is {}'.format(user1["balance"]))
            receipt()
            print("Thank you for using Sierra Bank")
            break
    else:
        Trials -= 1
        print('wrong pin, you have ', Trials, ' more trials remaining')
        if Trials == 0:
            print('Your account has been temporarily locked, please visit your branch')
import datetimeuser1 = {"Username": {"1": "Hellen", "2": "Eugene", "3": "victor"},"PIN": {"1": 0000, "2": 1234, "3": 7896}, "balance": {"1": 50000, "2": 60000, "3": 2500}}Trials = 3pin1 = user1["PIN"]["1"]pin2 = user1["PIN"]["2"]global user_balanceglobal user_nameif pin1:user_balance = user1["balance"]["1"]user_name = user1["Username"]["1"]if pin2:user_balance = user1["balance"]["2"]user_name = user1["Username"]["2"]def withdrawing():global user_balanceif pin1:user_balance = user1["balance"]["1"]withdraw = int(input('Enter the amount you wish to withdraw:\n '))user_balance -= withdrawprint('Your account balance is {}'.format(user_balance))def receipt():global user_namereceipts = input("Would you like a receipt for your transaction?y/n:\n ")if receipts == "y":print(user_name)print('Your account balance is {}'.format(user_balance))print(datetime.datetime.now())print("Welcome to Sierra Bank")while Trials != 0:pin = int(input('Enter your pin number:\n '))if pin == pin1 or pin2:option = input('w: withdraw or b: balance:\n ')if option == 'w':withdrawing()option2 = input("Would you wish to withdraw again?y/n :\n")if option2 == "y":withdrawing()receipt()print("Thank you for using Sierra Bank")breakelse:receipt()print("Thank you for using Sierra Bank")breakelse:print('Your account balance is {}'.format(user1["balance"]))receipt()print("Thank you for using Sierra Bank")breakelse:Trials -= 1print('wrong pin, you have ', Trials, ' more trials remaining')if Trials == 0:print('Your account has been temporarily locked, please visit your branch')



