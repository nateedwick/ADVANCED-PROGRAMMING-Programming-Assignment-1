# ADVANCED PROGRAMMING: Programming Assignment 1

## Project Overview  
This project contains solutions to basic Python programming problems as part of **Advanced Programming Assignment 1**.  
It demonstrates how to identify, apply, and combine different Python codes and functions to solve problems. 
The problems cover essential concepts such as string manipulation, dictionary lookups, and list operations.  

## Getting Started
The code can be run in any Python environment or IDE. For this project, **Jupyter Notebook** was used through Anaconda Navigator to write and execute the solutions.  

## Problems and Solutions

### 1. Alphabet Soup Problem  
- **Goal:** Create a function that takes a string and returns a string with its lettersin alphabetical order.

- **Code:**  Create a function named alphabet_soup with a parameter called "word". Transform the input "word" into a list of letters, sort them alphabetically with the sort( ) function, and join them back together with the join( ) function.
  ```python
  def alphabet_soup(word):
      letters = list(word)                      # turn the word into a list of letters
      letters.sort()                            # sort the letters in the list alphabetically
      return "".join(letters)                   # compile lahat ng letters
  
- **Output:**
  ```python
      print(alphabet_soup("hello"))   # ehllo
      print(alphabet_soup("hacker"))  # acehkr

> ehllo\
> acehkr

 ### 2. Emoticon Problem 
- **Goal:** Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad and mad with their corresponding emoticons.
- **Code:** Create a function called emotify( ) with one parameter called sentence. Inside the function, store a dictionary d that contains the words smile, grin, sad, and mad as keys, and their corresponding emoticons :), :D, :((, and >:( as values. Use the split( ) function to separate the sentence into individual words and save them in a list called words. Prepare an empty list new_words to store the modified words. Create a for loop to go through each word in words. In every iteration, convert the word into lowercase using the lower( ) function and check if it exists as a key in the dictionary d. If it matches, append its corresponding emoticon to new_words. If not, append the original word. After the loop finishes, use " ".join(new_words) to combine all elements of new_words into a single string, separating them with spaces. This returns the new sentence where the specific words have been replaced with their emoticons, while all other words retain their original case.


  ```python
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

    return " ".join(new_words)                # compile lahat ng nasa new_words with spaces in between\

- **Output:**
  ```python
  print(emotify("Make me smile"))   # Make me :)
  print(emotify("I am mad"))        # I am >:(

> Make me :)\
> I am >:(

### 3. Unpacking List Problem
- **Goal:** Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.
- **Code:**  Create a list called lst that contains several numbers. To unpack it, assign the first element lst[0] to the variable first, all elements in between lst[1:-1] to the variable middle, and the last element lst[-1] to the variable last. The expression lst[0] directly accesses the first element in the list. The slice lst[1:-1] takes everything except the first and last elements, which makes up the middle part of the list. The expression lst[-1] accesses the last element using negative indexing.
  ```python
    lst = [1, 2, 3, 4, 5, 6]
    
    first = lst[0]                                # take first item in the list (index 0 = 1)
    middle = lst[1:-1]                            # take all items except yung first at yung last ([2,3,4,5])
    last = lst[-1]                                # take last item in the list (index -1 = 6)


- **Output:**
  ```python
    print("first:", first)                       
    print("middle:", middle)
    print("last:", last)

> first: 1\
> middle: [2, 3, 4, 5]\
> last: 6
