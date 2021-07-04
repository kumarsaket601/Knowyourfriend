# Knowyourfriend

var readlineSync = require('readline-sync');
const chalk = require('chalk');
 var score = 0;
var userName = readlineSync.question(chalk.blue('whats your name?'));

console.log("\n Welcome! " + userName + ", lets find How much you know about Dhoni");

console.log("\n");

function play(question , answer){

  var userAnswer = readlineSync.question(question);

  if(userAnswer == answer){
    console.log(chalk.green("right"));
    score = score + 1;
   
   console.log("----------");
  
  }else{
    console.log(chalk.red("wrong"));
    console.log("----------");
    score = score - 1;
  }
}




var questions = [{

  question : "In which year did he lead India to their second Cricket World Cup win? \n\n a.2011\n b.2013\n c.2007\n d.2009\n",
  
  answer : "a"
},

 questionTwo = {
  question : " Back in his early days, which junior cricket club did Dhoni play for? \n\n a.Central  coalfields limited\n b.Bokaro  power plant sports\n c.Ranchi Police Junior\n d.Bengal cricket  junior\n",
  answer : "a"
  
},

 questionThree = {
   question : " How many runs did he score before getting run out in his debut ODI match against Bangladesh? \n\n a.100\n b.71\n c.23\n d.0\n",
   answer : "d"

 },

 questionFour = {
   question : "  In how many matches did he become the fastest to top the ICC ODI batsmen ranking?  \n\n a.63\n b.42\n c.24\n d.15\n",
   answer : "b"
 },

  questionFive = {
   question : "On how many occasions did he finish ODI matches with a sixer?  \n\n a.Three\n b.One\n c.Nine\n d.Six\n",
   answer : "c"
  }];

for( var i = 0 ; i < questions.length ; i++){
  
  var vote = questions[i];
  play(vote.question, vote.answer);
  console.log(chalk.green(score));
}

console.log("Your final scroe is: ", score);



