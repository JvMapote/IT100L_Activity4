import datetime
#Jayvee N Mapote
#Activity 4
#A11
def ending():
    exit()
def Age():
    a = str(input("enter name: "))
    b = int(input("enter Age: "))
    y = int(datetime.datetime.now().strftime("%Y"))
    x = y-b
    z = 100 - b + y
    k = z - y
    message = 'Hello %s, you are currently %d years old\nYou were born on %d\nBy %d you will be 100 years old\nYou will have to wait %d years to be 100 years old' %(a,b,x,z,k)
    print(" ")
    print(message)
def Voting():
    a = str(input("enter Fullname: "))
    b = int(input("Enter Birthyear: "))
    y = int(datetime.datetime.now().strftime("%Y"))
    x = y-b
    z = x - 6

    if x >= 18 and z>=18:
        print('\nHi %s. You can vote for the 2016 Presidential elections.' %(a))
    elif x >= 18 and z < 18:
        print('\nHi %s. You can vote for the 2022 Presidential elections.' %(a))
    else:
        print('\nHi %s. You can’t vote yet for both elections. Register on Year' %(a))
def Grading_System():
    try:
        name = str(input("enter Name: "))
        prelim = int(input("enter Prelim Grade: "))
        if prelim > 0 and prelim <= 100:
            midterm = int(input("enter Midterm Grade: "))
            if midterm > 0 and midterm <= 100:
                finals = int(input("enter finals Grade: "))
                if finals > 0 and finals <= 100:
                    quizes1 = int(input("enter Quiz1 Grade: "))
                    if quizes1 > 0 and quizes1 <= 50:
                        quizes2 = int(input("enter Quiz2 Grade: "))
                        if quizes2 > 0 and quizes2 <= 50:
                            quizes3 = int(input("enter Quiz3 Grade: "))
                            if quizes3 > 0 and quizes3 <= 50:
                                ass1 = int(input("enter Assignment1 Grade: "))
                                if ass1 > 0 and ass1 <= 25:
                                    ass2 = int(input("enter Assignment2 Grade: "))
                                else:
                                    raise ValueError
                            else:
                                raise ValueError
                        else:
                            raise ValueError
                    else:
                        raise ValueError
                else:
                    raise ValueError
            else:
                raise ValueError
        else:
            raise ValueError
        

    except ValueError:
            print("\nYou entered wrong value!")
    
    try:
        exam1 = (prelim/100)*20
        exam2 = (midterm/100)*20
        exam3 = (finals/100)*20
        quiz1 = (quizes1/50)*10
        quiz2 = (quizes2/50)*10
        quiz3 = (quizes3/50)*10
        assignment1 = (ass1/25)*5
        assignment2 = (ass2/25)*5
        x = (exam1+exam2+exam3+quiz1+quiz2+quiz3+assignment1+assignment2)

        if x > 96 and x <= 100:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 1.00. You Passed the course.' %(name, x))
        elif x >= 91.51 and x <= 96:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 1.25. You Passed the course.' %(name, x))
        elif x >= 87.01 and x <= 91.50:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 1.50. You Passed the course.' %(name, x))
        elif x >= 82.51 and x <=87:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 1.75. You Passed the course.' %(name, x))
        elif x >= 78.01 and x <= 82.50:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 2.00. You Passed the course.' %(name, x))
        elif x >= 73.51 and x <= 78:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 2.25. You Passed the course.' %(name, x))
        elif x >= 69.01 and x <= 73.50:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 2.50. You Passed the course.' %(name, x))
        elif x >= 64.51 and x <= 69:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 2.75. You Passed the course.' %(name, x))
        elif x >= 60 and x <= 64.50:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 3.00. You Passed the course.' %(name, x))
        elif x < 60:
            print('\nHi %s. Your final grade is %d. Your equivalent grade is 5.00. You failed the course.' %(name, x))
        else:
            print("error")
    except:
        print("\n\n")
        Grading_System()

while True:
    print(
          "1. Activity 1 - 4\n" +
          "2. Activity 2 – 1\n" +
          "3. Activity 2 - 3\n" +
          "Type [End] to quit\n")

    selection = input("Enter Selection: ")
    
    print()
#The selection from the program
    {"1":Age,
     "2":Voting,
     "3":Grading_System,
     "End":ending
    }[selection]()
    
    print()