# update the direction and velocity after collision on paddles

## Feature

Reports back with updated velocity of the pong ball and the
direction in which the ball will move

## Acceptance Criteria

### Scenario: either player A or player B hits the ball with paddle

  Given that the game is bug free

  When either player A or player B hits the ball with paddle

  Then calculate the updated velocity and direction with which the
  ball will now progress and return the data to the central module

### Scenario: the ball hits either top or bottom wall

  Given that the game is in progress and the pong ball is moving

  When the pong ball hits the top or bottom wall

  Then calculate the updated velocity and direction with which the
  ball will now progress and return the data to the central module
  