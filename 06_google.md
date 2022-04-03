# Google


## Instructions
Create or use an existing programming task in a programming language of a class you are teaching (or would like to teach).
  - The task should involve multiple steps, ~5.
* Run a few internet searches that a student might run when presented with your task.
* In a markdown file:
  - Describe the task
  - For each search you ran provide three links from the results
    - Provide a critique on the result. Things to consider:
      - Was it useful?
      - Was it too simple/complex?
      - Was it unecessarily complicated?
      - Did it include copy/pastable code?
      - Did you learn from it/could a student learn from it?

---

## Task: Pong Remix
In the P5js course I teach, one of the assignments I have my students do is a remix of Pong. I give students the [starter code](06_pong.html), and they have to remix it however they want. Here are some ideas I give my students :
* game does not start until the user presses the mouse button
* speed up the ball upon collision with the paddle
* paddle gets shorter upon collision with the ball
* paddle is frozen when the ball is on the bottom half of the canvas
* paddle constantly gets shorter (slowly)
* mouse controls middle of paddle
* ball bounces based on where it hits paddle 
* pause feature
* score & lives
* score resets after last life lost
* two-player (keyboard)

## Search: "p5js pong remix"

### Result 1: [My former student](https://sites.google.com/a/hstat.org/aaliyahs9023--sep10/p5js/pongremixedproject)

Aaliyah's portfolio from 2017 is on Google Sites, which I had all students use, years ago. Since then, I have used portfolios for more open-ended and longer tasks, where A) there isn't an exact feature requested, and B) I can see students working on the code for a long period of time. Nonetheless, Aaliyah's code is public (and the #1 result on Google, mind you). Aaliyah added the score feature, which wasn't terribly difficult. What makes her code is unique is the ball/paddle/text colors, so if a future student's pong is red/yellow/green in the same combination, it would be pretty obvious that the student copy/pasted without even trying to learn from the score functionality of the `score = score + 1` section.

### Result 2: [2-player video walkthrough](https://www.youtube.com/watch?v=iEicBgGocUA)

This result walks through step-by-step how to make 2-player pong in the tradtional left-to-right orientation. If a student follows this, either A) they wouldn't change the orientation and it would be obvious they plagiarized, or B) they would figure out how to keep the orientation top-to-bottom, in which case a fair amount of learning would have to take place.

### Result 3: [Score, no game over, change bounce direction](https://editor.p5js.org/annawasson/sketches/BQFIoo6s2)

Here is a similar version of Pong to the base project I give, but with significantly different starter code. If a student copy/pasted this, the lack of "Game over" functionality would immediately be a red flag, but also the fact that the code is so different, that they would still have to dissect it enough to learn how to make the score increase.

### Result 4: [Former student, hearts/lives feature](https://github.com/elizabethv0218/p5js)

Here we find Elizabeth's entire p5js repo. Since those days of public repos, I have now started using Github Classroom to manage private repos. Nevertheless, Elizabeth's [pong remix](https://github.com/elizabethv0218/p5js/blob/master/pong-remix.html) adds on to the starter code in extremely complex ways. For example, she preloads a heart image to represent how many "lives" the player has. This is not something I have taught my students, so if a student copy/pastes, they would (at the very least) have to figure out how to use their own image, since copying/pasting Elizabeth's code doesn't immediately work. 

It's also worth noting that if a student copy/pastes _all_ of Elizabeth's code, it would be pretty apparent from the fact that we were using an older version of p5js (0.4.13) back in 2018. 

But if a student chooses to study how Elizabeth used the `scoreboard()`, `lives()`, and `instructions()` functions, they could learn a lot from her code.