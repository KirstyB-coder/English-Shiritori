# This is a single player, English language version of the game Shiritori
import random


def main():
    instructions()
    user_initiates_game()
    game_play()


# instructions for the game
def instructions():
    print("This game is called Shiritori.")
    print("The computer gives you a starting word.")
    print("Please keep the chain going by typing a word that begins with the last letter of the previous word.")
    print("Don't use the same word twice.")
    print("")
    print("If you want to play press enter.")


# user initiates game
def user_initiates_game():
    initiates_game = input()


# game play
def game_play():

    # generate and print a random starting word
    words = ["time", "good", "person", "egg", "baby", "heart", "pasta", "animal", "star", "elephant"]
    random_index = random.randint(0, len(words)-1)
    print("This is your starting word:")
    print("")
    first_word = (words[random_index])
    print(first_word)
    print("")

    # creates list to hold words used in game
    game_list = []
    game_list.append(first_word)

    # solves fencepost problem
    answer = input("Enter your word: ")

    # while loop for continuous play, tests word fits rules of the game before continuing
    while answer[0] == game_list[-1][-1]:
        print("Great job, let's check it!")
        if answer in game_list:
            print("You already used this word, try again")
            answer = input("Enter another word: ")
        else:
            game_list.append(answer)
            answer = input("Enter your word: ")
    # the game ends when you lose
    else:
        print("Sorry, that's not right.")
        number_of_elements = len(game_list)
        print("Your chain is", number_of_elements-1, "words long.")
    print("Thanks for playing my awesome game today!")



if __name__ == '__main__':

    main()
