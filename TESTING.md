# Testing

## Table of Contents

1. [**Testing Overview**](#testing-overview)
2. [**Validation**](#validation)
    - [**W3C Markup Validator results**](#w3c-markup-validator-results)
    - [**W3C CSS Validator results**](#w3c-css-validator-results)
    - [**JSHint Validation results**](#jshint-validation-results)
3. [**Testing User Stories from User Experience Section**](#testing-user-stories-from-user-experience-section)
4. [**Manual Testing on Live Site**](#manual-testing-on-live-site)
5. [**Jasmine Testing**](#jasmine-testing)
6. [**Bugs Discovered**](#bugs-discovered)

## Testing Overview

- The website was tested on Google Chrome, Mozilla Firefox, Opera, Safari and Microsoft Edge browsers.

- Using Chrome developer tools the responsive nature of the site was tested on the Moto G4, Galaxy S5, iPhone5/SE, iPhone 6/7/8, iPad and Surface Duo.

- The website was tested on real-life devices, namely a 14" Windows laptop, an Alcatel 1 Android Phone and an iPhone SE.

## Validation

- The [W3C Markup Validator](https://validator.w3.org/#validate_by_input) service was used to validate the HTML code of the project.
  
- The [W3C CSS Validator](https://jigsaw.w3.org/css-validator/#validate_by_input) service was used to validate the CSS code. No errors were found.

- [JSHint](https://jshint.com/) was used to validate the JavaScript code of the project.

### W3C Markup Validator results

- index.html

    - No errors were found. Two warnings were found - "The type attribute is unnecessary for JavaScript resources". This warning referred to the two scripts contained
    in the file. The code `type="text/javascript"` was deleted to remove this warning.

- game.html

    - No errors or warnings were found.

### W3C CSS Validator results 

- The CSS passed with no errors.

### JSHint Validation results

- Testing game.js

    - No major errors were found. Four warnings were produced, two were very minor and involved two missing semicolons which did not affect the running of 
    the program. The other two warnings stated that functions declared within loops referencing an outer scoped variable may lead to confusing semantics. 
    This referred to the variable activeColor and does not affect the running of the program. The functions could be refactored in subsequent updates.

- Testing utils.js

    - No major errors were found. Three warnings were produced, a semicolon was missing which was added and did not affect the running of the program. The 
    other two warnings stated that there was two undefined variables namely anime and emailjs. These were then declared inside the script to remove this warning. 
    The sendMail variable was declared as unused. This function is called in the form element of the index.html file.


## Testing User Stories from User Experience Section

- As a player, I want:
 
    1. A game that will help sharpen my memory, so I can boost my memory performance in other areas of my life.

        - Players of memory blocks are required to memorize the colour of between 9 and 25 squares in a grid depending 
        on the level they choose to play. The player also has to remember the colours within a certain time before the 
        countdown reaches zero. Keeping track of 9 items is a challenge in itself and so this game allows the player to 
        learn and practice skills such as the [mnemonic](https://en.wikipedia.org/wiki/Mnemonic) technique. Increasing your 
        short term memory helps in other areas of life such as remembering names and speeding up learning.

    2. A game that that has different levels of difficulty, so I can continue to challenge myself as my memory skills improve.

        - The game has three levels of difficulty, easy, medium and hard. Each jump in level significantly increases the difficulty of the game. 
        Moving from the easy level to medium level results in the number of coloured squares that need to be remembered increasing from 9 to 16, 
        an increase in 78%. The jump to the hard level increases the cells to 25 which is a 56% increase on the medium level and motivates the player 
        to work harder on their memory skills.

        <div align="center">
        <br>
        <img src="assets/images/testing_images/easy_level.png" alt="Screenshot: easy level">
        <img src="assets/images/testing_images/medium_level.png" alt="Screenshot: medium level">
        <img src="assets/images/testing_images/hard_level.png" alt="Screenshot: hard level">
        </div>

    3. To be able to keep track of my high score, so I can challenge myself to beat it.

        - At the end of every game, the player's score is calculated and compared to the current highscore. If they beat the highscore a message is 
        displayed congratulating them on achieving a new highscore. Their highscore is displayed at the top of the game page and is stored in the 
        local storage on their device. Therefore when they return to the website at a later date their highscore is still available and 
        displayed for them.
        
        <div align="center">
        <br>
        <img src="assets/images/testing_images/highscore.png" alt="Screenshot: high score message"><br><br>
        <img src="assets/images/testing_images/highscore_msg.png" alt="Screenshot: high score">
        </div>
          
    4. A game that I can play on all devices, so I can play it at any time or place.

        - Memory Blocks is a fully responsive website and can be played on all mobile phone devices as well as tablets, laptops and desktop computers.
 
- As a young player, I want:

    1. A game that is simple and intuitive to play, so I do not need to spend too much time learning how to play the game.

        - Memory Blocks is a very simple game to play, the goal of the game is to memorize a grid of coloured squares before a timer runs out. When 
        the timer reaches zero the coloured squares of the grid turn grey. Using their memory the player must then fill in the grid again. They simply
        choose a colour from the colour picker by clicking on it and then click on a square in the grid to fill that square with the chosen colour. The 
        game ends when the timer reaches zero. The player has the option to end the game before the timer runs out by clicking on the finish button. Messages
        are displayed a certain points during the game guiding the player on the relevant step to take such as memorizing the grid or filling in the grid.

        <div align="center">
        <br>
        <img src="assets/images/testing_images/playing_time.png" alt="Screenshot: playing time">
        </div>

    2. Easy controls for the game, so I can play the game comfortably and effortlessly.

        - The controls are easy to understand and implement. A series of click events are all that is required to play the game. The player simply clicks on the 
        relevant button to choose a level and clicks on the start button to play. To choose a colour they simply click on one of the coloured squares above the game grid. 
        The grid is filled in by clicking on each square of the grid. The game is ended by clicking on the finish button or by letting the timer run down. A 
        show solution button can then be clicked to show the correct solution. They can then click the play again button to start a new game. There is no typing 
        needed during the game so the use of a keyboard is not required. 

    3. A game that is fun and exciting to play, so I can share and play with my family and friends.

        - At the end of each game the player receives a score for their effort. They can then compete with family members and friends to try and beat each other's
        scores. A sense of competition brings entertainment and it motivates players to outperform others and allows them to assess their performance against the
        performance of others. The vibrant colour scheme of the website adds energy and the countdown timer adds tension to the game as the counter approaches zero.
         
        <div align="center">
        <br>
        <img src="assets/images/testing_images/score.png" alt="Screenshot: player score">
        </div>

- As an adult player or parent/grandparent, I want:

    1. A game I can play with my children/grandchildren, so I can spend more time having fun with them.

        - Memory Blocks is suitable for all ages. By challenging each other to beat their scores, Memory Blocks allows parent/grandparents to spend more fun time with 
        their children/grandchildren, all while developing and improving their memory skills.

    2. The ability to contact the developer of the game, so I can report any bugs or offer suggestions.

        - An email icon is provided on the home screen which when clicked opens a modal. The modal contains a contact form which the user can fill
        in to contact the site owner. A message is displayed on the home screen when the user fills out the form and sends it confirming whether or not the
        message was sent successfully.
        
        <div align="center">
        <br>
        <img src="assets/images/testing_images/contact_form.png" alt="Screenshot: contact form">
        </div>

    3. Simple instructions for the game, so I can easily learn how to play the game and instruct younger children how to play. 

        - A question mark icon is provided on the home screen which when clicked opens a modal. The modal contains a set of clear 
        and precise instructions on how to play the game.

        <div align="center">
        <br>
        <img src="assets/images/testing_images/instructions.png" alt="Screenshot: instructions">
        </div>

## Manual Testing on Live Site

- Home page

  1. Hovered over the icons to verify the hover colour change worked as expected.
  2. Clicked on the question mark icon to verify it opened the instructions modal.
  3. Hovered over the close button in the instructions modal to verify the hover colour change worked as expected.
  4. Clicked on the close button in the instructions modal to verify it closed.
  5. Clicked outside of the instructions modal to verify it closed.
  6. Clicked on the email icon to verify it opened the contact form modal.
  7. Hovered over the close button in the contact form modal to verify the hover colour change worked as expected.
  8. Clicked on the close button in the contact form modal to verify it closed.
  9. Clicked outside of the contact form modal to verify it closed.
  10. Tried to submit the form with empty fields to verify a warning message appeared.
  11. Tried to submit the form with an invalid email address to verify a warning message appeared.
  12. Submitted the form to verify that a message sent successfully appeared on the homepage.
  13. Clicked on the play button to verify it redirected to the game page.

- Game page - pre-game stage

  1. Hovered over the easy, medium and hard buttons to verify the hover colour change worked as expected.
  2. Hovered over the back arrow to verify the hover colour change worked as expected.
  3. Clicked the back arrow button to verify it redirected to the home page.
  4. Clicked the easy button to verify the grid changed to a 3 x 3 grid.
  5. Clicked the medium button to verify the grid changed to a 4 x 4 grid.
  6. Clicked the hard button to verify the grid changed to a 5 x 5 grid.
  7. Verified that the message displayed below the buttons changed for the appropriate button.
  8. Verified that the play button appeared when each of the buttons was clicked.
  9. Hovered over the play button to verify the hover colour change worked as expected.

- Game page - memorizing time stage - easy game

  1. Clicked the play button with easy game chosen to verify that the grid was filled with random colours.
  2. Verified that the play button and level buttons were hidden.
  3. Verified that the message "Memorize the grid..." displayed below the grid.
  4. Verified that the timer started at ten seconds and counted down to zero.
  5. Verified that the timer displayed "Go!" when it reached zero.
  6. Verified that the message "Fill in the grid" displayed when the timer reached zero.
  7. Verified that the Finish button displayed when the timer reached zero.
  8. Verified that each square of the grid turned grey when the timer reached zero.
  9. Verified the colour picker appeared above the grid when the timer reached zero.

- Game page - playing time stage - easy game

  1. Clicked on each of the colours of the colour picker to verify the border thickness of the clicked colour increased.
  2. Clicked on a square of the grid to verify its colour changed to that chosen in the colour picker.
  3. Repeated the above step for each of the colours.
  4. Verified that the timer started at 20 seconds and counted down to zero.
  5. Verified that when the timer reached 5 seconds the message displayed changed to "Hurry!".

- Game page - finished game time stage - easy game
  1. When the timer reached zero the following were verified:
        1. The colour picker was hidden.
        2. An "X" appeared on each square of the grid that was filled in incorrect.
        3. The opacity of the incorrect squares was reduced.
        4. The show solution and play again buttons were displayed.
        5. The message "Game Over!" was displayed.
        6. A message displaying the number of correct answers was displayed.
        7. A message with the player's score was displayed.
        8. A congratulations message was displayed below the grid when the highscore was beaten.
        9. The highscore at the top of the page updated when the highscore was beaten. 
        10. Verified that the highscore had the same value when the browser was closed and reopened.

  2. Clicked on the show solution button to verify that the colours of the grid changed to the correct colours.
  3. Clicked on the play again button to verify the game reset to the pre-game stage.

  All of the above tests were repeated under medium and hard game conditions with no errors found. The game plays the same for each level 
  of difficulty with just changes in the times and points as shown in the table below. 

    |                     	| Easy  	| Medium 	| Hard  	|
    |---------------------	|-------	|--------	|-------	|
    | Grid Size           	| 3 x 3 	| 4 x 4  	| 5 x 5 	|
    | Memorizing Time (s) 	| 10    	| 20     	| 30    	|
    | Playing Time (s)    	| 20    	| 40     	| 60    	|
    | Points per square     | 10    	| 20     	| 30    	|
    

## Jasmine Testing

The following functions were tested with [Jasmine](https://jasmine.github.io/index.html).

Functions that return a value:

- calculateMemorizingTime

- calculatePlayingTime

- getPoints

All the above functions passed the tests.

![Image](assets/images/testing_images/game_timers.png)

Functions that manipulate the User Interface:

- setUpEasyGame

- setUpMediumGame

- setUpHardGame

- resetGame 

All the above functions passed the tests.

![Image](assets/images/testing_images/setUpEasyGame.png)
![Image](assets/images/testing_images/setUpMediumGame.png)
![Image](assets/images/testing_images/setUpHardGame.png)
![Image](assets/images/testing_images/resetGame.png)

To view the results in your browser please clone the project repository by following the "Cloning the GitHub Repository" steps in the 
[README.md](https://github.com/Johnny-Morgan/memory-blocks/blob/master/README.md) 
and running the file [jasmine_testing.html](https://github.com/Johnny-Morgan/memory-blocks/blob/master/assets/jasmine_testing/jasmine_testing.html) 
in your browser.

## Bugs Discovered

 - On small devices, the words in the text for the tagline were breaking and wrapping on to the next line. This was due to an issue with the JavaScript 
code for the animation of the text. 

    ![Image](assets/images/testing_images/bug_smartphone.png)

    Fix: Disable the Javascript on small devices by adding the following code in the 
    [utils.js](https://github.com/Johnny-Morgan/memory-blocks/blob/master/assets/js/utils.js) file:

    ```javascript
    if (!(/iPhone|iPad|iPod|Android|webOS|BlackBerry|Opera Mini|IEMobile/i.test(navigator.userAgent))) {
        
    }
    ```

- The fields in the contact form modal were not clearing when the modal was closed. 

    Fix: added the following code to clear the three fields:

    ```javascript
    $('#contact').on('hidden.bs.modal', function (e) {
        $(this)
            .find("#name").val("").end()
            .find("#email").val("").end()
            .find("#message").val("").end();
    });
    ```
- When a game was being played for the first time, the highscore value was empty instead of displaying "0". The code was setting the 
variable highScore to 0 but the text value for the highscore div was not being updated. 

    Fix: added the following code when the highScore variable was being checked:

    ```javascript
    $("#high-score").html("0");
    ```

- When a player received a score that was equal to the highScore, a message congratulating the player on a new highscore was displayed. 
This was because the highscore variable was not being updated when it was beaten. 

    Fix: update the value of the highScore variable:

    ```javascript
    // Check for new high score
        if (score > highScore) {
            highScore = score;
            localStorage.setItem("highScore", score);
            $("#high-score").html(localStorage.getItem("highScore"));
            $(".high-score-message").html("Congratulations! New high score!");
        }
    ```
- The game grid could be changed during a game.

    Fix: hide the level selection buttons when the game starts. The div that contains the game level buttons was given a class of "game-level" and 
    the "hidden" class was added to the div when the play button was clicked. The "hidden" class gives the CSS property "display" a value of "none".

    ```javascript
   $(".game-level").addClass("hidden");
    ```

- If the play button was clicked more than once during gameplay the memorizingTime function was called again. This caused the timeInterval 
function to be called again, which lead to the memorizing timer to count down at a faster rate than normal.

    Fix: hide the play button when it is clicked to prevent the player from clicking it multiple times.

    ```javascript
   $("#play").addClass("hidden");
    ```
- The memorizing time was not calculated correctly if the player clicked between levels before pressing the play button. For example, 
if the player chose the easy level the boolean easyGame was set to true. However, if they then clicked on the medium level button, the mediumGame 
boolean was set to true. But the easyGame boolean still had a value of true. Therefore when the calculateMemorizingTime function was called it would return the value for an easyGame, as the first if statement is a check for an easyGame.

    Fix: when the easy button is clicked set the easyGame boolean to true and set the mediumGame and hardGame booleans to false. 
    Repeat for the medium and hard game button click events.

    ```javascript
   $("#easy").click(function () {
    easyGame = true;
    mediumGame = false;
    hardGame = false; 
    ```

- When the game finished, the score variable was always calculated as the highest score achievable. This was because the showWrongGuesses function 
was being called before calculateScore function. Calling the showWrongGuesses function first resulted in the playerColours array and the 
copyOfGridColours array both being empty. Therefore when the score was calculated, each index of each array was compared and evaluated to be the 
same (since they were both empty arrays). Hence the score and correctGuesses variables were incremented to the max score.

    Fix: call the showWrongGuesses function after calculateScore function.

- The footer was displaying in the middle of the home page on mobile devices when they were rotated to landscape mode.

    Fix: as the footer serves no purpose other than to show the developers name, it was decided to remove it on mobile devices. A responsive footer is a 
    feature that can be added in the future development of the site.

    ```
        /***** HIDE FOOTER ON MOBILE DEVICES*/
    @media (max-width: 823px) {
        footer {
            display: none;
        }
    }
    ```
    
- On Safari and Firefox browsers, the playing timer was starting before the memorizing timer finished causing the timers to countdown faster. 

    Fix: the number of milliseconds to wait before calling the playingTime function was increased. This bug was found late in testing and requires further investigation.

    ```javascript
   setTimeout(playingTime, (time + 1.1) * 1000); 
    ```