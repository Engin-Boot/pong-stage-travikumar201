# check for collison on paddle or wall

## Feature

Reports back if the pong ball collided with the paddle or the walls

## Acceptance Criteria

### Scenario: the pong ball collides on the walls

  Given that the game is bug free

  When a collision is detected on the walls

  Then it is reported to the central controller with the details

### Scenario: when ball collides on the paddles

  Given that the game is bug free

  When either player A or player B hits the ball with their paddle

  Then it is reported to the central controller with latitude and
  longitude of the collision and which player hit it
  