# update user experience

## Feature

Changes the frames of the screen as the ball moves ahead

## Acceptance Criteria

### Scenario: New game has started

  Given that the game is bug free

  When a new game starts

  Then the ball starts moving in a random direction

### Scenario: when collision is detected

  Given that either player A or player B hit the ball with their paddle

  When the velocity and direction of the ball movement is decided

  Then the user interface changes at a rate of 30 frames per second
  and the ball moves in the decided direction with the decided velocity

### Scenario: when ball collides on wall

  Given that the game is bug free

  When the pong ball hits either side of the wall

  Then the user interface is reset and a new set starts