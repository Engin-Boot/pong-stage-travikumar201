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

-describe-how-modules-interact-to-make-the-ball-move

## One score

-describe-how-the-modules-interact-to-record-scores
