# game-setup

## Feature

This page helps in setting up the game in accordance to single or double player mode

## Acceptance Criteria

### Scenario: Change theme locally

  Given that themes are available locally

  When player chooses a particular theme

  Then apply that theme in the game

### Scenario: Download theme from the internet

  Given that theme is not available locally

  When player chooses a particular theme

  Then ask user to pay the required amount
  and apply the theme in the game

### Scenario: Single player mode is selected

  Given that single player mode is selected

  When player enters his name and press start button

  Then the system assigns other player as computer
  and the game starts and calls a module to update screen

### Scenario: Double player mode is selected

  Given that double player mode is selected

  When player A and player B enter their names and press start button

  Then the game starts and calls a module to update screen
