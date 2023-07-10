1 . Do the below programs in anonymous function & IIFE

Print odd numbers in an array

Using anonymous function:

const printOddNumbers = function(arr) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] % 2 !== 0) {
      console.log(arr[i]);
    }
  }
};

printOddNumbers([1, 2, 3, 4, 5]);

Using IIFE:

(function(arr) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] % 2 !== 0) {
      console.log(arr[i]);
    }
  }
})([1, 2, 3, 4, 5]);

Convert all the strings to title caps in a string array

Using anonymous function:

const convertToTitleCaps = function(arr) {
  for (let i = 0; i < arr.length; i++) {
    arr[i] = arr[i][0].toUpperCase() + arr[i].slice(1);
  }
  return arr;
};

console.log(convertToTitleCaps(["hello", "world"]));

Using IIFE:

const titleCaps = (function(arr) {
  for (let i = 0; i < arr.length; i++) {
    arr[i] = arr[i][0].toUpperCase() + arr[i].slice(1);
  }
  return arr;
})(["hello", "world"]);

console.log(titleCaps);



Sum of all numbers in an array

Using anonymous function:

const sumArray = function(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
};

console.log(sumArray([1, 2, 3, 4, 5]));

Using IIFE:

const sum = (function(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
})([1, 2, 3, 4, 5]);

console.log(sum);


Return all the prime numbers in an array

Using anonymous function:

const getPrimeNumbers = function(arr) {
  const isPrime = function(num) {
    if (num <= 1) {
      return false;
    }
    for (let i = 2; i <= Math.sqrt(num); i++) {
      if (num % i === 0) {
        return false;
      }
    }
    return true;
  };

  const primeNumbers = [];
  for (let i = 0; i < arr.length; i++) {
    if (isPrime(arr[i])) {
      primeNumbers.push(arr[i]);
    }
  }
  return primeNumbers;
};

console.log(getPrimeNumbers([1, 2, 3, 4, 5, 6, 7, 8, 9]));

Using IIFE:
const primeNumbers = (function(arr) {
  const isPrime = function(num) {
    if (num <= 1) {
      return false;
    }
    for (let i = 2; i <= Math.sqrt(num); i++) {
      if (num % i === 0) {
        return false;
      }
    }
    return true;
  };

  const primeNumbers = [];
  for (let i = 0; i < arr.length; i++) {
    if (isPrime(arr[i])) {
      primeNumbers.push(arr[i]);
    }
  }
  return primeNumbers;
})([1, 2, 3, 4, 5, 6, 7, 8, 9]);

console.log(primeNumbers);



Return all the palindromes in an array
Using anonymous function:

const getPalindromes = function(arr) {
  const isPalindrome = function(str) {
    const reversedStr = str.split('').reverse().join('');
    return str === reversedStr;
  };

  const palindromes = [];
  for (let i = 0; i < arr.length; i++) {
    if (isPalindrome(arr[i])) {
      palindromes.push(arr[i]);
    }
  }
  return palindromes;
};

console.log(getPalindromes(["hello", "world", "level", "racecar"]));

Using IIFE:

const palindromes = (function(arr) {
  const isPalindrome = function(str) {
    const reversedStr = str.split('').reverse().join('');
    return str === reversedStr;
  };

  const palindromes = [];
  for (let i = 0; i < arr.length; i++) {
    if (isPalindrome(arr[i])) {
      palindromes.push(arr[i]);
    }
  }
  return palindromes;
})(["hello", "world", "level", "racecar"]);

console.log(palindromes);



Return median of two sorted arrays of the same size.

Using anonymous function:

const findMedian = function(arr1, arr2) {
  const mergedArray = [...arr1, ...arr2].sort((a, b) => a - b);
  const mid = mergedArray.length / 2;
  
  if (mergedArray.length % 2 === 0) {
    return (mergedArray[mid - 1] + mergedArray[mid]) / 2;
  } else {
    return mergedArray[Math.floor(mid)];
  }
};

console.log(findMedian([1, 3, 5], [2, 4, 6]));

Using IIFE:

(function(arr1, arr2) {
  const mergedArray = [...arr1, ...arr2].sort((a, b) => a - b);
  const mid = mergedArray.length / 2;
  
  if (mergedArray.length % 2 === 0) {
    console.log((mergedArray[mid - 1] + mergedArray[mid]) / 2);
  } else {
    console.log(mergedArray[Math.floor(mid)]);
  }
})([1, 3, 5], [2, 4, 6]);


Remove duplicates from an array

Using anonymous function:

const removeDuplicates = function(arr) {
  return arr.filter((value, index, self) => self.indexOf(value) === index);
};

console.log(removeDuplicates([1, 2, 3, 3, 4, 5, 4, 6]));

Using IIFE:

(function(arr) {
  const uniqueArray = arr.filter((value, index, self) => self.indexOf(value) === index);
  console.log(uniqueArray);
})([1, 2, 3, 3, 4, 5, 4, 6]);


Rotate an array by k times:

Using anonymous function:
const rotateArray = function(arr, k) {
  for (let i = 0; i < k; i++) {
    arr.push(arr.splice(0, 1)[0]);
  }
  return arr;
};

console.log(rotateArray([1, 2, 3, 4, 5], 3));

Using IIFE:

(function(arr, k) {
  for (let i = 0; i < k; i++) {
    arr.push(arr.splice(0, 1)[0]);
  }
  console.log(arr);
})([1, 2, 3, 4, 5], 3);



Do the below programs in arrow functions.

Print odd numbers in an array
const printOddNumbers = (arr) => {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] % 2 !== 0) {
      console.log(arr[i]);
    }
  }
};

printOddNumbers([1, 2, 3, 4, 5]);

Convert all the strings to title caps in a string array

const convertToTitleCaps = (arr) => {
  for (let i = 0; i < arr.length; i++) {
    arr[i] = arr[i][0].toUpperCase() + arr[i].slice(1);
  }
  return arr;
};

console.log(convertToTitleCaps(["hello", "world"]));

Sum of all numbers in an array

const sumArray = (arr) => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
};

console.log(sumArray([1, 2, 3, 4, 5]));

Return all the prime numbers in an array

const getPrimeNumbers = (arr) => {
  const isPrime = (num) => {
    if (num <= 1) {
      return false;
    }
    for (let i = 2; i <= Math.sqrt(num); i++) {
      if (num % i === 0) {
        return false;
      }
    }
    return true;
  };

  const primeNumbers = [];
  for (let i = 0; i < arr.length; i++) {
    if (isPrime(arr[i])) {
      primeNumbers.push(arr[i]);
    }
  }
  return primeNumbers;
};

console.log(getPrimeNumbers([1, 2, 3, 


Return all the palindromes in an array

const getPalindromes = (arr) => {
  const isPalindrome = (str) => {
    const reversedStr = str.split('').reverse().join('');
    return str === reversedStr;
  };

  const palindromes = arr.filter((word) => isPalindrome(word));
  return palindromes;
};

console.log(getPalindromes(["hello", "world", "level", "racecar"]));
