# central-unit

## Feature

This module co-ordinates between all the modules for successful
game execution

## Acceptance Criteria

### Scenario: a new game starts

  Given that details of both the players are filled
  and user presses start game button

  When the game starts

  Then update interface module is called for the game progress

### Scenario: checking for collision

  Given the interface is updated every 10 milliseconds

  When the pong ball is progressing in its calculated direction

  Then keep checking for a collision every 10 milliseconds with either
  wall or paddles of players

### Scenario: collision with  side walls

  Given that the check collision interface is returning data properly
  
  When the collision is with the left or right side wall

  Then point capturing module is called

### Scenario: collision with paddle

  Given that the check collision interface is returning data properly

  When the collision returned is with the paddle of any one player

  Then the module used for updating velocity and direction is called

### Scenario: the collision is with upper and lower walls

  Given that the collision is with the upper and lower walls

  When the changed velocity and direction data is received by the module

  Then the module for updating interface is called with new details

### Scenario: game ends

  Given that either player A or player has earned 10 points

  When the point capture module returns winner data

  Then the module to end game is called
