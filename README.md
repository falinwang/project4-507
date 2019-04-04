# SI 507 Project 4
- Name: Fa-lin Roy Wang
- Date: April 3, 2019

## which project option you chose
Option 2: Building a Pong game with the Pyglet library

## About
The project is about rewriting a 1-player Pong game. *The change I made here is changing the concept to hit the water ballons wall with the Brick! And it also shows updating scores when playing the game, also after fail or exit the game.* The water ballon wall is 6-deep floor-to-ceiling barricade of ballons.

![Homepage](https://github.com/falinwang/project4-507/blob/master/screenshot.png)


## Dependencies
```
future==0.17.1
pyglet==1.3.2
```

## Installation
To run project locally, follow these steps to setup your environment.

1. Create a folder for the project

2. Move to the project folder, create and activate a virtual environment:
      ```
      $> virtualenv env
      $> source env/bin/activate
      ```
3. Clone the repository:
      ```
      $> git clone https://github.com/falinwang/project4-507.git
      $> cd project4-507
      ```

4. Install requirements:

      `$> pip install -r 'requirements.txt'`

4. Run the application:

      `$> python SI507_project4.py`


## How to play the game

Use your keyboard to control the paddle:
- **W**: up
- **S**: down
- **P**: Pause the game
- **R**: Reset the game

To quit the game, press **Q** or **Esc**.
