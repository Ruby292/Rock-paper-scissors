<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
<script>
     function getComputerChoice() {
        let choices = ["rock", "paper", "scissors"];
        let computerChoice = choices[Math.floor(Math.random()*choices.length)];
        console.log(computerChoice);
        return computerChoice;
    }
    getComputerChoice();
    let comptLength = getComputerChoice();
    let compResult = comptLength.length;
    let playerChoice = prompt("Please insert your selection:","");
    let playerResult = playerChoice.length;
    if (playerResult === compResult) {
        alert(`${comptLength} and ${playerChoice}. You think exactly like computer!`);
    } else if ( playerResult > compResult) {
        let comparison1 = playerResult - compResult;
        switch (comparison1) {
            case 4:
                alert(`${comptLength} and ${playerChoice}. Opps! You lose this round.`);
                break;
            default:
                alert(`${comptLength} and ${playerChoice}. You win. Congratulations!`);
        } 
    } else if ( playerResult < compResult) {
        let comparison2 = compResult - playerResult;
        switch (comparison2) {
            case 4:
                alert(`${comptLength} and ${playerChoice}. You win. Congratulations!`);
                break;
            default:
                alert(`${comptLength} and ${playerChoice}. Opps! You lose this round.`);
        }
    }
    
</script>
</body>
</html># Rock-paper-scissors