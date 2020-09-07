# game-ends

## Feature

Once a player wins, a new page opens asking for restart or exiting game

## Acceptance Criteria

### Scenario: either player A or player B wins the game

  Given that player chooses to replay the game

  When the user presses replay button

  Then the central unit calls update user interface module
  and game starts with saved user details

### Scenario: user chooses to end the game

  Given that user chooses to end game

  When the user presses end button

  Then the players exit and game ends
  