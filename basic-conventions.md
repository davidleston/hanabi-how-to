---
title: Basic conventions
order: 2
---

### Timeliness

With timeliness a clue is provided only at the time it is actionable, clues are not given for future reference.

If it's the first turn of the game and you see your teammate has the following tiles:

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <tile title="red 4"></tile>
      <mark><tile title="blue 1"></tile></mark>
      <tile title="white 3"></tile>
    </tiles>
  </hand>
</game>

You can provide the clue ``blue`` and your teammate will assume it is playable and will likely play it on their next turn.

Similarly, when you are told a tile is a two, you can assume it is a playable two and you would likely want to play it on your next turn.

<game>
  <hand>
    <header>Your hand</header>
    <tiles>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <mark><tile title="hidden"></tile></mark>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
    </tiles>
  </hand>
</game>

### Succession

With succession tiles are discarded off the left and new tiles are drawn onto the right. Players discard tiles that have been in their hand the longest. This allows clues to clearly be instructions to play while a tile that has not received any clues is implicitly okay safe to discard.

When our teammate plays their blue tile:

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <tile title="red 4"></tile>
      <mark><tile title="blue 1"></tile></mark>
      <tile title="white 3"></tile>
    </tiles>
  </hand>
</game>

A new tile will be drawn and placed on the right side (from their perspective) of their hand:

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="rainbow 1"></tile>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <tile title="red 4"></tile>
      <tile title="white 3"></tile>
    </tiles>
  </hand>
</game>

On their next turn they discard their chop (the white three) and draw a new tile:

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="rainbow 4"></tile>
      <tile title="rainbow 1"></tile>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <tile title="red 4"></tile>
    </tiles>
  </hand>
</game>

### Clues are to play

If a clue identifies a tile as unambiguously safe to discard then the intention for that tile to be discarded before other tiles.

When our temmate has the following when all the ones have been played:

<game>
  <pile>
    <header>Played tiles</header>
    <tiles>
      <tile title="yellow 1"></tile>
      <tile title="yellow 2"></tile>
      <tile title="yellow 3"></tile>
      <tile title="yellow 4"></tile>
    </tiles><tiles>
      <tile title="blue 1"></tile>
      <tile title="blue 2"></tile>
      <tile title="blue 3"></tile>
    </tiles><tiles>
      <tile title="red 1"></tile>
    </tiles><tiles>
      <tile title="white 1"></tile>
    </tiles><tiles>
      <tile title="rainbow 1"></tile>
    </tiles>
  </pile>
  
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="rainbow 4"></tile>
      <tile title="rainbow 1"></tile>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <tile title="red 4"></tile>
    </tiles>
  </hand>
</game>

We can provide the clue ``one`` and our teammate will discard the one before discarding any other tiles.

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="rainbow 4"></tile>
      <tile title="rainbow 1"></tile>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <tile title="red 4"></tile>
    </tiles>
  </hand>
</game>

If a tile that is about to be discarded is clued then the clue is to not discard that tile.

<game>
  <pile>
    <header>Discards</header>
    <tiles>
      <tile title="yellow 4"></tile>
    </tiles><tiles>
      <tile title="blue 3"></tile>
    </tiles><tiles>
      <tile title="red 1"></tile>
      <tile title="red 4"></tile>
    </tiles><tiles>
      <tile title="white 1"></tile>
    </tiles><tiles>
      <tile title="rainbow 1"></tile>
    </tiles>
  </pile>

  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="blue 1"></tile>
      <tile title="red 1"></tile>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <tile title="red 4"></tile>
    </tiles>
  </hand>
</game>

We can see the red 4 needs to be saved from being discard as the ony other red 4 has already been discarded. By providing the clue ``four`` we can save this tile from being discarded.

In other situations a clue is an instructions to play a tile.
