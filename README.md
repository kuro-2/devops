"""import sys
class Bank:
    def __init__(self, name, balance=0.0):
        self.name = name
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount 
    

name = input("Enter Name:")
b = Bank(name)  # b is the instance of Bank class
pin = int(input("Enter pin:"))
if pin == 1234:
    while (True):
        print("Select your option")
        print("\t\t\t\t1.Exit")
        print("\t\t\t\t2.Deposit")
        print("\t\t\t\t3.Withdraw")
        print("\t\t\t\t4.Transfer")
        print("\t\t\t\t5.Transactions_History")
        choice = int(input())
        if choice==1:
            sys.exit()
        # amount for deposit or withdraw
        amt = float(input("Enter Amount"))
        # do the transaction
        if choice == 2:
            print("Balance after Withdrawal:", b.deposit(amt))
        elif choice == 3:
            print("Balance after Withdrawal:", b.withdraw(amt))
        elif choice == 4:
            b.Transfer()
        elif choice == 5:
            b.Transactions_History()


else:
    print("Enter valid pin")"""

from tkinter import*
from tkinter import ttk
import tkinter.messagebox

class atm:
    def __inti__(self,root):
        self.root = root
        blank_space = " "
        self.root.title(110 * blank_space + "ATM System")
        self.root.geometry("775x760+280+0")
        self.root.configure(background ='gainsboro')

        MainFrame = Frame(self.root, bd=20, width=784, height=700, relief=RIDGE)
        MainFrame.grid()

        TopFrame1 = Frame(MainFrame, bd=7, width=784, height=700,relief=RIDGE)
        TopFrame1.grid(row=1, column = 0, padx = 12)

        TopFrame2 = Frame(MainFrame, bd=7, width=784, height=700, relief=RIDGE)
        TopFrame2.grid(row=0, column = 0, padx = 8)

        TopFrame2Left = Frame(MainFrame, bd=5, width=784, height=700, relief=RIDGE)
        TopFrame2Left.grid(row=0, column=0, padx=8)

        TopFrame2Mid = Frame(MainFrame, bd=7, width=784, height=700, relief=RIDGE)
        TopFrame2Mid.grid(row=0, column=1, padx=8)

        TopFrame2Right = Frame(MainFrame, bd=7, width=784, height=700, relief=RIDGE)
        TopFrame2Right.grid(row=0, column=2, padx=8)


if __name__=='main__':
    root = Tk()
    application = atm(root)
    root.mainloop()

