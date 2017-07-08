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

### Play position / Play side

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

### Safe / Unsafe

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

### Tap

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

### Saved tiles

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

### Right / Left

When referring to another player's tiles right and left is used from the perspective of that other player. When another play draws a tile they put it on the the right side of their hand from their perspective.
    
### Information vs Clue

A clue is telling someone a color or number. Clueing is one way to provide information. Other ways to communicate information is discussed later.
