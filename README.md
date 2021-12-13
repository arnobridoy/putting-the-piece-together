# putting-the-piece-together
A begineer program to Collected user data and make them modified to convert into a paragraph.
So there have been created a loop that user can push many string line inputs.
If user make a input like "\end", at the time the program will be break and output will be given.

For kind info, Output will be shown as Capitalized, Giving an "." for any simplier line , and if input line start with "who",
"whats","how" , Then it will be make an outputy that ends with "?"


The code are given bellow:


#A begineer program to Collected user data and make them modified to convert into a paragraph.
#Definin function to make lines Capitalized and interogatives
def sentence_maker(line):
    wh_ques = ('how','what','who')
    capitalized = line.capitalize()
    
    if line.startswith(wh_ques):
        return "{}?".format(capitalized)

    else:
        return "{}.".format(capitalized)    


#creating an empty list to gather all the data here
collected_data = []

#Creting an infinity loop to take all the input from user
while True:
    user_inp = input("say Something: ")

#Only if user enter \end, then the progam will be ended and provide the output    
    if user_inp == "\end":
        break

    else:
        collected_data.append(sentence_maker(user_inp))

#Printing the user data as a paragraph
print(' '.join(collected_data))        



