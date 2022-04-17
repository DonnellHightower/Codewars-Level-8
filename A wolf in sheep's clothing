https://www.codewars.com/kata/5c8bfa44b9d1192e1ebd3d15/train/javascript

If the wolf is the closest animal to you, return "Pls go away and stop eating my sheep". Otherwise, return "Oi! Sheep number N! You are about to be eaten by a wolf!" where N is the sheep's position in the queue.

Note: there will always be exactly one wolf in the array.

Examples
Input: ["sheep", "sheep", "sheep", "wolf", "sheep"]
Output: "Oi! Sheep number 1! You are about to be eaten by a wolf!"

Input: ["sheep", "sheep", "wolf"]
Output: "Pls go away and stop eating my sheep"

solution

function warnTheSheep(queue) {
  let sheepPos = queue.length - queue.indexOf('wolf') -1
  if (sheepPos == 0){
    return `Pls go away and stop eating my sheep`
  } else {
  return `Oi! Sheep number ${sheepPos}! You are about to be eaten by a wolf!`
 }   
}

sample tests

const strictEqual = require('chai').assert.strictEqual;

function doTest (queue, expected) {
	const log = `for queue [${queue.join(', ')}]\n`;
	const actual = warnTheSheep(queue);
	strictEqual(actual, expected, log);
}

describe("Fixed tests", function() {
  it("Tests", function() {
    doTest(["sheep", "sheep", "sheep", "sheep", "sheep", "wolf", "sheep", "sheep"],
		"Oi! Sheep number 2! You are about to be eaten by a wolf!"
	);
    doTest(["sheep", "wolf", "sheep", "sheep", "sheep", "sheep", "sheep"],
		"Oi! Sheep number 5! You are about to be eaten by a wolf!"
	);
    doTest(["wolf", "sheep", "sheep", "sheep", "sheep", "sheep", "sheep"],
		"Oi! Sheep number 6! You are about to be eaten by a wolf!"
	);
    doTest(["sheep", "wolf", "sheep"],
		"Oi! Sheep number 1! You are about to be eaten by a wolf!"
	);
    doTest(["wolf"],
		"Pls go away and stop eating my sheep"
	);
    doTest(["sheep", "sheep", "wolf"],
		"Pls go away and stop eating my sheep"
	);
  });
});
