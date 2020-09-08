# Interaction Sequences

## Startup Sequence

    home->>+game-setup: Change game background/theme
    game-setup->>-home: If theme is available for free, change theme and return
    game-setup->>+ThirdPartyWebsite: If theme available online then take payment,
    download theme from this website
    ThirdPartyWebsite->>-game-setup: Reflect the change in the game
    game-setup->>+home: Change the theme and return
    home->>+game-setup: Single player mode choosen
    game-setup->>+game-setup: Player enters his name
    game-setup->>-home: Computer is assigned as the second player
    home->>update-ui: Game starts with pong ball moving in a random direction

## Movement Initiation

    update-ui->>+central-unit: returns back every 100 milliseconds
    central-unit->>+check-collision: calls every 100 milliseconds
    check-collision->>-central-unit: no collision detected
    central-unit->>+update-ui: move the pong ball in the decided direction
    and with decided speed
    update-ui->>-central-unit: returns after 100 milliseconds
    central-unit->>+check-collision: call to check collision
    check-collision->>-central-unit: collision with upper or lower wall
    central-unit->>+update-velocity-direction: updates the direction and velocity
    for the movement of pong ball
    update-velocity-direction->>-central-unit: returns updated velocity and direction
    central-unit->>+update-ui: move the pong ball in the decided direction and
    with decided speed
    update-ui->>-central-unit: returns after 100 milliseconds
    central-unit->>+check-collision: call to check collision
    check-collision->>-central-unit: collision with the paddle of players
    central-unit->>+update-velocity-direction: updates the direction and velocity
    for the movement of pong ball
    update-velocity-direction->>-central-unit: returns updated velocity and direction
    central-unit->>+update-ui: move the pong ball in the decided direction and with
    decided speed
    update-ui->>-central-unit: returns after 100 milliseconds

## One score

    central-unit->>+check-collision: collision detected with side walls
    check-collision->>-central-unit: returns data
    central-unit->>+capture-points: the score of winning player is increased by one
    capture-points->>+capture-points: either player A or player B reaches 10
    points first
    capture-points->>-central-unit: returns data
    central-unit->>+game-ends: ask for replay or quitting the game
    game-ends->>+home: if player chooses to quit  
    game-ends->>-central-unit: if player chooses to replay
