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

### Save Password Solution
    - Remove duplicates
    - Your function should take in a string of characters and return a
        string with the duplicate characters removed. Assume that your input
        is lowercased with only letters and numbers.
    - Solution:
        - create a new, empty string called dupesRemoved
        - loop through the string we want to remove dupes from
            - if no, add it
            - if yes, keep going through the loop (do nothing)
        - dupesRemoved -- it has no duplicates!

### Frequency of Letters in your name
    - Write a function that counts how many times each letter of your name
        occurs. Your function should take in your first and last name and return
        an object where the keys are each character in your name, and the value
        is how many times that character appears in your name.
    - Example input: "Peggy Porth"
    - Example output: {p: 2, e: 1, g: 2, y: 1, o: 1, r: 1, t: 1, h: 1}
    - Your function should NOT count spaces and should not be case sensitive (a
        lowercase t and a capital T should be considered the same character).
    - Solution plan:
        - peggyporth (our name)
        - initialize a new empty object to hold the letter counted
            - const count = {}
        - remove all spaces and lowercase all characters of the input str
            - toLowerCase() -> split(" ") -> join("");
            - const name = str.toLowerCase().split(" ").join("");
        - loop through the letters of the string
            - for(let i = 0; i < name.length; i++)
        - if the character is not the obj, add it, give it a value of 1
            - check if is it on our object using bracket notation
                - if(!count[name[i]])
                - count[name[i]] = 1;
        - if the character is already in the object, increment that char's value
            - count[name[i]] += 1;

### Chef Mario Recipe Solution 1
    - Chef Mario was in the middle of writing his cookbook masterpiece
        when he spilled coffee on his keyboard! Now all his recipes have repeat
        ingredients.
    - Help save Chef Mario's cookbook by writing a function that takes in an array 
        and returns a new array with all the duplicates removed. 

    - Example input: ["🌈 rainbow", "🦄 unicorn", "🍭 lollipops", "🦄 unicorn", "🍭 lollipops"];
    - Example output: ["🌈 rainbow", "🦄 unicorn", "🍭 lollipops"];
    - Solution plan:
        - create a new arr to hold unique items 
        - for each item in recipe arr
        - if the item is NOT yet in the unique arr, push it in (includes() method)
        - if it is in the unique arr, move on to the next item (do nothing)
        - return the unique arr
        Note: check the opposite
        if(!uniqueItems.includes(item)){
           uniqueItems.push(item);
       }

### Chef Mario Recipe Solution 2
    - Solution 1 is limited, if we have two arrays with hundred/thousands data, we have to do with nested arrays
    - Instead we can use and object to keep track the data
    - Solution plan:
        - create a new object to keep track of duplicates 
        - use filter to loop thorugh each item in the arr
            - for each item in arr
                - look up the item in the lookup table
                - if the item does NOT exist in the lookup, add it and return true
            - return false

### ### Chef Mario Recipe Solution 3
    - Spread operator
    - new Set()

### Pumpkin Prizes Solution
    - Write a function to flatten nested arrays of strings or
        numbers into a single array. There's a method
        for this, but pratice both doing it manually and using the method. 
        Example input: [1, [4,5], [4,7,6,4], 3, 5]
        Example output: [1, 4, 5, 4, 7, 6, 4, 3, 5]
    - Solution plan:
        - Built-in metod flatten()
            - return arr.flat()
        - Manually
            - initialize a new, empty array
                - loop through the passed in array and check - string or array?  
                    - built-in method Array.isArray()
                    - if the item is string, push into the new array
                    - if the item is an array, loop through it, pushing each item into the array
            - return new array

### Count Students Solution
    - He has an array of first-time attendees for each month of the year. 
        Help him find the total number of attendees! Your function should
        take in an array and return a number representing the total number
        of new attendees. 
        Example input: [1,2,3]
        Example output: 6
    - Solution plan:
        - initialize a new variable to hold the sum of the arr 
        - loop through the studentCount arr, add each value to the sum (for loop or forEach loop)
            - with forEach loop we are using implicit return
        - after done looping, return the sum
            - pass an array [1,3,4]

### Pizza Night Solution (Common exercise)
    - Write a function to find the food with the highest number of votes. 
    - Your function should take in a food object and find the food
    - with the most votes. It should log the winner, along with 
    - how many votes it received.  
    - Example input: {"🐈 cats": 19, "🐕 dogs": 17} 
    - Example output: The winner is 🐈 cats with 19 votes!
    - Solution plan:
        - initialize some new variable to: 
            - keep track of the current highest vote number
            - keep track of the current winning item
        -  for each food option in the food object
        - is the current value higher than the value of highestVotes?
            - yes: the new value of highestVotes in the current value and
            - winningItem = the current property
        - return string announcing the winner using winningItme and highestVote variables

### Totally Private Data Solution (Destructure data from the object)
    - Write a function that maps through the current data and returns
        a new an array of objects with only two properties: 
        fullName and birthday. Each result in your 
        array should look like this when you're done: 
    {
        fullName: "Levent Busser", 
        birthday: "Fri Aug 20 1971"
    }

    Read about toDateString() for info on formatting a readable date.
    Data is hosted locally on data.js
    - Solution Plan:
        - use map to loop through the data
            - return an object with the two new properties
            - concat the first and last name
            - create a new date object, passing in the dob
            - format by calling toDateString() method

### Find free Podcast Solution (map() and filter() methods)
    - Transform Mock Data (data1.js file)
    - Dont forget to import our data using 'import' ES6 syntax
        - import podcasts from './data1.js';
    - Write a function that takes in the podcast data and returns an new
        array of only those podcasts which are free.
        Additionally, your new array should return only 
        objects containing only the podcast title, rating, and whether or 
        not it is paid. 
        Expected output: 
        [
            {title: "Scrimba Podcast", rating: 10, paid: false}, 
            {title: "Something about Witches", rating: 8, paid: false}, 
            {title: "Coding Corner", rating: 9, paid: false}
        ]
    - Solution Plan:
        - filter list by paid prop
        - use map to create a new array of objects with only the specified properties
            - chain both methods 

### Candy Sale Solution
    - Transform Mock Data (data2.js)
    - Dont forget to import our data using 'import' ES6 syntax
        - import products from './data2.js';
    - To buy up all the candy, use map() and filter() to put all the
   candy into a `shoppingCart` array. 
   The new array should contain only the item and the price, like
   this: 
   Expected output: 
   [
       {item: "🍭", price: 2.99},
       {item: "🍫", price: 1.99}, 
       {item: "🍬", price: 0.89}
    ]
    - Solution plan:
        - filter the data by product.type -- only sweet
        - loop through the data using map 
        - for every candy, return a new object with only item and price
        - chain methods
        - return an object
        - bonus:
            - destructure and use short syntax

### Shopping Cart Solution (reduce() method)
    - Transfrom Mock Data (data3.js)
    - Dont forget to import data using 'import' ES6 syntax
        - import shoppingCart from './data3.js';
    - Use reduce() to total the groceries. 
    Then find a method that will round the total to 2 decimal places.
    Example output: 73.44
    - Solution Plan:
        - Only reduce you have to use
        - toFixed()

### Total Savory Items Solution (no other operations)
    - Transfrom Mock Data (data4.js)
    - Dont forget to import data using 'import' ES6 syntax
        - import shoppingCart from './data4.js';
    - Use reduce() and only reduce() to calculate and return 
    the total cost of only the savory
    items in the shopping cart.
    Expected output: 9.97
    - Solution Plan:
        - check if the current item has a type of "savory"
        - if yes, return acc += curr.price
        - if no, return acc

### Holiday gift shop Solution (sort method() )
    - Transfrom Mock Data (data5.js)
    - Dont forget to import data using 'import' ES6 syntax
        - import shoppingCart from './data5.js';
    - Study the sort method, callback - comparison
    -     You're online shopping for holiday gifts, but money is tight
    so we need to look at the cheapest items first. 
    Use the built in sort() method to write a function that returns a new array of
    products sorted by price, cheapest to most expensive. 
    
    Then log the item and the price to the console: 
    
    💕,0
    🍬,0.89
    🍫,0.99
    🧁,0.99
    📚,0.99
    ... continued
    
    - Solution Plan:
        - positive num - a before b 
            neg - b before a 
            0 - nothing changes 
            a - b sorts numbers in ascending order and 
            b - a sorts numbers in descending order

### Unique Genre Tags Solution 
    - Transfrom Mock Data (data6.js)
    - Dont forget to import data using 'import' ES6 syntax
        - import shoppingCart from './data6.js';
    - As a software dev at ScrimFlix, you're working on a feature 
    to let users browse TV shows by tag. The first step is to collect all 
    the tags from our data into a new array. Then we'll need 
    to filter out the duplicate tags. 
    Write a function that takes in the media data and returns
    a flat array of unique tags.
    Expected output: 
    ["supernatural", "horror", "drama",
    "fantasy", "reality", "home improvement", "comedy", "sci-fi", "adventure"]
    - Solution plan 1 (Array method):
        - use map to loop through the data and get a new array of tags
        - flatten the tags array with .flat()
        - create a new array uniqueTags to hold the unique values
        - loop through the tags array
            - is the element already in the uniqueTags arr? 
                - no: push into arr
                - yes: keep going
        - return uniqueTags arr
    - Solution plan 2: (Object method, Data and Algorithm style)
        - Optimized solution
        - Eleminate nested loops
        - filter tags arr
        - look up the tag in the uniqueTags obj
        - if it's not the, we have a unique item 
        - put the item in our object with a value of true

### Abroad Airlines Solution - built-in sorth() method (find a podcast as long as your flight)
    - Transfrom Mock Data (data7.js)
    - Dont forget to import data using 'import' ES6 syntax
        - import shoppingCart from './data7.js';
    - Our Scrimba Airlines in-flight entertainment package 
    includes a variety of podcasts. We need to add a feature that suggests
    podcasts to our patrons based on whether a flight is short or long. 

    Your sort function should take two arguments: the podcast data and
    flight length. If the flight is 60 minutes or less, sort the podcast list 
    from shortest to longest. If it's anything else, sort from longest
    to shortest. 

    Your function shouldn't return anything. Instead log a numbered list 
    of the title and duration of 
    each podcast to the console, like this:

    1. Crime Fan, 150 minutes
    2. Mythical Creatures, 99 minutes
    3. Crime Crime Crime, 70 minutes
    4. Coding Corner, 55 minutes
    5. Scrimba Podcast, 50 minutes
    6. Something about Witches, 35 minutes

    Note:   a - b will sort an array in descending
            b - a will sort in ascending order
    
    - Solution:
        - Check if flight is greater than 60 minutes
        - if yes, sort decending order (longest to shortest)
        - if no, sort ascending order (shortest to longest)
        - loop through my sorted array
        - construct a string using the title and duration props 
        - use the index to number the list
        - console.log each item

### Popularity Contest Solution (reduce built-in method() )
    - - Transfrom Mock Data (data8.js)
    - Dont forget to import data using 'import' ES6 syntax
        - import shoppingCart from './data8.js';
    - Iggy the Influencer and Toby the Tiktoker are dying to know
        who's more popular on social media. 
        Toby's TikToks get an average of 400 likes. On average, how many
        likes do Iggy's Instagram posts get? 
        In data8.js you'll find a list of Iggy's recent posts. 
        Use reduce() to write a function that returns the average number of likes.
        To find the average, add up the total number of likes, then divide
        by the total number of posts.
    - Solution plan: 
        - reduce to single total
            - add curr.likes to acc
        - divide the total by data.length to get the avg

### Night Naughty Solution (use reduce() method not flat() method )
    - Transfrom Mock Data (data9.js)
    - Dont forget to import data using 'import' ES6 syntax
        - import shoppingCart from './data9.js';
    - It's time for the Scrimbies, a prestigious award show for podcast hosts.
        We need to assemble a list of podcast hosts so we can start handing out awards. 
        Write a function that takes in the podcast data and
        returns a flat array of podcast hosts. There are quite a few ways to approach
        this, but try solving the problem using reduce(). 
        Once you have a flat array of hosts, write a second function to randomly assign each host a prize
        from the awards array. 
        Example output: ["🏆 Alex Booker", "⭐ Bob Smith", "💎 Camilla Lambert" ...]
    - Solution plan: 
        - flat arrays using reduce()
            - reduce the podcasts data down to a list of hosts
            - add curr.hosts to the acc array
        - Two solutions for flattening arrays:
        - Solution 1:
        - const awards = ["🏆", "⭐", "💎", "🥇", "👑"];
            function getHosts(data){
            // reduce the podcasts data down to a list of hosts
            return data.reduce((acc, curr)=>{
                // add curr.hosts to the acc array
                return acc.concat(curr.hosts)
            }, [])
            }
        - Solution 2: (spread operator)
        const awards = ["🏆", "⭐", "💎", "🥇", "👑"];
        function getHosts(data){
        // reduce the podcasts data down to a list of hosts
        return data.reduce((acc, curr)=>{
            // add curr.hosts to the acc array
            return [...acc, ...curr.hosts]
        }, [])
        }

        - function assignAwards(data){
            // use getHosts() to get a flat array of podcasts hosts
            // map through my array of hosts. for each:
                // use Math.random to generate a rand num between 0 and length of award arr
                // use the rand num to access a random award index
                // use string literal to concast a random award to each host                 
        }

        -function assignAwards(data){
            // use getHosts() to get a flat array of podcasts hosts
            const hosts = getHosts(data);
            // map through my array of hosts. for each:
            return hosts.map(host => {
                // use Math.random to generate a rand num between 0 and length of award arr
                const randIndex = Math.floor(Math.random() * awards.length); 
                // use the rand num to access a random award index
                // use string literal to concast a random award to each host 
                return `${awards[randIndex]} ${host}`;
            });   
        }

### Save the weekend Solution (automate your job)
    - Transfrom Mock Data (data10.js)
    - Dont forget to import data using 'import' ES6 syntax
        - import podcasts from './data10.js';
    - Your best friend is a copywriter who writes product descriptions 
        for a living. You want to use your hacking skills to help them 
        automate their job so you both can spend the weekend on a 
        tropical island. 
        Use array methods and the existing podcast data to write a function that
        can generate a description for each podcast. 
        Add the description as a new property on each podcast object, and return
        a new podcast array where each podcast has a description. 
        Each description should look like this: 
            [
                {
                    id: 1,
                    title: "Scrimba Podcast", 
                    ...
                    description: "Scrimba Podcast is a 50 minute education podcast hosted 
                    by Alex Booker."
                }
                ...
            ]
        If the podcast has more than one host, you can display only the first host.
        Stretch goal: Display all three hosts in the description, seperated with commas: 
        Example description: "Coding Corner is a 55 minute education podcast hosted by Treasure Porth, Guil Hernandez, and Tom Chant."
        - Solution plan:
            - map through the data
            - destructure the data
            - use title, duration, genre and host data to make description
            - for each podcast object, add description prop
                - two ways to add the 'description' prop
                    - First, manually
                        - podcast["description"] = `${title} is a ${duration} minute ${genre} podcast hosted 
                          by ${hosts[0]}.`;
                    - Second, returning a new object, modern way
                        - return {
                            ...podcast,
                            description: `${title} is a ${duration} minute ${genre} podcast hosted 
                            by ${hosts[0]}.`
                            }

### Anagrams in an Array Solution
    - Each item in the anagrams array is an anagram of a Scrimba teacher's
        first and last name, plus the phrase "Scrimba teacher". 
        Write a function to determine which strings in the array are 
        anagrams of "Bob Ziroll Scrimba Teacher".
        Your function should take two parameters: the phrase you want to compare to
        the anagrams, and an array of anagrams. The function should return
        a new array of anagrams that match the phrase. 
        Example input: treat, ["tater", "tree", "teart", "tetra", "heart", "hamster"]
        Example output: ["tater", "teart", "tetra"]
        Bonus: What other teachers are represented in these anagrams?
    - Solution plan:
        - Create the first function that sortPhase():
            - Takes a parameter
            - turn toLowerCase()
            - split() the phrase
            - sort() the phrase
            - join() the phrase
            - trim() the space inside the phrase
        - Create the second function that operates on the array isAnagramInArray():
            - array data
                const anagrams = [
                    "moz biblical torchbearers",  
                    "it's razorbill beachcomber", 
                    "och mcrobbie trailblazers", 
                    "bib chorizo cellarmaster", 
                    "thor scribble carbimazole", 
                    "zilla borscht abercrombie", 
                    "brazil scorcher batmobile", 
                    "dame shelburne characterizing", 
                    "uber englishman characterized", 
                    "agnes rhumbline characterized", 
                    "rehab scrutinized charlemagne", 
                    "dreams zurich interchangeable", 
                    "bam hamster technocratic", 
                    "mechatronic masterbatch", 
                    "bam ratchet mechatronics"
                ]
            - use .filter()
            - use sortPhrase() to sort both the input phrase and the current phrase in the array
            - compare the two words to return true or false
                - function sortPhrase(phrase){
                    return phrase.toLowerCase().split('').sort().join('').trim();
                }

                function isAnagramInArray(anagram, arr){
                    // use .filter()
                    // use sortPhrase() to sort both the input phrase and the current phrase in the array
                    // compare the two words to return true or false
                    return arr.filter(item => {
                        const word1 = sortPhrase(anagram);
                        const word2 = sortPhrase(item);
                        
                        return word1 === word2;
                    })
                }
                console.log(isAnagramInArray("Tom Chant Scrimba Teacher", anagrams)); test it

### 