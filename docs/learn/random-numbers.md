![](../images/luxe-dark.svg){width="96em"}

# Generate random numbers

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
