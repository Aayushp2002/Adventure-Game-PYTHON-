# Adventure-Game-PYTHON-
# Adventure game where the user's goal is to survive until the mission ends.


print("Welcome to my game! Have fun!")
yourName=input("Hello, what is your name? ").lower()
yourAge=int(input("What is your age? "))
print("Hello ",yourName," you are ",yourAge," years old")
healthOfTheUser=100

if yourAge >= 18:
    print("Your age is valid to play this game")
    wantToPlay=input("Do you want to play this game? ").lower()
    if wantToPlay=="yes":
        print("Let's play!")
        print("You will start the game with ",healthOfTheUser," health")
        leftOrRight=input("Do you want to go left or right?(left or right) ").lower()
        if leftOrRight=="right":
            ansOfLeftOrRight=input("After a right turn, you found a river. Do you want to swim through the river or go across it?(across or swim) ").lower()
            if ansOfLeftOrRight=="across":
                print("While walking by going across, you found an apple. You were hungry and ate the apple. The apple was poisonous and you died. Better luck next time!")




            elif ansOfLeftOrRight=="swim":
                print("You reached the other side of the river. However, you were bitten by a fish so you lost 50 health")
                healthOfTheUser-=50
                nextQ=input("After you crossed the river, you see a house and a cave. Where would you go?(house or cave) ").lower()
                if nextQ=="house":
                    print("You went inside the house and greeted the owner. The owner did not know you so he hit you with a stick. For that reason you lost 50 health")
                    healthOfTheUser-=25
                    if healthOfTheUser <=0:
                        print("Your health is 0. You lost the game. Better luck next time.")

                    else:
                        print("You survived the game! You won!")


                else:
                    print("You went inside the cave and there was a hungry lion sitting. The lion saw you and he ate you. You lost all your health and died!")

            
            else:
                print("I am sorry! You lost the game")

            




        else:
            print("For you left was unlucky. Sorry, you died")

    






    else:
        print("Have a nice day")

else:
    print("Your age is not valid to play this game")

