#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: plot` module

- [Plot](#plot)   

---

### Plot
`:::js import "luxe: plot" for Plot`
> A service API to plot values for games + debugging.
> Can plot values from anywhere as a counter or as a running history.
> Counter plots add values to their total and add the total to the history at the end of the frame.

- [define](#Plot.define+2)(**id**: `String`, **type**: `PlotType`)
- [define](#Plot.define+3)(**id**: `String`, **type**: `PlotType`, **max_history**: `Num`)
- [update](#Plot.update+2)(**id**: `String`, **value**: `Num`)
- [list](#Plot.list)()
- [history](#Plot.history)(**id**: `String`)
- [latest](#Plot.latest)(**id**: `String`)
- [average](#Plot.average)(**id**: `String`)

<hr/>
<endpoint module="luxe: plot" class="Plot" signature="define(id : String, type : PlotType)"></endpoint>
<signature id="Plot.define+2">Plot.define(**id**: `String`, **type**: `PlotType`)
<a class="headerlink" href="#Plot.define+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Define a new plot by id, with the given `type`. The max history defaults to 60 values if not specified.   

<endpoint module="luxe: plot" class="Plot" signature="define(id : String, type : PlotType, max_history : Num)"></endpoint>
<signature id="Plot.define+3">Plot.define(**id**: `String`, **type**: `PlotType`, **max_history**: `Num`)
<a class="headerlink" href="#Plot.define+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Define a new plot by id, with the given `type` and `max_history`   

<endpoint module="luxe: plot" class="Plot" signature="update(id : String, value : Num)"></endpoint>
<signature id="Plot.update+2">Plot.update(**id**: `String`, **value**: `Num`)
<a class="headerlink" href="#Plot.update+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Update a given plot by id, with the given `value`. 
> For `PlotType.normal` this will add the value to the history.
> For `PlotType.counter` this will add the value to the total so far this frame.   

<endpoint module="luxe: plot" class="Plot" signature="list()"></endpoint>
<signature id="Plot.list">Plot.list()
<a class="headerlink" href="#Plot.list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Get a list of plots defined, as string id (e.g Strings.get(id) is needed)   

<endpoint module="luxe: plot" class="Plot" signature="history(id : String)"></endpoint>
<signature id="Plot.history">Plot.history(**id**: `String`)
<a class="headerlink" href="#Plot.history" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get the history for a given plot, as a list of values   

<endpoint module="luxe: plot" class="Plot" signature="latest(id : String)"></endpoint>
<signature id="Plot.latest">Plot.latest(**id**: `String`)
<a class="headerlink" href="#Plot.latest" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the latest value for a given plot   

<endpoint module="luxe: plot" class="Plot" signature="average(id : String)"></endpoint>
<signature id="Plot.average">Plot.average(**id**: `String`)
<a class="headerlink" href="#Plot.average" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the average value for a given plot, averaging out the history   

