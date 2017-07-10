---
title: Terminology and tile placement
order: 3
---

### Chop

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

### Play position / Play side

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

When you intend to play a tile move it to the play position. When you clue your teammate "twos":

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

### Safe / Unsafe

Safe and unsafe refers to the ability to discard a tile without losing points. Fives are always unsafe. A tile is safe if it is a duplicate of a tile that’s already been played or not a duplicate of a tile that’s been discarded. Discarded tiles are kept in two piles.
 
 <game>
   <pile>
     <header>Played tiles</header>
     <tiles>
       <tile title="yellow 1"></tile>
     </tiles><tiles>
       <tile title="blue 1"></tile>
     </tiles><tiles>
       <tile title="red 1"></tile>
       <tile title="red 2"></tile>
     </tiles>
   </pile>
 
   <pile>
     <header>✓ Safe discards</header>
     <tiles>
       <tile title="yellow 1"></tile>
     </tiles><tiles>
       <tile title="red 2"></tile>
     </tiles>
   </pile>

   <pile>
     <header>⚠ Unsafe discards</header>
     <tiles>
       <tile title="yellow 4"></tile>
     </tiles><tiles>
       <tile title="red 3"></tile>
       <tile title="red 4"></tile>
     </tiles>
   </pile>
 </game>

 
 The unsafe pile is a collection of tiles whose duplicates are unsafe to discard. As tiles are played their duplicates are moved from the unsafe discard to the safe discard.

### Tap

When a tile is part of a clue it is rotated so it stands up. These tiles are said to be tapped.

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile title="blue 1"></tile>
      <tile title="red 1"></tile>
      <tile title="tapped yellow 2"></tile>
      <tile title="tapped rainbow 2"></tile>
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

### Saved tiles

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

### Right / Left

When referring to another player's tiles right and left is used from the perspective of that other player. When another play draws a tile they put it on the the right side of their hand from their perspective.
    
### Information vs Clue

A clue is telling someone a color or number. Clueing is one way to provide information. Other ways to communicate information is discussed later.
