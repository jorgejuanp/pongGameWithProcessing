# create Pong game With Processing
This is the Processing sketch I used to create a simple Pong game.

Controls for Left Player:
Q key: UP
A key: DOWN

Controls for Right Player:
Arrow keys: UP / DOWN

##Basic Process
1. **Idea**—Start with an idea.
2. **Parts**—Break the idea down into smaller parts.
....*Algorithm Pseudocode—For each part, work out the algorithm for that part in pseudocode. 
....*Algorithm Code—Implement that algorithm with code.
....*Objects—Take the data and functionality associated with that algorithm and build it into a
class.
3. **Integration**—Take all the classes from Step 2 and integrate them into one larger algorithm.


###1. THE IDEA
The object of this game is to have a ball bouncing on the top and bottom walls. 
Each player has to avoid the ball to get away through his side of the field. 
To make so, each player controls a paddle that moves from top to bottom (and viceversa),
in order to hit the ball. If the player hits the ball, it rebounds. 
If the ball gets away through one side, the player that scored, gets 1 point; 
the player that failed has to kick-off again.

###2. PARTS
  ####PART I
  Develop a program with a circle bouncing against all the walls on the screen
      **Setup:**
      ..*initialize Ball object
      **Draw:**
      ..*Erase background
      ..*Set Ball to initial position
      ..*Move Ball
      ..*Display Ball
      
      **Data:**
      ..*X and Y location
      ..*Radius
      ..*Speed in X and Y directions
      **Functions:**
      Constructor
        ..*Set initial X and Y location
        ..*Set X and Y speed
        ..*Set radius
      Move:
        ..*Increment X by speed in X direction
        ..*Increment Y by speed in Y direction
        ..*If Ball hits any edge, reverse direction
      Display:
        ..*Draw a circle at X and Y location
        
  ####PART II
  Make a rectangle whose Y position is controled by the user with the keyboard arrows; 
  make another rectangle whose Y position is controled by the user with the keyboard (other keys)
      **Setup:**
        ..*initialize Paddles, 
      **Draw:**
      ..*erase background
      ..*Set Paddles to initial position
      ..*Move Paddles depending on user keyboard
      ..*Display Paddles
      
      **Data:**
      ..*Initial X location (passing by argument) and Y location 
      ..*Paddle's width and height
      ..*Speed in Y direction
      **Functions:**
      Constructor
        ..*Set initial X and Y position
        ..*Set X to fixed
        ..*Set Y speed
      Move
        ..*Increment Y position when DOWN KEY is pressed
        ..*Decrement Y position when UP KEY is pressed
      Display
        ..*Draw two Paddles specifying its X location
      
  ####PART III
  Write a programm that tests if a rectangle and the ball intersect. This
  will be used to check if the ball hit the rectangle and has to rebound
      **Data:**
      ..*Ball X and Y location
      ..*Paddle X and Y location
      **Functions:**
      ..*check if Ball X position and Paddle X position converge
      ..*Check if Ball Y position and Paddle Y position converge
      ..*if X and Y converge, reverse Ball direction
      
  ####PART I CONTINUED
  Make the ball rebound only on top and bottom walls (not left, nor right).
  
  ####PART IV
  Kick-off: write a program that creates a new ball and moves it against the last 
  winner.
      Data:
      - new Ball initial X and Y position
      - new Ball direction
      Functions:
      - move Ball the oposite direction from where it got away
      
  ####PART V
  POINT! check if a ball got away and show who scored
  ####PART VI
  Score: write a program that keeps track of the score (how many points
  each user has) and shows it on the screen.
