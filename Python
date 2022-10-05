"""This is a program for a chatbot which helps to play HANGMAN.
   1.The bot will start with the greetings at first the bot intoduces itself
     and describes what it will do.
   2.After that bot asks the name of the user and it greets the user and it welcomes user.
   3.The bot first welcomes you by representing a hangman.
   4.In this game the bot picks a random word from the words file which is called as quess word.And then
     bot asks to enter the the random guess letters.If the guess letter matches any letter in the guess word
     the it asks for next one to match.If not the user enters the quess letter which in not in the quess word
     then the hangman starts hanging by adding each part in step by step manner.
   5.If the hangman is fully hanged with all parts then the game is Over.We cannot try any more after that.
   6.Else if Hangman is not completely hanged the we have chances to correctly guess the letters which matches
     the guess word.If we guessed the word correctly then we will win the gam if not
     we lose the game.
"""
import random
import time 
from time import sleep
from words import word_list
import datetime
time=datetime.datetime.now().hour
def greetings():
    print()
    msg=["Hey there!! I am a bot.I am here to have fun together by playing Hangman",
         "Hello!! I am a bot .You can play Hangman game(Guess the word) with me.Let's play together and have fun!!!"]
    print(random.choice(msg))
    print()
def ask_name():
    l=["⭐⭐⭐"+" "+"Very excited to play with you! what is your name"+"❔","⭐⭐⭐"+"Very excited to play with you! may i know your name"+"❔"]
    print("====================================================================================")
    print()
    print(random.choice(l))
    print()
def Introduce(name):
    if(time<12):
        greeting="Good Morning😃"
    elif(time<18):
        greeting="Good Afternoon🙂"
    else:
        greeting="Good Night! It's high time to play😴"
    print("{}".format(greeting)+" "+name+" "+"!!!"+"Glad to meet you.Let's play our Game")
def welcome_you():
    print()
    print("----Welcome to Hangman----")
    print()
    print("    I AM A HANGMAN   ")
    print()
    print('   ',  '------')
    print('   ',  '|    |')
    print('   ',  '|    O')
    print('   ',  '|   -|-')
    print('   ',  '|    |')
    print('   ',  '|   / \\')
    print('------------')
    sleep(4)
guess_word = random.choice(word_list).lower()
def print_guessword(guess_word):
    print("Let me pick a word")
    print()
    sleep(4)
    print("Okay I've got it!..")
    print()
    sleep(4)
    print("The word has", len(guess_word), "letters")
#for creating empty guessword
    for i in range(len(guess_word)):
        print('_',' ', end = "")
    print()
#list to store matched letters
correct_letters=["_"]*len(guess_word)
#list to store unmatched letters
wrong_letters=[]
#creating hangman parts
def Hangman_parts(x):
    if x == 0:
        print("---------"+"Hangman at this position"+"-------")
        print('   ',  '------')
        print('   ',  '|    |')
        print('   ',  '|     ')
        print('   ',  '|     ')
        print('   ',  '|     ')
        print('   ',  '|     ')
        print('------------')
    if x == 1:
        print()
        print("---------"+"Hangman at this position"+"-------")
        print('   ',  '------')
        print('   ',  '|    |')
        print('   ',  '|     ')
        print('   ',  '|     ')
        print('   ',  '|     ')
        print('   ',  '|     ')
        print('------------')
        print()
    if x == 2:
        print()
        print("---------"+"Hangman at this position"+"-------")
        print('   ',  '------')
        print('   ',  '|    |')
        print('   ',  '|    O')
        print('   ',  '|   -|-')
        print('   ',  '|     ')
        print('   ',  '|     ')
        print('------------')
        print()
    if x == 3:
        print()
        print("---------"+"Hangman at this position"+"-------")
        print('   ',  '------')
        print('   ',  '|    |')
        print('   ',  '|    O')
        print('   ',  '|   -|-')
        print('   ',  '|    | ')
        print('   ',  '|     ')
        print('------------')
        print()
    if x == 4:
        print()
        print("---------"+"Hangman at this position"+"-------")
        print('   ',  '------')
        print('   ',  '|    |')
        print('   ',  '|    O')
        print('   ',  '|   -|-')
        print('   ',  '|    | ')
        print('   ',  '|   / \\')
        print('------------')
        print()
#for printing matched letters in the guessword
def add_correctletters():
    for i in correct_letters:
        print(i,end=" ")
    print()
#for printing unmatched letters in the guessword
def add_wrongletters():
    for i in wrong_letters:
        print(i,end=" ")
    print()
def play_game():
    while (True):
        print()
        guess_letter = input("Guess a letter ☞ : ").lower()
        print()
        if guess_letter in guess_word:
            print("Let me check")
            sleep(3)
            print()
            index = 0
            for i in guess_word:
                if(i==guess_letter):
                    correct_letters[index]=guess_letter
                index=index+1
            print(">>>>>>> The matched letters are :"+" ")
            print()
            add_correctletters()
            print()
            Hangman_parts(len(wrong_letters))
        elif (guess_letter not in guess_word):
            print("Let me check !!")
            sleep(3)
            print()
            if guess_letter in wrong_letters:
                print("<<<You already guessed this letter>>>", guess_letter)
                print()
            else:
                print(guess_letter, "is not in my word")
                print()
                wrong_letters.append(guess_letter)
                print(">>>>>> Matched letters are :"+" ")
                print()
                add_correctletters()
                print()
                Hangman_parts(len(wrong_letters))
        if("_" not in correct_letters):
            print("Congratulations !!!"+" "+"👏👏👏"+"   You guessed it!")
            print()
            for i in range(len(guess_word)):
                print("✅",end=" ")
            print()
            print()
            print("The picked word is"+"->"+ guess_word.upper())
            print()
            print("THANK YOU FOR PLAYING HANGMAN")
            print()
            break
        if(len(wrong_letters)>4):
            print("Ohhh!! GAME OVER ...."+" YOU LOST")
            print()
            print("=======================================================================")
            print()
            print("I picked", guess_word.upper())
            print()
            print("THANK YOU FOR PLAYING HANGMAN")
            print()
            break
def bot():
    greetings()
    ask_name()
    name=input("Enter your name "+":"+" ")
    Introduce(name)
    welcome_you()
    print_guessword(guess_word)
    play_game()
bot()
