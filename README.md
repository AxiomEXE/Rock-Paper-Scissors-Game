# Rock-Paper-Scissors-Game
```markdown

const getUserChoice = userInput => {
  userInput = userInput.toLowerCase();
  if (userInput === 'rock' || 'paper' || 'scissors'){
    return userInput;
  } else {
    console.log('Error Alert!');
  }
}

const getComputerChoice = () =>{
  const randomNumber = Math.floor(Math.random() * 3);
  switch(randomNumber){
    case 0:
      return 'rock';
    case 1:
      return 'paper';
    case 2:
      return 'scissors';
  } 
};

const determineWinner = (userChoice, computerChoice) =>{
  if (userChoice === 'bomb'){
    return 'Congrats, you win everything.'
  }
  if (userChoice === computerChoice){
    return 'This game is a tie!';
  };
  if (userChoice ==='rock'){
    if (computerChoice ==='paper'){
      return 'The Computer Wins!'
    } else {
      return 'The User Wins!'
    }
  }
  if (userChoice ==='paper'){
    if (computerChoice === 'scissors'){
      return 'The Computer Wins!'
    } else {
      return 'The User Wins!'
    }
  }
  if (userChoice ==='scissors'){
    if (computerChoice ==='rock'){
      return 'The Computer Wins!'
    } else {
      return 'The User Wins!'
    }
  }
}

const playGame = () => {
  const userChoice = getUserChoice('bomb');
  const computerChoice = getComputerChoice();
  console.log(`You chose ${userChoice}.`);
  console.log(`The computer chose ${computerChoice}.`)
  console.log(determineWinner(userChoice, computerChoice));
}

playGame();

```
