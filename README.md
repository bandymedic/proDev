 //reverse a string//

  //declare a function and argument

  function reverseString(str) {

	//using .split to separate every character into separate strings, .reverse to reverse the order of separate characters, .join to put the reverse order characters back into one string.
	
	return str.split("").reverse().join("");
}
  //call the function to reverse the variable "str"

  reverseString("EseveR");

________________________________________________________________

//factorialize a number (n!)//

//declare a blank variable for an array
var thx = [];

  //declare a function and argument

  function factorialize(num) {
	
	//declare "if" statement to compare "logical OR" findings with boolean semantics to return statement if true
	if (num === 0 || num === 1) {
	   return 1;
	}
	
	//declare "if" statement to set condition if variable "thx" has an array containing value of the variable "num" greater than 0 to return the variable "thx" with an array containing the value of "num"

	if (thx[num] > 0) {
	   return thx[num];
	}

	//return variable thx[num] equals conditional function of "factorialize" with argument "num" - 1 multiplied by the argument "num"

	return thx[num] = factorialize(num-1) * num;

   }

//call the funtion "factorialize" with argument

factorialize(8);

________________________________________________________________

//check for palindromes//

//declare a function and argument

function palindrome(str) {

	//return the var "str" using .replace with operators /[\W_]/g will match non-word characters and underscores globally, then convert .toLowerCase. Compare that value to "str" .replace with operators /[\W_]/g will match non-word characters and underscores globally, then convert .toLowerCase, then .split to isolate all characters of string, then .reverse to reverse the order of all characters of string, then .join to put the reverse order characters back into one string. This will return a boolean stating if the string is a palindrome or not.

	return str.replace(/[\W_]/g, '').toLowerCase() === str.replace(/[\W_]/g, '').toLowerCase().split('').reverse().join('');

}

//call the function with argument string
palindrome("racecar");

________________________________________________________________

//find the longest word in a string//

//declare a function and argument

function findLongestWord(str) {

   //declare variables to .split "str" using white spaces (" ") and variable to create a baseline length of the string.
   var splitString = str.split(" ");
   var stringLength = 0;

   //create a for loop to declare a new variable "i", compare it to splitString.length, and to add "i" to itself after every loop has been executed.
   for (var i = 0; i < splitString.length; i++) {
	
	//create if statement to compare splitString with splitString passing "i" as the value for location in array and .length
	if (splitString[i].length > stringLength) {
	   
	   //code to be executed if the above condition is true
	   stringLength = splitString[i].length;
	}
   }
   
   //return the value of the variable stringLength
   return stringLength;

//call the function with argument string
findLongestWord("We were somewhere outside of Barstow, on the edge of the desert, when the drugs began to take hold..");

________________________________________________________________

//titlecase a sentence//

//declare a function and argument
function titleCase(str) {

   //declare variables to convert(using .toLowerCase and .split) and store(using the .map function to replace the character at the "0" position of each string .toUpperCase)
   var convertSent = str.toLowerCase().split(" ");
   var newSent = convertSent.map(function(val) {
	return val.replace(val.charAt(0), val.charAt(0),toUpperCase());
   });

   //return the value of the var "newSent" and use .join to combine back into one string
   return newSent.join(" ");
}

//call the function with argument
titlecase("He who makes a beast out of himself, gets rid of the pain of being a man");

________________________________________________________________

//return largest numbers in arrays//

//declare a function and argument
function largestOfFour(arr) {

   //declare a variable to store results of function
   var results = [];

	//create a for loop to declare a var "n", compare "n" to arr.length, and then add "n" to itself for every loop that has been completed
	for (var n = 0; n < arr.length; n++) {
	   
	    //create variable to define largest number in each array
	    var largestNumber = arr[n][0];

	    //create another for loop to declare var "i", compare "i" to arr with array position of [n].length, and to add "i" to itself for every loop that has been completed
	    for (var i = 1; i < arr[n].length; i++) {
		
		//create an if statement to compare arr[n][i] to largestNumber variable
		if (arr[n][i] > largestNumber) {

		   //code to be executed if the above condition is true
		   largestNumber = arr[n][i];
	  	   }
		}

		//declare "results" variable with "n" as array position is equal to largestNumber variable
		results[n] = largestNumber;
	     }

	   //return the variable "results"
	   return results;
}

//call the function with argument
largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);


________________________________________________________________

//Check if a string (first argument, str) ends with the given target string (second argument, target).//

//define a function with arguments for str and target string
function confirmEnding(str, target) {

   //return "str" using .substr function with argument of negative target.length and test if it absolutely equals the var "target"
   return str.substr(-target.length) === target;
}

//call the function with arguments to test
confirmEnding("Batman", "n");

________________________________________________________________

//Repeat a given string (first argument) num times (second argument). Return an empty string if num is not a positive number.//

//define a function with arguments for str and num of times to repeat str
function repeatStringNumTimes(str, num) {

   //create an if statement to compare "num" with 0
   if (num >= 0) {

	//code to be executed if the above condition is true
	return str.repeat(num);

	//else statement to be executed if the above condition is false
   }	else {
	return ""; //returns null
   }
}

//call the function with arguments to test
repeatStringNumTimes("test", 3);

________________________________________________________________

//Truncate a string (first argument) if it is longer than the given maximum string length (second argument). Return the truncated string with a ... ending.

//define a function and arguments for str and num at which to truncate
function truncateString(str, num) {

   //create an if statement to compare str length with num and if num is greater than 3
   if (str.length > num && num > 3) {

	//code to be executed if the above condition is true
	return str.slice(0, (num - 3)) + '...';

	//else if statement to compare str length with num and if num is less than or equal to 3
   }	else if (str.length > num && num <= 3) {

	//code to be executed if the else if statement is true
	return str.slice(0, num) + '...';

   	//else statement to return str if none of the other conditions apply
   }	else {
	return str;
   }
}

//call the function with arguments to test
truncateString("It was the best of times, it was the worst of times");

________________________________________________________________

//Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.//

//define function and arguments for array and requested size of arrays
function chunkArrayInGroups(arr, size) {
	
   //define variables for temporary array and the resulting array
   var temp = [];
   var result = [];

   //create a for loop to define var "a", compare "a" to the array length, and add "a" to itself for every loop that has been completed
   for (var a = 0; a < arr.length; a++) {
	
	//create an if statement to use modulo operator to determine remainder between "a" and size !== not equal to size - 1
	if (a % size !== size - 1)
	
	   //code to be executed if the above condition is true
	   temp.push(arr[a]);

	//create an else statement if the if statement is false
	else {
	   temp.push(arr[a]);
	   result.push(temp);
	   temp = [];
	}
   }

   //create an if statement to compare "temp" length is not equal in size to 0
   if (temp.length !== 0)

   	//code to be executed if the above condition is true
	result.push(temp);
   
   //return the variable result after all items have been updated
   return result;
}

//call the function and arguments
chunkArrayInGroups(["a", "b", "c", "d"], 2);


________________________________________________________________

//Return the remaining elements of an array after chopping off n elements from the head.//

//define function and arguments for the array and how many to cut
function slasher(arr, howMany) {

   //.splice array at the 0 position by the var "howMany"
   arr.splice(0, howMany);

   //return the new value of array
   return arr;
}

//call the function and arguments
slasher([1, 2, 3, 4, 5], 2);


________________________________________________________________

//Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.//

//define the function and argument
function mutation(arr) {

   //define variables for the test array at the 1 position and target array at the 0 position and .toLowerCase
   var arrTest = arr[1].toLowerCase();
   var arrTarget = arr[0].toLowerCase();

   //create a for loop to create a new variable "i", compare "i" to the length of the test array, and add "i" to itself after every completed loop
   for (i = 0; i < arrTest.length; i++) {

	//create an if statement to test if the target array's .indexOf(test array position [i]) is equal to -1
	if (arrTarget.index(arrTest[i]) === -1)
		
	   //return boolean if above statement is true
	   return false;

	}

	//return boolean if the function finds that the first element of the array contains all of the letters of the string in second element
	return true;
}

//call the function and argument array
mutation(["hello", "hey"]);

________________________________________________________________

//Remove all falsy values from an array.//

//define function and argument
function bouncer(arr) {

   //return the array .filter for negative boolean elements
   return arr.filter(boolean);
}

//call the function and argument array **note the true entry in the array is not eliminated
bouncer([7, "ate", "", false, 9, true]);


________________________________________________________________________________________________

//Remove all values in array as defined by the second argument//

//define function and argument
function destroyer(arr) {
  //remove all the values
  
  var args = Array.prototype.slice.call(arguments);
  //get full array values

  args.splice(0,1);
  //remove original array

  var placeHolder = [];
  //create place holder for new array

  for (var i = 0; i < arr.length; i++) {
    for (var j = 0; j < args.length; j++) {
      if (arr[i] === args[j]) {
        delete arr[i];
        //compare array with values and delete any matches
      }
    }
  }
  placeHolder = arr.filter(Boolean);
  //filter out falsy values
  return placeHolder;
}

//****OR****//
 
  placeHolder = arr.filter(removeFalseVar);

  return placeHolder;
}

//create a function to remove falsy values
function removeFalseVar(value) {
  return Boolean(value);
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);

_______________________________________________________________

//Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. The returned value should be a number.

function getIndexToIns(arr, num) {
  // Find my place in this sorted array.
  
  var count = 0;
  //variable of count for results
  
  for (i = 0; i < arr.length; i++) {
    if (arr[i] - num < 0) {
      //if statement to check if arr value - number returns negative, then it is a smaller number
      
      count = count + 1;
      //if the statement returns true, then add count + 1 and test with next number in arr
    }
  }
  return count;
}

getIndexToIns([40, 60], 50);


________________________________________________________________


//One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount... A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus 'A' ↔ 'N', 'B' ↔  'O' and so on.

//define a function and argument to split the argument str, map the string, and join it back together after altering it using regex and ascii code
function rot13(str) {
  str = str.split("").map(cipher).join("");
  return str;
}

//define a function and argument to filter the string using a regex code to filter "^ = not" upper and lower case letters globally
function cipher(letter) {
  var symbolregex = /[^a-zA-Z]/g;
  
  //tests boolean to see if the string is a letter or not 
  if (symbolregex.test(letter)){ 
    return letter;
  }
 
  //finds ascii code of defined letter 
  var codeAscii = letter.charCodeAt(0);
  
  //if statement to set limit at 77 in Ascii to return only uppercase letters. if the number is higher than 77, then we subtract 13 to shift the cipher of the letter. if the number is lower than 77, then we add 13 to shif the cipher of the letter.
  if (codeAscii > 77) {
    codeAscii -= 13;
  } else {
    codeAscii += 13;
  }
  
  //returns string from ascii code back to corresponding letter
  return String.fromCharCode(codeAscii);
}
// Change the inputs below to test
rot13("LBH QVQ VG!");


_______________________________________________________________

//Return the sum of two numbers in the array and all numbers between them. example [1, 5] would be 1 + 2 + 3 + 4 + 5 = 15

//define a function and argument to add all numbers between and including the two numbers in the array
function sumAll(arr) {
  //using Math.min and .max we are arranging the numbers in sequential order
  var min = Math.min(arr[0], arr[1]);
  var max = Math.max(arr[0], arr[1]);
  
  //temp variable to store results of for loop
  var temp = 0;
  
  //for loop to run sequence of addition for each number until limit is reached
  for (var i = min; i <= max; i++) {
    temp += i;
  }
  
  return temp;
}
//change inputs to test
sumAll([1, 4]);

__________________________________________________________________

//compare two arrays and return a new array with any items that are not common between the two original arrays. example [1, 2, 3, 4, 5] and [1, 2, 3, 4], the new array should contain [5].

//define a function and arguments to compare arrays
function diffArray(arr1, arr2) {

  //define variable to hold new array
  var newArr = [];

  //define function to 
  function onlyInFirst(first, second) {
      
     //for loop to run through every instance in array until limit is reached
     for (var i = 0; i < first.length; i++) {
        
        //if statement to push value to new array
        if (second.indexOf(first[i]) === -1) {

	   newArr.push(first[i]);
	}
     }
   }

   onlyInFirst(arr1, arr2);
   onlyInFirst(arr2, arr1);

   return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);


______________________________________________________________________


//Convert the given number into a roman numeral

// declare variable and nest function in the variable
var convertToRoman = function(num) {
  
  //declare variables to define decimal value and corresponding roman numeral place in arrays
  var decimalValue = [ 1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1 ];
  var romanNumeral = [ 'M', 'CM', 'D', 'CD', 'C', 'XC', 'L', 'XL', 'X', 'IX', 'V', 'IV', 'I' ];
  
  //declare variable to store result
  var romanized = '';
  
  //for loop to compare length of decimal value and iterate until all places are processed
  for (var index = 0; index < decimalValue.length; index++) {
    
    //while loop to iterate the decimal value of num and index to a roman numeral
    while (decimalValue[index] <= num) {
      romanized += romanNumeral[index];
      num -= decimalValue[index];
    }
  }

  return romanized;
};

convertToRoman(36);

________________________________________________________________________

//return a string from a collection that matches the source

//declare function to define arguments
function whatIsInAName(collection, source) {
  
  //define var to create an array
  var arr = [];
  
  //redefine array to filter the first argument 'collection' by function using obj as argument 
  arr = collection.filter(function(obj){
    
    //for loop to find position in obj and if source does not equal obj return false boolean
    for (var i in source) {
      if (source[i] != obj[i]) {
        return false;
      }
    }
    return true;
  });
  
  return arr;
}

//resulting function should compare the two arguments and find the part of the collection that matches the source. useful for finding titles of movies or songs, or even artists in lists of songs/artists
whatIsInAName([{ first: "Romeo", last: "Montague" }, { first: "Mercutio", last: null }, { first: "Tybalt", last: "Capulet" }], { last: "Capulet" });

____________________________________________________________________

//define function to replace specific word in string

function myReplace(str, before, after) {
  
  //if statement to compare the beginning character of the argument 'before' is equal to an upper case character
  if(before.charAt(0) === before.charAt(0).toUpperCase()){
    
    //result of if statement matches the uppercase character at the beginning of the argument 'after' and concat the rest of the word into the argument
    after = after.charAt(0).toUpperCase() + after.slice(1);
  }
  
  //replace the argument defined 'before' found in the 'str' with the argument 'after'
  return str.replace(before, after);

}

//function should replace the words defined in the arguments regardless of capitalization
myReplace("A quick brown fox jumped over the lazy dog", "jumped", "leaped");

________________________________________________________________________

//define function to translate 'str' to pigLatin
function translatePigLatin(str) {
  
  //define variable for vowels
  var vowel = ['a', 'e', 'i', 'o', 'u'];

  //define var to store split string into array containing each letter of 'str'
  var splStr = str.split('');
  
  //if statement to detect if 'str' starts with a vowel and return the string with 'way' concatenated at the end
  if(vowel.includes(str[0])) {
    return str += 'way';
  } 

    //else statement to push and shift the characters at the beginning of the string if they are consonants, ie. straw - str then aw + str = awstr
    else {
    for(var i = 0; i < str.length; i++) {
      if(!vowel.includes(str[i])) {
        splStr.push(splStr.shift());
      } 
        
	//else statement to modify the push and shift string by adding 'ay' at the end, ie. awstr + ay = awstray
	else {
        splStr.push('ay');
        
	//return the string to a whole word by using .join	
	return splStr.join('');
      }
    }
  }
  return str;
}

//function should translate the argument to pig latin, 
translatePigLatin("consonant"); //"onsonantcay"

__________________________________________________________________________________________________________________

//DNA Pairing

//define a function to pass a string containing the elements of DNA as labeled A, T, C, and G.
function pairElement(str) {
  
  //define a variable that creates an object containing the defined DNA elements and pairings
  var dnaElements = {A: 'T', 
                     T: 'A', 
                     C: 'G', 
                     G: 'C'};
  
  //return the string split into separate characters then mapped est an argument 'basePairs' and inside that function return the argument 'basePairs' and each corresponding dnaElements character.
  return str.split("").map(function(basePairs) {
    return [basePairs, dnaElements[basePairs]];
  
  });
  
}
//call the function to parse the DNA elements data into proper pairs. Only functional when the characters A,T,C,and G are used.
pairElement("GCG");

_____________________________________________________________________________________________________________________

//ASCII validation. Check for missing characters in the argument string passed in function based on ASCII.

//define function that passes an argument string to find missing letter in the string and return it as the output
function findMissingLetter(str) {

  //define variable that splits and maps string and returns ASCII codes for each character
  var num = str.split('').map(function(letter){
    return letter.charCodeAt();
  });
  
  //define for loop to iterate through each character of the argument
  for (var i = 0; i < num.length; i++) {
    
    //if statement that finds the position of the missing character and identifies it by ASCII code and translates it back to character.
    if (num[i+1] - num[i] > 1) {
      return String.fromCharCode(num[i] +1);
    }
    
  }
 
}

//call the function to review string, look for, and identify missing string. only valid if one letter missing.
findMissingLetter("abce");
   

_________________________________________________________________________________________________________________

//create a function to test if argument is a primitive boolean (strictly True or False)
function booWho(bool) {
 if (bool === true || bool === false) {
   return true;
 } else {
   return false;
 }
  
}

booWho(null);

___________________________________________________________________________________________________________________

//create a function to compare arrays in argument to produce one array without repeating characters

function uniteUnique(arr) {
  
  //using .slice, prepares the argument to be treated as one array
  var args = Array.prototype.slice.call(arguments);
  
  //using reduce to flatten all of the arrays in argument    
  return args.reduce(function(a, b) {
    
    //concatenate results and filter into sub array.
    return a.concat(b.filter(function(subArr){
      
      //test each part of argument to make sure there are no duplicates in new array
      return a.indexOf(subArr) < 0;
    }));
    
  });
}

//call the function to break down the argument arrays into one, filter into new array, and test for duplicates.
uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);


__________________________________________________________________________________________________________________

//create a function to translate special characters to HTML compatable code.

function convertHTML(str) {
  
  //create an object for the following characters &, <, >, ", and ' as the key and HTML code for the character as the value
  var entities = { '&': '&amp;',
                   '<': '&lt;',
                   '>': '&gt;',
                   '\"': '&quot;',
                   '\'': '&apos;',
                  };

  //split the string to analyze each character, map the array, and join it back together
  return str.split('').map(function(character){
    
    //return the value for the entities character or return the character itself if not a special character. 
    return entities[character] || character;
    
  }).join('');
  
  
  
}

convertHTML("Dolce & Gabbana");

______________________________________________________________________________________________________________


//create a function that takes a string and "Spinal Tap" cases it (lowercase separated by hyphens)

function spinalCase(str) {
 //using .replace and regular expressions (regex) we are capturing all characters from a-z and A-Z globally, assigning them values $1 $2, and converting them all .toLowerCase
 str = str.replace(/([a-z])([A-Z])/g, "$1 $2").toLowerCase();
   
 //using .replace we are then identifying any whitespaces or underscores and replacing them with a hyphen
 return str.replace(/\s|_/g, '-');
}

spinalCase('AllThe-small Things'); //this will result in 'all-the-small-things'


_______________________________________________________________________________________________________________

//passing a positive integer 'num', return the sum of all odd Fibonacci numbers that are >= 'num'

//define function to return the sum of all fibonacci numbers >= var num
function sumFibs(num) {
  
  //define prototype for new arr returning the last number of the array
  Array.prototype.last = function(){
    return this[this.length - 1];
  };
  
  //define prototype for new arr returning the second to last number of the array
  Array.prototype.secondToLast = function(){
    return this[this.length - 2];
  };
  
  //define var to begin fibonacci sequence, it always starts with 1, 1
  var fibo = [1, 1];
  
  //while loop to add last and second to last numbers in 'fibo' array and push the sum to the last position of the array, continue this while loop until the second to last and last numbers sum <= the var 'num'
  while(fibo.secondToLast() + fibo.last() <= num){
    fibo.push(fibo.secondToLast() + fibo.last());
  }
  
  //filter 'fibo' to remove all even numbers
  return fibo.filter(function(pos){
    return pos % 2 !== 0;
  
  //finish statement by using .reduce to sum the 'fibo' array numbers  
  }).reduce(function(a, b){
    return a + b;
  }); 

}

//call the function to create an array of odd fibonacci numbers for the 'num' variable, then return the sum of those odd numbers
sumFibs(12); //should return '10'
____________________________________________________________________________
//create a function that adds up all of the prime numbers found between 0 and the variable 'num'
function sumPrimes(num) {
  
  //define a variable to hold the prime numbers found
  var primes = [];
  
  //create a for loop to iterate through the 'primes' array starting with '2' since it is the first prime number after 0. This will continue and push the numbers to 'primes' until <= 'num'.
  for (var i = 2; i <= num; i++) {
    if(isPrime(i)){
      primes.push(i);
    }
  }
  
  //helper function to define if num is prime
  function isPrime (num){
    
    //for loop to iterate through the numbers to test if prime. if statement to test if number remainder is absolutely equal to '0' then return boolean false to show number is not prime, else return boolean true.
    for(var j = 2; j < num; j++){
      if(num % j === 0){
        return false;
      } 
    }
    return true;
  }

 //return value of 'primes' by reducing (first number, new number) and then showing sum of entire array.
 return primes.reduce(function(a, b){
   return a+b;
 });
}

//call function
sumPrimes(10); //should be 17, 2 + 3 + 5 + 7 = 17
_________________________________________________________________________



//define function to find the lowest common multiple (LCM) of two numbers in array and start document off with '//noprotect' to run only in browser and prevent infinite loops.

//noprotect
function smallestCommons(arr) {
  
  //define variables for maximum and minimum number in array (in the event the argument given is not in sequential order. Assign 'mltple' the value of max.
  var max = Math.max(arr[0], arr[1]);
  var min = Math.min(arr[0], arr[1]);
  var mltple = max;

  //for loop to start at max, as long as i is > or = to min, iterate down from i.
  for(var i = max; i >= min; i--){
    
    //if statement that states that if 'mltple' * 'i' has a remainder not equal to 0 then 'mltple' = 'mltple' + 'max'. 
    if(mltple % i !== 0){
      mltple += max; 
      i = max;
    } 
  }

  return mltple;  
}


smallestCommons([23, 18]);

__________________________________________________________________________

//define a function to test knowledge of filter method. A. return the first element of array and B. pass a truth test.
function findElement(arr, func) {
   
   //A. return the first element of an array by filtering by the arg 'func'
   return arr.filter(func)[0];

}

                          //B. pass a truth test as to return any even number
findElement([1, 2, 3, 4], function(num){ return num % 2 === 0; });


____________________________________________________________________

//define a function to test knowledge of shift().
function dropElements(arr, func) {

   //set up while loop to test if the argument into the function is true or false. if false '!' at position 0, then shift (knock the first value off of the array)
   while(!function(arr[0])){
      arr.shift();
   }
   
   //when all values in argument 'arr' are tested, return arr.
   return arr;

}

dropElements([1, 2, 3], function(n) {return n < 3; });

_______________________________________________________________________


//define a function to flatten an array with subarrays by: testing each item in array to see if it is an array and then pushing the item to a new array
function steamrollArray(arr) {
  
  //create new array to store results
  var newArr = [];
  
  //call the 'flatten' function to be defined
  flatten(arr);
  
  //define function to flatten arrays by:
  function flatten(arr){
    
    //assigning a test for each item of te array
    arr.forEach(function(item){
      
      //then creating an if statement testing if the item is not '!' an array using Array.isArray
      if (!Array.isArray(item)){
        
        //then pushing that item to the new array
        newArr.push(item);
        
      }
      //so if the if statement is an array (true), then flatten the array
      else{
        
        flatten(item);
        
      }
      
    });
  
  }
    
 //show results of newArr
 return newArr; 

}

steamrollArray([1, [2], [3, [[4]]]]);

_______________________________________________________________________________

//define function to decipher binary code to char code to plain characters. 
function binaryAgent(str) {
  
  //split the string 'str' then use map to create new array with anonymous function 'binary'
  return str.split(' ').map(function(binary){
    
    //return the String and using parseInt decipher the new array by base 2, giving a value fromCharCode.
    return String.fromCharCode(parseInt(binary, 2));
  
  //then join the string back together.  
  }).join('');
  
  
}

//call the function which should return "Aren't bonfires fun!?"
binaryAgent("01000001 01110010 01100101 01101110 00100111 01110100 00100000 01100010 01101111 01101110 01100110 01101001 01110010 01100101 01110011 00100000 01100110 01110101 01101110 00100001 00111111");


//cool concept for data encryption and storage.


______________________________________________________________________________

//define function to test if all properties in object are present as defined by the second argument 'pre'
function truthCheck(collection, pre) {
  
  //return the collection and for every entry, check properties for the 'pre' argument if not present in every entry then the result is false.
  return collection.every(function(properties){
    
    return properties[pre];
  
  });
  
  
}

//call the function and result should be 'true'
truthCheck([{"user": "Tinky-Winky", "sex": "male"}, {"user": "Dipsy", "sex": "male"}, {"user": "Laa-Laa", "sex": "female"}, {"user": "Po", "sex": "female"}], "sex");

//good way to make sure if there are any missing parameters in object entries.

______________________________________________________________________________________

function addTogether() {
  
  //helper function to identify number
  var check = function(num) {
    return typeof num === 'number' ? num: undefined;
  };
  
  // universal variables to mark position place
  var a = check(arguments[0]);
  var b = check(arguments[1]);
  
  
  if (arguments.length == 2) {
    return a && b ? a + b : undefined;
  } else {
    if (a) {
      return function (nextArg) {
        return a && check(nextArg) ? a + nextArg : undefined;
      };
    } else {
      return undefined;
    }
  }
  
  
  
  
}

addTogether(2,3);


__________________________________________________________________________


//define a function that returns a boolean response test of a number to validate if it is a US telephone number
function telephoneCheck(str) {
  
   //return regular expression (regex) and .test the 'str'
   return (/^(1\s?)?(\(\d{3}\)|\d{3})[\s\-]?\d{3}[\s\-]?\d{4}$/gm).test(str);
  
}
//call the function, should return true
telephoneCheck("555-555-5555");


__________________________________________________________________________

// Setup JSON object of a record collection with key value pairs giving each album a reference number and listing album, artist, and tracks for each entry.
var collection = {
    "2548": {
      "album": "Slippery When Wet",
      "artist": "Bon Jovi",
      "tracks": [ 
        "Let It Rock", 
        "You Give Love a Bad Name" 
      ]
    },
    "2468": {
      "album": "1999",
      "artist": "Prince",
      "tracks": [ 
        "1999", 
        "Little Red Corvette" 
      ]
    },
    "1245": {
      "artist": "Robert Palmer",
      "tracks": [ ]
    },
    "5439": {
      "album": "ABBA Gold"
    }
};

// Keep a copy of the collection for tests
var collectionCopy = JSON.parse(JSON.stringify(collection));

//define function to update record collection by using bracket notation to update JSON object
function updateRecords(id, prop, value) {
  
  //if statement to check if the value of the 'prop' is not equal to tracks and if the value is empty, add the value to that empty property
  if (prop !== 'tracks' && value !== '') {
    collection[id][prop] = value;
  }
  //else if statement to check if the value of the 'prop' is equal to tracks and if the value is empty...
  else if (prop === 'tracks' && value !== ''){
    
    //if statement to check if the collection does not have a property of 'tracks' using .hasOwnProperty, then build a new 'prop' with an empty array
    if (!collection[id].hasOwnProperty(prop)){
      collection[id][prop] = [];
    }
    
    //.push the value to update the property
    collection[id][prop].push(value);

  //else if statement to check if the value is empty, then delete the property (which overwrites the value)
  } else if (value === ''){
    delete collection[id][prop];
  }
  
  //return the updated collection
  return collection;
}

// Alter values below to test your code
updateRecords(5439, "artist", "ABBA");

_________________________________________________________________________________________________________

//define function that can show the symmetric difference between individual arrays within an array.
function sym(args) {
  //helper function 1: individual array val filter to output new array with no repeats
  function dup(arr) {
    
    //define a newArr for the output
    var newArr = [];
    arr.forEach(function(value){
      if(newArr.indexOf(value) < 0) {
        newArr.push(value);
      }
    });
    return newArr;
  }
  
  //helper function 2: to combine arrays returning values that do not repeat.
  function finalArray(arr1, arr2) {
    var arr3 = arr1.concat(arr2);
    return arr3.filter(function(element, index, array){
      if (array.slice(0, index).indexOf(element) === -1 &&
         array.slice(index + 1).indexOf(element) === -1) {
        return element;
      }
    });
  }
  args = Array.prototype.slice.call(arguments);
  
  return args.reduce(function(a, b){
    a = dup(a);
    b = dup(b);
    a = finalArray(a, b);
    return a;
  });  
    
  
  
}

sym([3, 3, 3, 2, 5], [2, 1, 5, 7], [3, 4, 6, 6], [1, 2, 3], [5, 3, 9, 8], [1]);

_______________________________________________________________________________________

//Global Object
var money = [
  {name: 'ONE HUNDRED',  value: 100.00},
  {name: 'TWENTY',       value:  20.00},
  {name: 'TEN',          value:  10.00},
  {name: 'FIVE',         value:   5.00},
  {name: 'ONE',          value:   1.00},
  {name: 'QUARTER',      value:   0.25},
  {name: 'DIME',         value:   0.10},
  {name: 'NICKEL',       value:   0.05},
  {name: 'PENNY',        value:   0.01},
];

//define a function that simulates a monetary transaction with the variables of price, cash tendered, and cash in drawer.
function checkCashRegister(price, cash, cid) {
  var change = cash - price,
      
      //value reduced down to create new array to test if enough cash on hand
      till = cid.reduce(function(a, b){
        return a + b[1];
      }, 0.0).toFixed(2);
  
  //if statement to return a string if the till is less than or equal to change
  if (till < change) {
    return "Insufficient Funds";
  } else if (till == change) {
    return "Closed";
  }
  
  //reverse the cash in drawer to make sure the iteration is correct
  cid = cid.reverse();
  
  //
  var result = money.reduce(function(acc, next, index){
    if (change >= next.value) {
      var currentValue = 0.0;
      while (change >= next.value && cid[index][1] >= next.value) {
        currentValue += next.value;
        change -= next.value;
        change = Math.round(change * 100)/100;
        cid[index][1] -= next.value;
      }
      acc.push([next.name, currentValue]);
      return acc;
    }
    else {
      return acc;
    }
  }, []);
  
  
  //shorthand for if loop
  return result.length > 0 && change === 0 ? result : "Insufficient Funds";
}

// Example cash-in-drawer array:
// [["PENNY", 1.01],
// ["NICKEL", 2.05],
// ["DIME", 3.10],
// ["QUARTER", 4.25],
// ["ONE", 90.00],
// ["FIVE", 55.00],
// ["TEN", 20.00],
// ["TWENTY", 60.00],
// ["ONE HUNDRED", 100.00]]

checkCashRegister(19.50, 20.00, [["PENNY", 0.50], ["NICKEL", 0], ["DIME", 0], ["QUARTER", 0], ["ONE", 0], ["FIVE", 0], ["TEN", 0], ["TWENTY", 0], ["ONE HUNDRED", 0]]);

  
  
  
  return result;
}

// Example cash-in-drawer array:
// [["PENNY", 1.01],
// ["NICKEL", 2.05],
// ["DIME", 3.10],
// ["QUARTER", 4.25],
// ["ONE", 90.00],
// ["FIVE", 55.00],
// ["TEN", 20.00],
// ["TWENTY", 60.00],
// ["ONE HUNDRED", 100.00]]

checkCashRegister(19.50, 20.00, [["PENNY", 1.01], ["NICKEL", 2.05], ["DIME", 3.10], ["QUARTER", 4.25], ["ONE", 90.00], ["FIVE", 55.00], ["TEN", 20.00], ["TWENTY", 60.00], ["ONE HUNDRED", 100.00]]);

______________________________________________________________________

//define function to update an inventory array with a new inventory array
function updateInventory(arr1, arr2) {
  
  //set variable to hold the concatenated and reduced arrays
  var objInv = arr1.concat(arr2).reduce(function(acc, CurrentValue){
    if (acc[CurrentValue[1]]){
      acc[CurrentValue[1]] += CurrentValue[0];
    } else {
      acc[CurrentValue[1]] = CurrentValue[0];
    }
    return acc;
  }, {} );
  
  //return the object with the keys in alphabetical order with the proper values
  return Object.keys(objInv).sort().map(function(invKey){
    return [objInv[invKey], invKey];
  });
}

// Example inventory lists
var curInv = [
    [21, "Bowling Ball"],
    [2, "Dirty Sock"],
    [1, "Hair Pin"],
    [5, "Microphone"]
];

var newInv = [
    [2, "Hair Pin"],
    [3, "Half-Eaten Apple"],
    [67, "Bowling Ball"],
    [7, "Toothpaste"]
];

updateInventory(curInv, newInv);

__________________________________________________________________________	

function permAlone(str) {
  
  //change str to an array
  var arr = str.split(''),
  
  //establish a counter to start at 0
      counter = 0;
  
  //helper function to properly swap values of a and b
  function swap (a, b) {
    var tempArr = arr[a];
    arr[a] = arr[b];
    arr[b] = tempArr;
  }
  
  //function to generate the permutations using Heap's Algorithm
  function generate (n) {
    if (n===1 && !/([a-z])\1+/.test(arr.join(''))) {
      counter ++;
    } else {
      for (var i = 0; i !== n; i++){
        generate(n-1);
        swap(n % 2 ? 0 : i, n-1);
      }
    }
  }
  
  generate(arr.length);
  return counter; //could return the actual permutated array, but it may be lengthy.
  
}

permAlone('aab');

_______________________________________________________________________________________

//using object constructor, the code will allow identification and modification of the Person's name
var Person = function(firstAndLast) {
    
    //isolate the first name
    this.getFirstName = function() {
      return firstAndLast.split(" ")[0];
    };
    
    //isolate the last name
    this.getLastName = function() {
      return firstAndLast.split(" ")[1];
    };
    
    //return the full name
    this.getFullName = function() {
      return firstAndLast;
    };

    //return full name by replacing first name 
    this.setFirstName = function(name) {
      firstAndLast = name + " " + firstAndLast.split(" ")[1];
    };

    //return full name by replacing last name    
    this.setLastName = function(name) {
      firstAndLast = firstAndLast.split(" ")[0] + " " + name;
    };
    
    //return full name by replacing first and last name
    this.setFullName = function(name) {
      firstAndLast = name;
    };
   

 };

var bob = new Person('Bob Ross');
bob.getFullName();

______________________________________________________________________________________________

//define a function to determine the orbital period of an object in space
function orbitalPeriod(arr) {
  
  //define a variable to show the gravitational constant * mass of the object(earth) in km^3 s^-2
  var GM = 398600.4418;

  //define a variable to show the radius of the earth in km
  var earthRadius = 6367.4447;
  
  //for each object in the array create a function that uses object as the argument
  arr.forEach(function (object){

    //create a new key called orbitalPeriod and using math.round to return an integer, call 2 multiplied times PI, then find the square root of the earthRadius and avgAlt of the object to the 3rd power, finally divide by GM.
    object.orbitalPeriod = Math.round(2*Math.PI*Math.sqrt(Math.pow(earthRadius + object.avgAlt, 3)/ GM));
    
    //delete the avgAlt 
    delete object.avgAlt;
  });
  //return the updated array
  return arr;
}

//the following argument should return: [{"name":"sputnik","orbitalPeriod":86400}]
orbitalPeriod([{name : "sputnik", avgAlt : 35873.5553}]);

____________________________________________________________________________________________________

//define function to identify pairs of numbers in arr that equal arg && return the sum of their indicies
function pairwise(arr, arg) {
  
  //return arr by .reduce passing all of the available arguments
  return arr.reduce(function(acc, next, index, array){
  
    //for loop to cycle through array starting at index + 1
    for(var i = index + 1; i < array.length; i++){
      
      //if the array at the index position and i position equal the arg, then
      if(array[index] + array[i] === arg){
        
        //the acc equals index + 1 and itself
        acc += index + i;
        
        //once the array index positions have been identified, replace with Not a Number(NaN)
        array[index] = array[i] = NaN;
      }
    }
    
   //return the value of the acc 
   return acc;
    
  //make sure to define the start as 0  
  }, 0);
}

//the following should produce the result of 11
pairwise([1,4,2,3,0,5], 7);


# proDev
