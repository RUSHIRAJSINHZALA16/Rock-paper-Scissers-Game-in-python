# Rock-paper-Scissers-Game-in-python
import random
user_Wins=0
Computer_Wins=0

options=["rock","paper","scissers"]


while True:
    user_input = input("Type rock/paper/scissers or q to Quit: ").lower()
    if user_input=="q":
        break
       
    if user_input not in options:
        continue
    
    random_number= random.randint( 0, 2)

    computer_pick= options[random_number]
    print("Computer picked",computer_pick+'.')

    if user_input == computer_pick:
            print("GAME has be tied!")
    elif user_input == "rock" and computer_pick == "scissers":
            print("You wOn!")
            user_Wins +=1
    elif user_input == "paper" and computer_pick == "rock":
            print("You wOn!")
            user_Wins+=1 
    elif user_input == "scissers" and computer_pick == "paper":
            print("You wOn!")
            user_Wins +=1 
    else:
            print("You lost!")
            Computer_Wins+=1
            
            
print("You win", user_Wins,"Times")
print("The Computer won",Computer_Wins,"Times")
print("Goodbye!")
          
