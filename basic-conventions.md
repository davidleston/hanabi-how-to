---
title: Basic conventions
order: 2
---

### Timeliness

With timeliness a clue is provided only at the time it is actionable, clues are not given for future reference.

If it's the first turn of the game and you see your teammate has the following tiles:

<hand>
  <header>Teammate's hand</header>
  <tiles>
    <tile color="yellow" rank="2"></tile>
    <tile color="green" rank="2"></tile>
    <tile color="red" rank="4"></tile>
    <tile color="blue" rank="1"><highlighted></highlighted></tile>
    <tile color="white" rank="3"></tile>
  </tiles>
</hand>

You can provide the clue "blue" and your teammate will assume it is playable and will likely play it on their next turn.

Similarly, when you are told a tile is a two, you can assume it is a playable two and you would likely want to play it on your next turn.

<hand>
  <header>Your hand</header>
  <tiles>
    <tile hidden></tile>
    <tile hidden></tile>
    <tile hidden><highlighted></highlighted></tile>
    <tile hidden></tile>
    <tile hidden></tile>
  </tiles>
</hand>

### Succession

With succession tiles are discarded off the left and new tiles are drawn onto the right. Players discard tiles that have been in their hand the longest. This allows clues to clearly be instructions to play while a tile that has not received any clues is implicitly okay safe to discard.

When our teammate plays their blue tile:

<hand>
  <header>Teammate's hand</header>
  <tiles>
    <tile color="yellow" rank="2"></tile>
    <tile color="green" rank="2"></tile>
    <tile color="red" rank="4"></tile>
    <tile color="blue" rank="1"><highlighted></highlighted></tile>
    <tile color="white" rank="3"></tile>
  </tiles>
</hand>

A new tile will be drawn and placed on the right side (from their perspective) of their hand:

<hand>
  <header>Teammate's hand</header>
  <tiles>
    <tile color="rainbow" rank="1"></tile>
    <tile color="yellow" rank="2"></tile>
    <tile color="green" rank="2"></tile>
    <tile color="red" rank="4"></tile>
    <tile color="white" rank="3"></tile>
  </tiles>
</hand>

On their next turn they discard their chop (the white three) and draw a new tile:

<hand>
  <header>Teammate's hand</header>
  <tiles>
    <tile color="rainbow" rank="4"></tile>
    <tile color="rainbow" rank="1"></tile>
    <tile color="yellow" rank="2"></tile>
    <tile color="green" rank="2"></tile>
    <tile color="red" rank="4"></tile>
  </tiles>
</hand>


### Clues are to play

If a clue identifies a tile as unambiguously safe to discard then the intention for that tile to be discarded before other tiles.

When our temmate has the following when all the ones have been played:

<game>
  <pile>
    <header>Played tiles</header>
    <tiles>
      <tile color="yellow" rank="1"></tile>
      <tile color="yellow" rank="2"></tile>
      <tile color="yellow" rank="3"></tile>
      <tile color="yellow" rank="4"></tile>
    </tiles>
    <tiles>
      <tile color="blue" rank="1"></tile>
      <tile color="blue" rank="2"></tile>
      <tile color="blue" rank="3"></tile>
    </tiles>
    <tiles>
      <tile color="red" rank="1"></tile>
    </tiles>
    <tiles>
      <tile color="white" rank="1"></tile>
    </tiles>
    <tiles>
      <tile color="rainbow" rank="1"></tile>
    </tiles>
  </pile>
  
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile color="rainbow" rank="4"></tile>
      <tile color="rainbow" rank="1"></tile>
      <tile color="yellow" rank="2"></tile>
      <tile color="green" rank="2"></tile>
      <tile color="red" rank="4"></tile>
    </tiles>
  </hand>
</game>

We can provide the clue "one" and our teammate will discard the one before discarding any other tiles.

<hand>
  <header>Teammate's hand</header>
  <tiles>
    <tile color="rainbow" rank="4"></tile>
    <tile color="rainbow" rank="1"></tile>
    <tile color="yellow" rank="2"></tile>
    <tile color="green" rank="2"></tile>
    <tile color="red" rank="4"></tile>
  </tiles>
</hand>


If a tile that is about to be discarded is clued then the clue is to not discard that tile.

<game>
  <pile>
    <header>Discards</header>
    <tiles>
      <tile color="yellow" rank="4"></tile>
    </tiles>
    <tiles>
      <tile color="blue" rank="3"></tile>
    </tiles>
    <tiles>
      <tile color="red" rank="1"></tile>
      <tile color="red" rank="4"></tile>
    </tiles>
    <tiles>
      <tile color="white" rank="1"></tile>
    </tiles>
    <tiles>
      <tile color="rainbow" rank="1"></tile>
    </tiles>
  </pile>

  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile color="blue" rank="1"></tile>
      <tile color="red" rank="1"></tile>
      <tile color="yellow" rank="2"></tile>
      <tile color="green" rank="2"></tile>
      <tile color="red" rank="4"></tile>
    </tiles>
  </hand>
</game>

We can see the red 4 needs to be saved from being discard as the ony other red 4 has already been discarded. By providing the clue "four" we can save this tile from being discarded.

In other situations a clue is an instructions to play a tile.

### Placement of tiles and terminology

#### Chop
The leftmost position in a hand, the position of the next tile to be discarded, is called the chop - as in the chopping block.

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile color="blue" rank="1"></tile>
      <tile color="red" rank="1"></tile>
      <tile color="yellow" rank="2"></tile>
      <tile color="green" rank="2"></tile>
      <tile color="red" rank="4"><highlighted></highlighted></tile>
    </tiles>
  </hand>
  
  <hand>
    <header>Your hand</header>
    <tiles>
      <tile hidden><highlighted></highlighted></tile>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden></tile>
    </tiles>
  </hand>
</game>

#### Play position / Play side
The rightmost position in a hand is called the play position or the play side of the hand.

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile color="blue" rank="1"><highlighted></highlighted></tile>
      <tile color="red" rank="1"></tile>
      <tile color="yellow" rank="2"></tile>
      <tile color="green" rank="2"></tile>
      <tile color="red" rank="4"></tile>
    </tiles>
  </hand>
  
  <hand>
    <header>Your hand</header>
    <tiles>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden><highlighted></highlighted></tile>
    </tiles>
  </hand>
</game>

When you intend to play a tile move it to the play position. When you clue your teammate "twos":

<game>
  <hand>
    <header>Your view of teammate's hand</header>
    <tiles>
      <tile color="blue" rank="1"></tile>
      <tile color="red" rank="1"></tile>
      <tile color="yellow" rank="2"><highlighted></highlighted></tile>
      <tile color="green" rank="2"><highlighted></highlighted></tile>
      <tile color="red" rank="4"></tile>
    </tiles>
  </hand>

  <hand>
    <header>Teammate's perspective</header>
    <tiles>
      <tile hidden></tile>
      <tile hidden><highlighted></highlighted></tile>
      <tile hidden><highlighted></highlighted></tile>
      <tile hidden></tile>
      <tile hidden></tile>
    </tiles>
  </hand>
</game>

Your teammate will move those twos to the play position:

<game>
  <hand>
    <header>Your view of teammate's hand</header>
    <tiles>
      <tile color="yellow" rank="2" tapped><highlighted></highlighted></tile>
      <tile color="green" rank="2" tapped><highlighted></highlighted></tile>
      <tile color="blue" rank="1"></tile>
      <tile color="red" rank="1"></tile>
      <tile color="red" rank="4"></tile>
    </tiles>
  </hand>

  <hand>
    <header>Teammate's perspective</header>
    <tiles>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden tapped><highlighted></highlighted></tile>
      <tile hidden tapped><highlighted></highlighted></tile>
    </tiles>
  </hand>
</game>

When a tile is drawn it is place it immediately to the left of all the tiles intended for play. In this example after the yellow 2 is played the new tile is drawn onto the left of the green 2:

<game>
  <hand>
    <header>Your view of teammate's hand</header>
    <tiles>
      <tile color="green" rank="2" tapped></tile>
      <tile color="rainbow" rank="3"><highlighted></highlighted></tile>
      <tile color="blue" rank="1"></tile>
      <tile color="red" rank="1"></tile>
      <tile color="red" rank="4"></tile>
    </tiles>
  </hand>

  <hand>
    <header>Teammate's perspective</header>
    <tiles>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden><highlighted></highlighted></tile>
      <tile hidden tapped></tile>
    </tiles>
  </hand>
</game>

#### Safe / Unsafe
Safe and unsafe refers to the ability to discard a tile without losing points. Fives are always unsafe. A tile is safe if it is a duplicate of a tile that’s already been played or not a duplicate of a tile that’s been discarded. Discarded tiles are kept in two piles.
 
 <game>
   <pile>
     <header>Played tiles</header>
     <tiles>
       <tile color="yellow" rank="1"></tile>
     </tiles>
     <tiles>
       <tile color="blue" rank="1"></tile>
     </tiles>
     <tiles>
       <tile color="red" rank="1"></tile>
       <tile color="red" rank="2"></tile>
     </tiles>
   </pile>
 
   <pile>
     <header>✓ Safe discards</header>
     <tiles>
       <tile color="yellow" rank="1"></tile>
     </tiles>
     <tiles>
       <tile color="red" rank="2"></tile>
     </tiles>
   </pile>

   <pile>
     <header>⚠ Unsafe discards</header>
     <tiles>
       <tile color="yellow" rank="4"></tile>
     </tiles>
     <tiles>
       <tile color="red" rank="3"></tile>
       <tile color="red" rank="4"></tile>
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
      <tile color="blue" rank="1"></tile>
      <tile color="red" rank="1"></tile>
      <tile color="yellow" rank="2" tapped></tile>
      <tile color="green" rank="2" tapped></tile>
      <tile color="red" rank="4"></tile>
    </tiles>
  </hand>
  
  <hand>
    <header>Your hand</header>
    <tiles>
      <tile hidden></tile>
      <tile hidden tapped></tile>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden></tile>
    </tiles>
  </hand>
</game>

#### Saved tiles

Tiles that you intend to not discard are said to be saved. These tiles are no longer in the line of succession to be chopped. Place these tiles in a back row between you and the tiles that are in line of succession.

<game>
  <hand>
    <header>Teammate's hand</header>
    <tiles>
      <tile color="blue" rank="5" tapped><highlighted></highlighted></tile>
    </tiles>
    <tiles>
      <tile color="red" rank="1"></tile>
      <tile color="yellow" rank="2"></tile>
      <tile color="green" rank="2"></tile>
      <tile color="red" rank="4"></tile>
    </tiles>
  </hand>
  
  <hand>
    <header>Your hand</header>
    <tiles>
      <tile hidden></tile>
      <tile hidden></tile>
      <tile hidden></tile>
    </tiles>
    <tiles>
      <tile hidden tapped><highlighted></highlighted></tile>
      <tile hidden tapped><highlighted></highlighted></tile>
    </tiles>
  </hand>
</game>

#### Right / Left

When referring to another player's tiles right and left is used from the perspective of that other player. When another play draws a tile they put it on the the right side of their hand from their perspective.
    
#### Information vs Clue

A clue is telling someone a color or number. Clueing is one way to provide information. Other ways to communicate information is discussed later.
