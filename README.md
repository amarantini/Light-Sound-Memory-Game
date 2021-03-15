# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Qiru**

Time spent: **10** hours spent in total

Link to project: https://glitch.com/edit/#!/light-sound-memory-game-qiru
Live Site: https://light-sound-memory-game-qiru.glitch.me

## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked. 
* [X] Game buttons each light up and play a sound when clicked. 
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [X] Buttons use a pitch (frequency) other than the ones in the tutorial
* [X] More than 4 functional game buttons
* [X] Playback speeds up on each turn
* [X] Computer picks a different pattern each time the game is played
* [X] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [X] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![Loss the game](https://cdn.glitch.com/c900ee34-f91e-44e9-88f7-4f09930dbf98%2Floss.gif)
![Win the game](https://cdn.glitch.com/c900ee34-f91e-44e9-88f7-4f09930dbf98%2Fwin.gif)



## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 

I read the documents on w3schools.com on color picking and increasing margin and padding.
I searched for the methods to set up a count down timer on stackoverflow.
I google the frequency of the pinano note CDEFGA.

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

The biggest challenge I encountered is to set up a count-down timer using setInterval and clearInterval. I was unfamiliar with these two functions and had to search on W3Schools to look at how they work. I also looked at several examples on W3Schools and Stackoverflow to better understand how to set up a countdown clock. One difficulty of this task is the design of the countDown function. Following an example on W3Schools, I used Date().getTime() to count the time difference. But I soon realized this is unnecessary because setInterval is already counting the time for me. Therefore, I used a count variable to track the number of times countDown() is called and make sure the countDown function which is set to be run in an interval of 1000 ms is called exactly 20 times. The most difficult part is to know where to put setInterval and clearInterval in a complicated logic circuit. I wasn’t able to terminate the countDown() function in some cases and ran into an infinite loop even though I applied clearInterval(). I tried to debug by setting up breakpoints using console.log() and found that my clearInterval() was called correctly. I also searched for possible solutions on many different forums. And eventually, one suggestion works! When I put an extra clearInterval() before calling setInterval(), I was able to terminate the countDown() in the correct time. I realized that the cause of this bug might be that I was calling several setInterval() and countDown() at the same time as I modified guess() and stopGame() to reset countDown() and start over again at a new turn of guessing. I went through a painful debugging session but also learned about how functions were called and worked in a web app. 

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

I found that creating a small program in this way may be sufficient (i.e. simple file structure, all functions within one javascript file). However, when I try to add features, it becomes confusing. I can easily mess up the entire program by accidentally change a variable that is required for another function. Therefore, I feel that for a larger project, it is important to organize the code into components using techniques such as React and separate different functions into different files. In this way, we can better manage the code and reuse them in other places. Also, I found that it is difficult to test the functionality of my code, other than repeating the game again and again, in which case I could miss some bugs if I didn’t test all possible moves thoroughly. I would like to learn how to write small tests for each individual function and ensured that they worked as expected and ensure all lines of code are covered in tests. 

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

I would like to add some additional features to this game and rearrange the page layout to make it look nicer. I would like to center the title and the start/stop buttons. I would like to add difficulty levels and enable the users to choose. For example, in a simple game, a pattern consists of 6 elements. In a difficult game, a pattern can have 10-15 elements. Or the users can decide on the number of elements in the pattern freely. To do this, I need to add an input field for the users, either a dropdown list or a text field, and enable generatePattern() function to take user inputs and generate patterns according to user demands. I also want to reorganize the code into different components using React to help better manage the code.

## License

    Copyright [Qiru Hu]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.