# Python-basics-course-assignment

# 1. Below are a set of scores that students have received in the past semester.
# Write code to determine how many are 90 or above and assign that result to the value a_scores.

scores = "67 80 90 78 93 20 79 89 96 97 92 88 79 68 58 90 98 100 79 74 83 88 80 86 85 70 90 100"
scores_split = scores.split(" ")
a_scores = 0
for x in scores_split:
    x = float(x)
    if x >= 90:
        a_scores += 1
        
# 2. Write code that uses the string stored in org and creates an acronym which is assigned to the variable acro.
# Only the first letter of each word should be used, each letter in the acronym should be a capital letter, and there should be nothing to separate the letters of the acronym.
# Words that should not be included in the acronym are stored in the list stopwords. 
# For example, if org was assigned the string “hello to world” then the resulting acronym should be “HW”.

stopwords = ['to', 'a', 'for', 'by', 'an', 'am', 'the', 'so', 'it', 'and', "The"]
org = "The organization for health, safety, and education"

stopwords = set(w.upper() for w in stopwords)
acro = ''.join(i[0] for i in org.upper().split(' ') if i not in stopwords)

# 3. Write code that uses the string stored in sent and creates an acronym which is assigned to the variable acro.
# The first two letters of each word should be used, each letter in the acronym should be a capital letter, and each element of the acronym should be separated by a “. ” (dot and space).
# Words that should not be included in the acronym are stored in the list stopwords.
# For example, if sent was assigned the string “height and ewok wonder” then the resulting acronym should be “HE. EW. WO”.

stopwords = ['to', 'a', 'for', 'by', 'an', 'am', 'the', 'so', 'it', 'and', 'The']
sent = "The water earth and air are vital"

acro = '. '.join(word[:2].upper() for word in sent.split() if word not in stopwords)
print(acro)

# 4. A palindrome is a phrase that, if reversed, would read the exact same.
# Write code that checks if p_phrase is a palindrome by reversing it and then checking if the reversed version is equal to the original.
# Assign the reversed version of p_phrase to the variable r_phrase so that we can check your work.

p_phrase = "was it a car or a cat I saw"
r_phrase = p_phrase[::-1]

for item in inventory:
    item_desc, number, cost = item.split(", ")
    print("The store has {} {}, each for {} USD.".format(number, item_desc, cost))
    
str1 = "I love python"
# HINT: what's the accumulator? That should go here.

#Currently there is a string called str1. Write code to create a list called chars which should contain the characters from str1. Each character in str1 should be its own element in the list chars.
chars = []
for w in str1:
    chars.append(w)
print(chars)

