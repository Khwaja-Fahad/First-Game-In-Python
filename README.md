import random as rnd

computer_win=0
user_win=0
options=["rock","paper","secissor"]

while True:
    user_pick=input("Enter Your Choice Rock/Paper/Secissor or want to Quit: ").lower()
    
    if user_pick =="quit":
        break
    
    if user_pick not in options:
        print("\n")
        continue
    
    random_number=rnd.randint(0,2)
    computer_pick=options[random_number]
    
    print("Computer Pick", computer_pick,".")
    
    if user_pick =="rock" and computer_pick =="secissor":
        print("You Won! \n")
        user_win +=1
    
    elif user_pick =="secissor" and computer_pick =="paper":
        print("You Won! \n")
        user_win +=1
    
    elif user_pick =="paper" and computer_pick =="rock":
        print("You Won! \n")
        user_win +=1
    
    elif user_pick =="rock" and computer_pick =="rock":
        print("\n")
        continue
    
    elif user_pick =="secissor" and computer_pick =="secissor":
        print("\n")
        continue
    
    elif user_pick =="paper" and computer_pick =="paper":
        print("\n")
        continue
    
        
    else:
        print("Computer Won! \n")
        computer_win +=1


print("You Won",user_win,"Times")
print("Computer Won",computer_win,"Times")
print("Good Bye")
