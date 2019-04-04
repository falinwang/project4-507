The tasks in this list roughly correspond to changing the code for the Pong game (https://en.wikipedia.org/wiki/Pong) in basepong.py to a game (vaguely) like Breakout (https://en.wikipedia.org/wiki/Breakout_(video_game)).

For Project 4 Option 2, you should complete the following tasks for the game -- as well as one new game feature (a new image, a new mechanism, a key you can press that does something...) of your own creation/choosing.

* Change the starting Ball angle to `angle = random.randint(10, 75)`, so you can have a reasonable starting angle for a one-player game where hitting the right side of the game doesn't earn a point, it just bounces off.

* Change the `Ball`'s `initial_x` to `20` and `initial_y` to `20` so that the Ball starts in a reasonable place for a one player game.

* Make these changes to `Game.__init__` so that you can play a one-player game:

    * Remove the 2nd player's paddle

    * Make the right-hand wall deflect the ball back instead of scoring a point? (Hint: make it
    # an instance of a different class.)

* Make a 6-deep floor-to-ceiling barricade of bricks on the right side of the game, that looks somewhat like this: https://www.dropbox.com/s/x3hvmhw7j0za0z0/Screenshot%202019-03-26%2019.43.10.png?dl=0

    * HINT: Examples provided that create walls will be helpful here.

    * HINT: Each thing in the window is just another game object... what's its image? How can you do some simple math and iteration to figure out where the images should each go? Drawing it out is VERY helpful.

    * HINT: How would you make one column of bricks, using a for loop? The x position will be fixed, but the y position will get larger with each successive iteration. You can calculate how many bricks are needed, and thus how many times to iterate, by dividing the window height by the height of a brick.

        * And how would you make a set of six columns? Another for loop, iterating six times. On each iteration the x position is larger, and then you use the inner loop to create one column of bricks.

    * Test this to make sure it works before going on.

* Make bricks disappear when hit by making a `Brick` subclass of `BallDeflector` and switching your bricks from problem 2 to be instances of `Brick` instead of `BallDeflector`. (Hint: if you worked on Problem 2 in a "neat" way, you shouldn't have to change much code at all to do this.)

    * Hints on how to do this:
        * Make the Brick subclass
        * Create a `deflect_ball()` method for it. In that method,  
            * call the parent class's `deflect_ball()` method, so that the ball deflects normally.
            * get the game's list of game_objects, and call the `.remove()` method on it to remove the current brick. That way, when the game tells all of it's game_objects to display themselves, this brick won't display. Also, when the ball tries to see if it's run into any other game objects, it won't check with this brick any more.

        * THEN, Make the bricks be instances of the new `Brick` class instead of the `BallDeflector` class.

* Keep track of how many bricks have been hit. Every 10th brick, increase the ball velocity. (HINT: An example that will be available also shows code that does something like this.)

* Note also that the score display is difficult to deal with in this scenario, and that's OK, and it's OK to ignore it if you like, but if you choose to keep track of score in some way -- that's a cool new feature you could implement! -- you can still keep track of it in the code and print it to the command prompt, and that's perfectly fine (should you choose to pursue that path forward for your own feature, you can decide what it means to earn a point).
