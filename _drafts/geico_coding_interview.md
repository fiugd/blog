2024-09-24

task:
replace 'aa' with 'b'
replace 'bb' with 'c'
etc, up to 'zz'
explain the operational and space complexity of your solution

```javascript
/* DURING THE INTERVIEW 1 */

const bumpChar = (char) => {
  const i = char.charCodeAt(0) + 1;
  return String.fromCharCode(i);
  // const map = 'abcdefghijklmnopqrstuvwxyz';
  // const i = map.indexOf(char);
  // return map[i+1];
};

function solution(N) {
  // create a string with all a's
  let filled = new Array(N).fill().map((x) => "a");

  let keepGoing = true;
  while (keepGoing) {
    let transformed = "";
    for (var point = 0; point < filled.length; point += 2) {
      const currentChar = filled[point];
      const isRepeat = currentChar === filled[point + 1];

      if (filled[point] === "z") {
        keepGoing = false;
        break;
      }

      // at first of word & no repeat
      if (!isRepeat && point === 0) {
        keepGoing = false;
        const rest = filled.slice(point);
        transformed += rest;
        break;
      }
      // found not repeat, but is not at first
      if (!isRepeat) {
        const rest = filled.slice(point);
        transformed += rest;
        break;
      }
      // repeat
      const mapped = bumpChar(currentChar);
      transformed += mapped;
    }
    filled = transformed;
  }
  return filled;
}

/* DURING THE INTERVIEW 2 */

// function solution(N) {
//     // create a string with all a's
//     let filled = new Array(N).fill().map(x => 'a');

//     const iterate = (filled) => {
//         let transformed = ''
//         for(var point=0;point<filled.length;point+=2){
//             const currentChar = filled[point];
//             const isRepeat = currentChar === filled[point+1];
//             if(filled[point] === 'z'){
//                 keepGoing = false;
//                 return filled;
//             }
//             // at first of word & no repeat
//             if(!isRepeat && point===0){
//                 keepGoing = false;
//                 const rest = filled.slice(point);
//                 return transformed + rest;
//             }
//             // found not repeat, but is not at first
//             if(!isRepeat){
//                 const rest = filled.slice(point);
//                 return transformed + rest;
//             }
//             // repeat
//             const mapped = bumpChar(currentChar);
//             transformed += mapped;
//         }
//         return iterate(transformed)
//     }

//     return iterate(filled);
// }

//You can get a codepoint* from any index in a string using String.prototype.charCodeAt. If your string is a single character, you’ll want index 0, and the code for a is 97 (easily //obtained from JavaScript as 'a'.charCodeAt(0)), so you can just do:

//s.charCodeAt(0) - 97
//And in case you wanted to go the other way around, String.fromCharCode takes Unicode codepoints* and returns a string.

//String.fromCharCode(97 + n)

/* AFTER THE INTERVIEW 1 */

function solutionSimple(N) {
  const alphabet = "zyxwvutsrqponmlkjihgfedcba".split("");
  let result = "";
  let remaining = N;
  for (const [i, char] of alphabet.entries()) {
    const power = Math.pow(2, 25 - i);
    if (remaining < power) continue;
    const quotient = Math.floor(remaining / power);
    result += char.repeat(quotient);
    remaining -= quotient * power;
  }
  return result;
}

const answer = solutionSimple(5);
//const answer = solutionSimple(Math.pow(2, 25) + 1);
new Array(10).fill().forEach((x, i) => {
  console.log(solutionSimple(i + 1));
});
console.log(solutionSimple(Math.pow(2, 25)));
console.log(solutionSimple(Math.pow(2, 25) + 1));

console.log(solutionSimple(10000000000));
```
