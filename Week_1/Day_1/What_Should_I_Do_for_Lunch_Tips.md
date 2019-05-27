### Tips

Try experimenting with the comparison operators (`<`, `>`, `===`, etc.) in the node REPL, which you can launch using the `node` command in Vagrant.

Work on your code iteratively – that means in small pieces.

To help you figure out how to use `hungry` and `availableTime` inside your function, try outputting their values to the Terminal as follows.

'''javascript

function whatToDoForLunch(hungry, availableTime) {
  let whatToDo = "";
  if (hungry === false) {
    whatToDo = "Get back to work.";
  } else if (hungry === true) {
    if (availableTime < 20) {
      whatToDo = "Pick something up and eat it in the lab.";
    } else if (availableTime >= 20 && availableTime <= 30) {
      whatToDo = "Try a place nearby.";
    } else if (availableTime > 30) {
      whatToDo = "This is a bootcamp after all and you should probably reconsider."
    }
  }

  console.log(whatToDo);
}


/*
 * This is some test runner code that's simply calling our whatToDoForLunch function
 * defined above to verify we're making the right decisions. Do not modify it!
 */

console.log("I'm hungry and I have 20 minutes for lunch.");
whatToDoForLunch(true, 20);
console.log("---");

console.log("I'm hungry and I have 50 minutes for lunch.");
whatToDoForLunch(true, 50);
console.log("---");

console.log("I'm not hungry and I have 30 minutes for lunch.");
whatToDoForLunch(false, 30);
console.log("---");

console.log("I'm hungry and I have 15 minutes for lunch.");
whatToDoForLunch(true, 15);

'''