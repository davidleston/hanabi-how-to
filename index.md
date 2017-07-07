---
layout: default
---

How to be great at Hanabi
=========================

## Introduction

Advanced players can achieve a perfect score in most games. If you do not yet know how to play Hanabi I suggest first watching one of the many [videos explaining the rules of the game](https://www.youtube.com/results?search_query=how+to+play+hanabi).

Becoming an advanced player involves having retrospectives between games. Retrospectives are discussions with your teammates about how the team could have done better. Photos taken during the game can help with the question "What would you have done in this situation".

During these retrospectives a collection of conventions of play develop. Conventions are agreements with your teammates about what actions mean in specific situations.

Conventions have names, advantages, disadvantages, and exceptions. I’ll demonstrate each convention from the perspective of providing information and from the perspective of receiving information.

## Basic Conventions

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

### House Rules
Hanabi is the game that you make it. Here are some rules I play by that may be different from how others play. I consider these to be rules rather than conventions.
- You may only rearrange tiles when it is your turn or as the result of receiving a clue.
- Arrangement and tapping of tiles are purely confirmation of conventions. Tiles must not be arranged or tapped in such a way that information is conveyed that wouldn’t already be understood without rearrangement or tapping.
- Clues must identify at least one tile.

### General tips
- Prioritize getting more tiles played sooner
- Don’t worry about how many clues are left
- Don’t be afraid to discard
- Try to convey as much information in each turn

## Chaining / clueing multiple tiles

When multiple tiles are clued the tiles are played from right to left. The collection tiles queued up for play is called the chain.

### Turning off chains

Whenever a clue includes the head of a chain the entire chain is saved (no longer queued for play, no longer in the line of succession).

### Playing through a chain being turned off

If such a clue is a color clue and the only tile in the chain clued is the head and there are other tiles not in the chain included in the clue, then the other tiles are queued up. This is called playing through the clue. Otherwise any tiles included in a clue to the head of the chain are also saved. The distinction between number and color clues only applies to clues that include the head of a chain or the chop (discussed later).

### Reordering a chain

A clue that contains one or more tiles in a chain (but not the head of the chain) moves those tiles to the head of the chain. The tiles that are moved to the head of the chain maintain their order. Any tiles included in the clue that were not in the chain are saved.

### Alternative to chaining

A team may decide to play a game with chaining off. The decision to play with chaining on or off is made before the game begins. When chaining is off the rightmost tile in a multi-tile clue is queued for play and the other tiles are saved.

## Saving / playing the chop
A number clue that includes the chop means to save all the tiles in the clue. A color clue means means the same thing as if the chop was not involved. This distinction between number and color clues only applies to clues that include the head of a chain or the chop.

### Saving multiple tiles with one clue
An early save is saving a tile before it is on the chop. A tile can be saved early by cluing a number that is both not currently playable and not clearly safe to discard. A common early save is to clue a five when there are no playable fives. Saving a tile early also saves the chop.

### Providing safe discard saves the chop
    
Another way to save the chop is to clue one or more tiles such that it’s clearly discardable. This is prioritize the discarding of these tiles and save the chop. This can be done by cluing number or color.

### Max clues to prevent discard

The rules disallow discarding when all eight clues are available. If the next player has an unsafe discard and all eight clues are available on your turn and you have a play then go ahead and play to maintain max clues on the next player’s turn. If seven clues are available and you’re about to play a five then play the five to max the clues. If seven clues are available and you can discard then discard. The exception to this last one is if your chop might be future playable and you can see that the next player’s penultimate discard is not future playable then go ahead and clue the save. They’ll discard the already played tile and you’ll have saved a potential future playable from being discarded from your chop. The reason for delaying cluing the save is because delaying might prevent the need to save.
    
There may be situations in which multiple tiles need to be saved and none of the above are options. In a games with more than two players everyone is responsible for keeping an eye out for this situation. Multiple players may need to clue a player before their next turn. This means you’re looking at more than just the next player’s chop. If a you receive a save clue from two players before you in turn order and the interim player doesn’t have a play queued nor has a useful clue to give then assume the interim player is going to give you another save clue and save one more tile in from the chop than you normally would.
    
Clueing to play a tile that results in a bomb means save two from the from the chop. You can clue to play a tile that the player already knows to be unplayable and they will save two on the chop without actually playing. (Doesn't work if it's a forced clue)
    
Discarding / playing a tile that isn't expected tells the other player to save that many tiles. This is very unsafe and should only be used when absolutely necessary such as needing to save more than two tiles or needing to save tiles without clues. If the situation allows play instead of discarding because you might get lucky and actually get a valid play.

## Finesse and bluff (3 or more players)

- only bluff one up
- Forces intermediate player to play
- Cannot bluff on a forced rainbow, a forced rainbow is always a finesse.
- Reverse finesse and reverse bluff requires convention that clueing additional tiles appends to the chain either always or when it’s a possible reverse finesse/bluff.
