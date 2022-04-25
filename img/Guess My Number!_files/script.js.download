'use strict';

// console.log(document.querySelector('.message').textContent);
// document.querySelector('.message').textContent = 'Correct';
// document.querySelector('.number').textContent = 13;
// document.querySelector('.score').textContent = 20;
// document.querySelector('.guess').value = 23;
// console.log(document.querySelector('.guess').value);

let secretNum = Math.trunc(Math.random() * 20) + 1;
let score = 20;
let highscore = 0;

const displayMessage = function (message) {
  document.querySelector('.message').textContent = message;
};

document.querySelector('.check').addEventListener('click', function () {
  const guess = Number(document.querySelector('.guess').value);
  console.log(guess, typeof guess);

  //When there is no input
  if (!guess) {
    // alert((document.querySelector('.message').textContent = 'No Number!'));
    displayMessage('No Number!');

    //When Player wins
  } else if (guess === secretNum) {
    displayMessage('Correct 😉');
    document.querySelector('.number').textContent = secretNum;
    document.querySelector('body').style.backgroundColor = 'green';

    if (score > highscore) {
      highscore = score;
      document.querySelector('.highscore').textContent = highscore;
    }

    //When the number is to high
  } else if (guess !== secretNum) {
    if (score > 1) {
      displayMessage(guess > secretNum ? 'To High 🤪' : 'To low🤣');
      score = score - 1;
    } else {
      displayMessage('Game Over!');
      document.querySelector('.score').textContent = 0;
    }
  }
  // } else if (guess > secretNum) {
  //   if (score > 1) {
  //     document.querySelector('.message').textContent = 'To High!';
  //     score = score - 1;
  //   } else {
  //     document.querySelector('.message').textContent = 'Game Over!';
  //     document.querySelector('.score').textContent = 0;
  //   }

  //   //When the number is to low
  // } else if (guess < secretNum) {
  //   if (score > 1) {
  //     document.querySelector('.message').textContent = 'To Low Darling!';
  //     score = score - 1;
  //     document.querySelector('.score').textContent = score;
  //   } else {
  //     document.querySelector('.message').textContent = 'Game Over!';
  //     document.querySelector('.score').textContent = 0;
  //   }
  // }
});
document.querySelector('.again').addEventListener('click', function () {
  score = 20;
  secretNum = Math.trunc(Math.random() * 20) + 1;
  displayMessage('Start guessing...');
  document.querySelector('.score').textContent = score;
  document.querySelector('.number').textContent = '?';
  document.querySelector('.guess').value = '';
  document.querySelector('body').style.backgroundColor = '#5d5857';
});
