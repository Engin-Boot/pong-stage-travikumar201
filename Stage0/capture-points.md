# capture points and declare winner

## Feature

Adds ppoints to players existing score

## Acceptance Criteria

### Scenario: either of the players misses the ball

  Given that the game is bug free

  When player A misses the ball and the ball hits the side walls

  Then the score of player B is increased by one and vice versa

### Scenario: first to earn 10 points

  Given that the game is bug free

  When either player A or player B reaches 10 points first

  Then that player is declared winner and this data is sent to
  central module
  