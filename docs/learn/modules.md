![](../images/luxe-dark.svg){width="96em"}

## Reference a module 

Alongside your `project.luxe` file, there is a file called `luxe.project/modules.lx`. Dependencies on modules can be added to this file, or added via the launcher. [The tutorial covers this](../tutorials/world/index.md/#using-the-module-in-a-project). For example, if you were using a module called `arcade` at version `0.0.24` it would look like this:

```js
  modules = {
    luxe = "2025.6.5"
    arcade = "0.0.24"
  } //modules
```
