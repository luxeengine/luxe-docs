#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2022.0.4`)  


---

## `luxe: assert` module

- [Assert](#assert)   

---

### Assert
`:::js import "luxe: assert" for Assert`
> Simple assertions.
> 
> An assertion is a statement in code that is a strict rule.
> They prevent code from behaving in unexpected ways, by asserting that the code is acting in the way you intended.
> This can catch a lot of bugs, because it can enforce correct usage of code.
> 
> For example, if your function does not allow null for an argument, that is something you can assert.
> Then the user of your code knows that they've used your API incorrectly and can correct the issue.
> 
> An assertion calls `Fiber.abort()`, ending execution (unless handled higher up).

- [is_true](#Assert.is_true)(**condition**: `Bool`)
- [is_true](#Assert.is_true+2)(**condition**: `Any`, **message**: `Any`)
- [is_false](#Assert.is_false)(**condition**: `Any`)
- [is_false](#Assert.is_false+2)(**condition**: `Any`, **message**: `Any`)
- [not_null](#Assert.not_null)(**value**: `Any`)
- [not_null](#Assert.not_null+2)(**value**: `Any`, **message**: `Any`)
- [is_null](#Assert.is_null)(**value**: `Any`)
- [is_null](#Assert.is_null+2)(**value**: `Any`, **message**: `Any`)

<hr/>
<endpoint module="luxe: assert" class="Assert" signature="is_true(condition : Bool)"></endpoint>
<signature id="Assert.is_true">Assert.is_true(**condition**: `Bool`)
<a class="headerlink" href="#Assert.is_true" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Assert that a particular condition is true.
> 
>   ```js
>   //In this code, we expect that the player
>   //should never be here if they are not flying.
>   Assert.is_true(player.flying)
>   ```   

<endpoint module="luxe: assert" class="Assert" signature="is_true(condition : Any, message : Any)"></endpoint>
<signature id="Assert.is_true+2">Assert.is_true(**condition**: `Any`, **message**: `Any`)
<a class="headerlink" href="#Assert.is_true+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Assert that a particular condition is true, and display a message on abort.
> 
>   ```js
>   //In this code, we expect that the player
>   //should never be here if they are not flying.
>   Assert.is_true(player.flying, "Expected player to be in a flying state")
>   ```   

<endpoint module="luxe: assert" class="Assert" signature="is_false(condition : Any)"></endpoint>
<signature id="Assert.is_false">Assert.is_false(**condition**: `Any`)
<a class="headerlink" href="#Assert.is_false" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Assert that a particular condition is false.
> 
>   ```js
>   Assert.is_false(player.flying)
>   ```   

<endpoint module="luxe: assert" class="Assert" signature="is_false(condition : Any, message : Any)"></endpoint>
<signature id="Assert.is_false+2">Assert.is_false(**condition**: `Any`, **message**: `Any`)
<a class="headerlink" href="#Assert.is_false+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Assert that a particular condition is false, and display a message on abort.
> 
>   ```js
>   Assert.is_false(player.flying, "Expected player NOT to be in a flying state")
>   ```   

<endpoint module="luxe: assert" class="Assert" signature="not_null(value : Any)"></endpoint>
<signature id="Assert.not_null">Assert.not_null(**value**: `Any`)
<a class="headerlink" href="#Assert.not_null" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Assert that a particular statement is not null.
> 
>   ```js
>   //We require a valid player in this code
>   Assert.not_null(player)
>   ```   

<endpoint module="luxe: assert" class="Assert" signature="not_null(value : Any, message : Any)"></endpoint>
<signature id="Assert.not_null+2">Assert.not_null(**value**: `Any`, **message**: `Any`)
<a class="headerlink" href="#Assert.not_null+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Assert that a particular statement is not null.
> 
>   ```js
>   Assert.not_null(player, "A valid player is required")
>   ```   

<endpoint module="luxe: assert" class="Assert" signature="is_null(value : Any)"></endpoint>
<signature id="Assert.is_null">Assert.is_null(**value**: `Any`)
<a class="headerlink" href="#Assert.is_null" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Assert that a particular statement is null.
> 
>   ```js
>   //We assume the player is not holding something.
>   Assert.is_null(player.item_in_hand)
>   ```   

<endpoint module="luxe: assert" class="Assert" signature="is_null(value : Any, message : Any)"></endpoint>
<signature id="Assert.is_null+2">Assert.is_null(**value**: `Any`, **message**: `Any`)
<a class="headerlink" href="#Assert.is_null+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Assert that a particular statement is null, and display a message on abort.
> 
>   ```js
>   Assert.is_null(player.item_in_hand, "Player must not have an item in hand when calling this")
>   ```   

