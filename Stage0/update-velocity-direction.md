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
  