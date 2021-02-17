[![Work in Repl.it](https://classroom.github.com/assets/work-in-replit-14baed9a392b3a25080506f3b7b6d57f295ec2978f6f33ec97e36a161684cbe9.svg)](https://classroom.github.com/online_ide?assignment_repo_id=4147921&assignment_repo_type=AssignmentRepo)
# Candidate-Testing

// Welcome to your first assignment.
// Add your code here. You can do it!

const input = require('readline-sync');
let candidateName = input.question("Please Enter your Name:");
let score = 0;
console.log("Candidate Name: " + candidateName);
let quizArray = [
"1) True or false: 5000 meters = 5 kilometers.",
"2) (5 + 3)/2 * 10 = ?",
3) Given the array [8, "Orbit", "Trajectory", 45], what entry is at index 2?',
"4) Who was the first American woman in space?",
"5) What is the minimum crew size for the International Space Station (ISS)?"];
let correctAnswer = [
"True",
"40",
"Trajectory",
"Sally Ride",
"3"];
for(let i = 0; i < quizArray.length; i += 1){
let candidateResponse = input.question(quizArray[i]);
let input2 = candidateResponse.toLowerCase();
let smallLetters = correctAnswer[i].toLowerCase();

if (input2 === smallLetters) {
//console.log('Correct Answer');
score++;
} else {
//console.log('Wrong Answer');
}
console.log(`Your Answer: ${candidateResponse}`);
console.log(`Correct Answer: ${correctAnswer[i]}\n`);

}

let num = (score/(quizArray.length)*100);

console.log(`>>> Overall Grade: ${num}% (${score} of ${quizArray.length} responses correct) <<<`);

if (num < 80) {
console.log(">>> Status: Failed <<<");
} else {
console.log(">>> Status: Passed <<<");
}