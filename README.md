import random

def get_choice():
    while True:
        user = input("ENTER YOUR CHOICE: ")
        computer = ["stone", "paper", "scissors"]
        pasand = random.choice(computer)

        while(user != computer[0] and user != computer[1] and user != computer[2]):
            print("please enter the valid input!!")
            user = input("ENTER YOUR CHOICE: ")

        if(user == pasand):
            print(f"user choice: {user} computer: {pasand}")
            print("match Tie!!!")

        elif(user == "stone"):
            if(pasand == "paper"):
                print("paper ne pakad liya stone ko")
            else:
                print("stone ne todd diya scissors ko")

        elif(user == "paper"):    # Changed from "stone" to "paper"
            if(pasand == "scissors"):
                print("scissors ne paper ko cut kr diya")
            else:
                print("paper ne stone ko pakad liya")

        elif(user == "scissors"):   # Added missing case
            if(pasand == "stone"):
                print("stone ne scissors ko tod diya")
            else:
                print("scissors ne paper ko cut kr diya")

        break   # To stop the infinite loop

get_choice()
