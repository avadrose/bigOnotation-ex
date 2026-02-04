Big O Notation Exercise



Part 1: SImplifying Expressions

a. O(n + 10) → O(n)
b. O(100 * n) → O(n)
c. O(25) → O(1)
d. O(n² + n³) → O(n³)
e. O(n + n + n + n) → O(n)
f. O(1000 * log(n) + n) → O(n)
g. O(1000 * n * log(n) + n) → O(n log n)
h. O(2ⁿ + n²) → O(2ⁿ)
i. O(5 + 3 + 1) → O(1)
j. O(n + n^(1/2) + n² + n * log(n)^10) → O(n²)



Part 2: Calculating Time Complexity

function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
Time Complexity: O(n)

function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
Time Complexity: O(n)

function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
Time Complexity: O(1)

function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}
Time Complexity: O(n)

function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
}
Time Complexity: O(n^2)

function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";

  for (let char of str) {
    if(vowels.includes(char)) {
      if(char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
Time Complexity: O(n) **max keys is 10, space is O(1), time is still O(n)



Part 3: Short Answer 

a. True or false: n² + n is O(n²). → True
b. True or false: n² * n is O(n³). → True
c. True or false: n² + n is O(n). → False
d. Time complexity of .indexOf (array) → O(n)
e. Time complexity of .includes (array) → O(n)
f. Time complexity of .forEach (array) → O(n)
g. Time complexity of .sort (array) → O(n log n) (typical/average; algorithm-dependent)
h. Time complexity of .unshift (array) → O(n)
i. Time complexity of .push (array) → O(1) (amortized)
j. Time complexity of .splice (array) → O(n)
k. Time complexity of .pop (array) → O(1)
l. Time complexity of Object.keys() → O(n) (n = number of keys)


Bonus: 
Space complexity of Object.keys() → O(n) (it creates an array of all keys)