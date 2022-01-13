# how to...

This page includes various things to learn about luxe, or refer to for quick reference.

---

## Generate random numbers

For API documentation and example usage, view the [Wren random](http://wren.io/modules/random/random.html) docs.

```js
import "random" for Random

construct ready() {

  var rng = Random.new()

    //float values between 0 and 1

  rng.float() // 0.53178795980617
  rng.float() // 0.20180515043262
  rng.float() // 0.43371948658705

    //float with a range 
  rng.float(-10, 10) //-5.9638969913476

    //int values
  rng.int(-10, 10) // -6

    //pull a random value from a list
  var list = [0,1,2,3,4,5]
  var item = rng.sample(list)
  var items = rng.sample(list, 3)

    //randomize list
  rng.shuffle(list) //list is modified in place

}

```

---

## Using multiple wren files 

In your project, you can make more files to separate your code.
Project scripts are imported as an absolute id, relative to the project root.

If you create a file called `player.wren` inside the root of your project, 
you can import it with `import "player" for Player` at the top of `game.wren`.

!!! note ""
    Note there is no extension, no _luxe module_ syntax (`luxe: string`) and no preceding dot-slash like `./player`.

If you created that file inside of a folder, like `player/logic/backpack.wren`, you would use `import "player/logic/backpack" for Backpack`. 

You always use that import id, even if you were inside a script in the `player/logic/` folder. 

---

## Reference a module 

Alongside your `project.luxe` file, there is a file called `project.modules.lx`. Dependencies on modules can be added to this file, or added via the [launcher](launcher). For example, if you were using a module called `arcade` at version `0.0.12` it would look like this:

```js
  modules = {
    luxe = "2022.0.1"
    arcade = "0.0.16"
  } //modules
```

---
