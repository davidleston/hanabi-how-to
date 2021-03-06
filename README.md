<script>
:root {
  font-family: sans-serif;
  --tileBackground: #222;
  --tileBorderRadius: 5px;
  --tileWidth: 3em;
  --tileHeight: 1.75em;
}

pile tiles {
  display: inline-flex;
  align-items: flex-end;
  flex-direction: column-reverse;
}

pile, hand {
  display: inline-block;
  background: #eee;
  padding: calc(var(--tileBorderRadius) * 2);
  border-radius: var(--tileBorderRadius);
  margin: 5px;
  box-shadow: inset 0px 0px 1px rgba(0,0,0,.5);
}

header {
  margin-bottom: var(--tileBorderRadius);
}

tiles {
  display: flex;
  align-items: flex-end;
}

tile {
  order: 1;
  padding: 5px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  flex: 1 1 1;
  flex-direction: row;
  width: var(--tileWidth);
  height: var(--tileHeight);
  box-shadow: inset 0 0 7px black;
  background: var(--tileBackground);
  border-radius: var(--tileBorderRadius);
}

hand tile {
  margin-top: calc(var(--tileWidth) - var(--tileHeight));  
}

tile[tapped] {
  flex-direction: column;
  width: var(--tileHeight);
  height: var(--tileWidth);
  margin-top: 0;
}

tile::before, tile::after {
  flex: 1;
  text-align: center;
}

tile::before {
  content: attr(rank);
  font-weight: bold;
  font-size: 110%;
}

[hidden]::before {
  content: '⛩️';
}

[color=yellow] {
  color: yellow;
}
[color=yellow]::after {
  content: '🌼';
}
[color=blue] {
  color: lightblue;
}

[color=blue]::after {
  content: '⚘';
  font-size: 160%;
}

[color=green] {
  color: lightgreen;
}

[color=green]::after {
  content: '☘'
}

[color=red] {
  color: deeppink;
}

[color=red]::after {
  content: '🌹';
}

[color=white] {
  color: ghostwhite;
}

[color=white]::after {
  content: '❀';
  font-size: 140%;
}

[color=rainbow] {
  color: ghostwhite;
}

[color=rainbow]::after {
  content: '🌈';
}

tile[unsafe] {
  --sparseness: 4px;
  background: repeating-linear-gradient(45deg, var(--tileBackground), var(--tileBackground) var(--sparseness), yellow var(--sparseness), yellow calc(var(--sparseness) + 1px));
}
</script>

# hanabi-how-to

<hand>
  <header>Player 1</header>
  <tiles>
    <tile color=yellow rank=1 tapped></tile>
    <tile color=yellow rank=2></tile>
    <tile color=yellow rank=3></tile>
    <tile color=yellow rank=4></tile>
    <tile color=yellow rank=5></tile>
  </tiles>
</hand>