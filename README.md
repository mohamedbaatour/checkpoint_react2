# checkpoint_react2// task 1
let sentence = prompt("This is a sentence:");


let wordCount = 1;
let vowelCount = 0;
let characterCount = 0;


for (let i = 0; i < sentence.length; i++) {
  let char = sentence[i];


  if (char === " ") {
    wordCount++;
  }

  if (char.match(/[aeiou]/gi)) {
    vowelCount++;
  }

  characterCount++;
}


console.log(`Word count: ${wordCount}`);
console.log(`Vowel count: ${vowelCount}`);
console.log(`Character count: ${characterCount}`);

//task 2
function sumDistinctElements(set1, set2) {
  const distinctElements = [];

  for (let i = 0; i < set1.length; i++) {
    if (!set2.includes(set1[i])) {
      distinctElements.push(set1[i]);
    }
  }

  for (let i = 0; i < set2.length; i++) {
    if (!set1.includes(set2[i])) {
      distinctElements.push(set2[i]);
    }
  }

  return distinctElements.reduce((sum, element) => sum + element, 0);
}
