# JavaScript Challenges

## What we will practice:
    - Strings and Strings methods
    - Arrays and Arrays methods
    - Working with data and APIs
    - Classic interviews challenges like:
        - Reversing a string
        - finding anagrams
        - FizzBuzz
    - A skill we learn though practice
    - A efficient but limited way for a potential employer to gauge our ability to code
    - Not an amazing measure of our potential
    Tips for Success:
        - Write pseudo code (or look at someone else)
        - Use built-in methods, unless stated otherwise
        - Look things up
        - clg frequently
        - Practice solving problems aloud
        - Struck? Study solutions and try again
    Keep in mind:
        - Solved problem? We're doing great! (Optimization and edge cases are stretch goals)
        - Solution maybe will be different than others
        - Write 'pure' functions
            - A pure function is a function that:
                - Takes a value
                - Returns a value
            - A pure function is reusable function
        - Verbose and readable over short and clever
# endrixhukellari-JavaScript-challenges

### Panic Solution
    - Split and Join built-in methods
    - toUpperCase method

### Whisper Solution
    - endsWith and slice built-in methods

### Alternating Caps Solution
    - Looping through the string
    - UpperCase every character with an even index
    - Assemble each character back into a string

### toTitleCase Solution
    - JS doesnt have built-in method to uppercase only the first letter of the first word
    - We are going to create from scratch
    - One method is:
        - Take the first index of the word, to uppercase
        - And take the rest of the word without the first index and then use slice
    - Second Method is:
        - split sentence into an array of words
        - loop through the arrays of words and capitalize func on each word
        - join sentence arr back into a string

### Definitely Not FizzBuzz Solution
    - Hint:
        - Remainer/Modulus operator
    - Our company has 100 employees and their employee ID numbers range from 1 - 100. If the employee's ID number is: 
    - Divisible by 3 - Vacation! 
    - Divisible by 5 - $100,000 bonus! 
    - Divisible by both 3 and 5 - JACKPOT! 1 Million and a Yacht!
    - Not divisible by 3 or 5 - :(
    - Plan to solve this:
        - Loop through 1-100
            - check if its divisible by 3 & 5 (both 3 and 5) or (3*5 = 15) divisible by 15
            - next is divisible by 3?
            - next is divisible by 5?
            - if none of numbers isnt divisible return a sad face :/

### Emojify - Popular Services like Notion, Slack and Github supports emoji short codes Solution
    - Autodetect if you are writing an emoji (:smile, :smile_cat)
    - Replace code with emoji
    - We are going to mimic this using JS
    - Hints:
        - To check for colons in a word use 'startsWith()' and 'endsWith()'
        - Use slice() to trim the colons from the word so you can use it to look up emojis in the emojis object
            - Check slice() methods how it works. Single Argument, two args and what is (1, -1)
            - Check if our 'word' exists in the emoji object
        - To check each word in a phrase for emoji shortcodes,
            - split() the passed in phrase into an array
            - map through the array and call emojifyWord() on each word in the phrase
            - join the array back together as a string, and return

### Is it an Anagram? Solution
    - What is an Anagram?
        - An anagram is "same letters", "different words"
    - Write a function to check if two strings of lowercase letters are anagrams. 
    - Return true if the word is an anagram. Return false if it isn't.
    - Big hints:
        - If two words are anagrams, their lengths will be the same exactly the same
        - Sort both strings so they're in alphabetical order (there's a built-in method for this)
        - Are they equal when sorted? Then you have an anagram
        - Tip:
            save - vase (compare the length)
            save - aesv (sort the save alphabetically)
            vase - aesv (sort the vase alphabetically)
            aesv === aesv? ANAGRAM!
    Plan: 
    - are the strings the same length? if yes return false. 
    - split string into an array
    - sort
    - join the array back together as a string
    - repeat with second word
    - are the two words equal? true or false

### Decode an Alien Message - Reverse the String Solution
    - We have two ways
        1- String methods (easy)
            - split() the string, reverse it and join
        2- Reversing Manually
            - Init a new empty string
            - loop through original string backwards, adding each character to the new string (backward loop)
            - return the string
        3- Reverse string in Array
            - map throug the array
            - for every item call the function 'Reversing Manually'

### Palindromes Solution
    - What is a Palindrome?
        - A palindrome is a same word forward or backward
        - Example:
            - civic
            - kayak
            - level
            - racecar
            - noon
            - solos
    - Write a function to check if a lowercased string of letters is a palindrome.
    - If the word is palindrome, return true. If it isn't, return false.
    - Hint:
        - Reverse the word and compare it to the original word
    - Solution 1
        1- Manually Reversing the String
            - reverse the word using a backward for loop to create a new string
            - compare the new string to the original word - are they equal? 
            - yes - return true
            - no - return false
    - Solution 2
        2- 