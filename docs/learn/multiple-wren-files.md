![](../images/luxe-dark.svg){width="96em"}


# Using multiple wren files 

In your project, you can make more files to separate your code.
Project scripts are imported as an absolute id, relative to the project root.

If you create a file called `player.wren` inside the root of your project, 
you can import it with `import "player" for Player` at the top of `game.wren`.

!!! note ""
    Note there is no extension, no _luxe module_ syntax (`luxe: string`) and no preceding dot-slash like `./player`.

If you created that file inside of a folder, like `player/logic/backpack.wren`, you would use `import "player/logic/backpack" for Backpack`. 

You always use that import id, even if you were inside a script in the `player/logic/` folder. 
