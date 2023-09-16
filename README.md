
from time import *
import random as r


def mistake(paratest, usertest): # paratest means paragraph test & usertest means jo user input karega uska test
    error = 0
    for i in range(len(paratest)):
        try:
            if paratest[i] != usertest[i]:
                error = error + 1
        except :
            error = error + 1
    return error
def speed_time(time_s, time_e, userinput):
    time_delay = time_e - time_s
    time_R= round(time_delay,2)
    speed = len(userinput)/time_R
    return round(speed)

while True:
    ck = input("Ready to test : yes / no: ")
    if ck == "yes":
        test = ["A paragraph is a self-controlled unit of discourse in writing dealing with a particular point or idea.",
                "My name is gayatri pradhan","Welcome to my world!!"]
        test1 = r.choice(test) # test se random line choose hoga
        print("      ***** Typing speed *****")
        print(test1)
        print() # give one line braek
        print() # one line break
        time_1 = time()
        testinput= input(" Enter: ")
        time_2= time()

        print('speed:',speed_time(time_1, time_2, testinput),"w/sec")
        print("Error : ",mistake(test1, testinput))
    elif ck =="no":
        print("Thank You")
        break
    else:
        print("Wrong input")
