function analyzeSentence(sentence) {
  // Initialize counters
  let length = 0;
  let wordCount = 0;
  let vowelCount = 0;

  // Define the vowels
  const vowels = 'aeiou';

  // Split the sentence into words based on spaces
  const words = sentence.split(' ');

  // Count the number of words
  wordCount = words.length;

  // Iterate through each character in the sentence
  for (let char of sentence) {
    // Increment the length counter
    length++;

    // Check if the character is a vowel
    if (vowels.includes(char.toLowerCase())) {
      vowelCount++;
    }
  }

  // Return the results as an object
  return {
    length: length,
    wordCount: wordCount,
    vowelCount: vowelCount
  };
}

// Example usage
const result = analyzeSentence("Hello world. This is a test.");
console.log(result); 
// Output: { length: 26, wordCount: 6, vowelCount: 8 }
