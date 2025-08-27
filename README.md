# ADVANCED PROGRAMMING Programming Assignment 1
This repository contains my work for **Programming Assignment 1** in ADVANCED PROGRAMMING, completed using Jupyter Notebook. 




**1. ALPHABET SOUP PROBLEM
**

def alphabet_soup(word):
    letters = list(word)                      # turn the word into a list of letters
    letters.sort()                            # sort the letters in the list alphabetically
    return "".join(letters)                   # compile lahat ng letters

print(alphabet_soup("hello"))
print(alphabet_soup("hacker"))



**2. EMOTICON PROBLEM
**

def emotify(sentence):
    d = {
        "smile": ":)", 
        "grin": ":D",
        "sad": ":((",
        "mad": ">:("
    }

    words = sentence.split()                  # split into list of words
    new_words = []                            # empty list para istore bagong version ng words

    for w in words:                           # go through each word one by one
        lw = w.lower()                        # make the word lowercase
        if lw in d:                           # check in dictionary
            new_words.append(d[lw])           # replace with emoticon
        else:
            new_words.append(w)               # retain orig. word pag wala sa dictionary

    return " ".join(new_words)                # compile lahat ng nasa new_words with spaces in between

print(emotify("Make me smile"))
print(emotify("I am mad"))



**3. UNPACKING LIST PROBLEM
**

lst = [1, 2, 3, 4, 5, 6]

first = lst[0]                                # take first item in the list (index 0 = 1)
middle = lst[1:-1]                            # take all items except yung first at yung last ([2,3,4,5])
last = lst[-1]                                # take last item in the list (index -1 = 6)

print("first:", first)                       
print("middle:", middle)
print("last:", last)
