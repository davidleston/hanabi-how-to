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
    </tiles>
    <tiles>
      <tile title="blue 1"></tile>
      <tile title="blue 2"></tile>
      <tile title="blue 3"></tile>
    </tiles>
    <tiles>
      <tile title="red 1"></tile>
    </tiles>
    <tiles>
      <tile title="white 1"></tile>
    </tiles>
    <tiles>
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
    </tiles>
    <tiles>
      <tile title="blue 3"></tile>
    </tiles>
    <tiles>
      <tile title="red 1"></tile>
      <tile title="red 4"></tile>
    </tiles>
    <tiles>
      <tile title="white 1"></tile>
    </tiles>
    <tiles>
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

### Placement of tiles and terminology

#### Chop
The leftmost position in a hand, the position of the next tile to be discarded, is called the chop - as in the chopping block.

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="blue 1"></tile>
      <tile title="red 1"></tile>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <mark><tile title="red 4"></tile></mark>
    </tiles>
  </hand>
  
  <hand>
    <header>Your hand</header>
    <tiles>
      <mark><tile title="hidden"></tile></mark>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
    </tiles>
  </hand>
</game>

#### Play position / Play side
The rightmost position in a hand is called the play position or the play side of the hand.

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <mark><tile title="blue 1"></tile></mark>
      <tile title="red 1"></tile>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <tile title="red 4"></tile>
    </tiles>
  </hand>
  
  <hand>
    <header>Your hand</header>
    <tiles>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <mark><tile title="hidden"></tile></mark>
    </tiles>
  </hand>
</game>

When you intend to play a tile move it to the play position. When you clue your teammate ``twos``:

<game>
  <hand>
    <header>Your view of teammate's hand</header>
    <tiles>
      <tile title="blue 1"></tile>
      <tile title="red 1"></tile>
      <mark><tile title="yellow 2"></tile></mark>
      <mark><tile title="green 2"></tile></mark>
      <tile title="red 4"></tile>
    </tiles>
  </hand>

  <hand>
    <header>Teammate's perspective</header>
    <tiles>
      <tile title="hidden"></tile>
      <mark><tile title="hidden"></tile></mark>
      <mark><tile title="hidden"></tile></mark>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
    </tiles>
  </hand>
</game>

Your teammate will move those twos to the play position:

<game>
  <hand>
    <header>Your view of teammate's hand</header>
    <tiles>
      <mark><tile title="tapped yellow 2"></tile></mark>
      <mark><tile title="tapped green 2"></tile></mark>
      <tile title="blue 1"></tile>
      <tile title="red 1"></tile>
      <tile title="red 4"></tile>
    </tiles>
  </hand>

  <hand>
    <header>Teammate's perspective</header>
    <tiles>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <mark><tile title="tapped hidden"></tile></mark>
      <mark><tile title="tapped hidden"></tile></mark>
    </tiles>
  </hand>
</game>

When a tile is drawn it is place it immediately to the left of all the tiles intended for play. In this example after the yellow 2 is played the new tile is drawn onto the left of the green 2:

<game>
  <hand>
    <header>Your view of teammate's hand</header>
    <tiles>
      <tile title="tapped green 2"></tile>
      <mark><tile title="rainbow 3"></tile></mark>
      <tile title="blue 1"></tile>
      <tile title="red 1"></tile>
      <tile title="red 4"></tile>
    </tiles>
  </hand>

  <hand>
    <header>Teammate's perspective</header>
    <tiles>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <mark><tile title="hidden"></tile></mark>
      <tile title="tapped hidden"></tile>
    </tiles>
  </hand>
</game>

#### Safe / Unsafe
Safe and unsafe refers to the ability to discard a tile without losing points. Fives are always unsafe. A tile is safe if it is a duplicate of a tile that’s already been played or not a duplicate of a tile that’s been discarded. Discarded tiles are kept in two piles.
 
 <game>
   <pile>
     <header>Played tiles</header>
     <tiles>
       <tile title="yellow 1"></tile>
     </tiles>
     <tiles>
       <tile title="blue 1"></tile>
     </tiles>
     <tiles>
       <tile title="red 1"></tile>
       <tile title="red 2"></tile>
     </tiles>
   </pile>
 
   <pile>
     <header>✓ Safe discards</header>
     <tiles>
       <tile title="yellow 1"></tile>
     </tiles>
     <tiles>
       <tile title="red 2"></tile>
     </tiles>
   </pile>

   <pile>
     <header>⚠ Unsafe discards</header>
     <tiles>
       <tile title="yellow 4"></tile>
     </tiles>
     <tiles>
       <tile title="red 3"></tile>
       <tile title="red 4"></tile>
     </tiles>
   </pile>
 </game>

 
 The unsafe pile is a collection of tiles whose duplicates are unsafe to discard. As tiles are played their duplicates are moved from the unsafe discard to the safe discard.

#### Tap

When a tile is part of a clue it is rotated so it stands up. These tiles are said to be tapped.

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="blue 1"></tile>
      <tile title="red 1"></tile>
      <tile title="tapped yellow 2"></tile>
      <tile title="tapped green 2"></tile>
      <tile title="red 4"></tile>
    </tiles>
  </hand>
  
  <hand>
    <header>Your hand</header>
    <tiles>
      <tile title="hidden"></tile>
      <tile title="tapped hidden"></tile>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
    </tiles>
  </hand>
</game>

#### Saved tiles

Tiles that you intend to not discard are said to be saved. These tiles are no longer in the line of succession to be chopped. Place these tiles in a back row between you and the tiles that are in line of succession.

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <mark><tile title="tapped blue 5"></tile></mark>
    </tiles>
    <tiles>
      <tile title="red 1"></tile>
      <tile title="yellow 2"></tile>
      <tile title="green 2"></tile>
      <tile title="red 4"></tile>
    </tiles>
  </hand>
  
  <hand>
    <header>Your hand</header>
    <tiles>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
      <tile title="hidden"></tile>
    </tiles>
    <tiles>
      <mark><tile title="tapped hidden"></tile></mark>
      <mark><tile title="tapped hidden"></tile></mark>
    </tiles>
  </hand>
</game>

#### Right / Left

When referring to another player's tiles right and left is used from the perspective of that other player. When another play draws a tile they put it on the the right side of their hand from their perspective.
    
#### Information vs Clue

A clue is telling someone a color or number. Clueing is one way to provide information. Other ways to communicate information is discussed later.
