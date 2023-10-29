#![](../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2022.0.5`)  


---

## `luxe: ui/block` module

- [UIBlock](#uiblock)   
- [UIBlockState](#uiblockstate)   

---

### UIBlock
`:::js import "luxe: ui/block" for UIBlock`
> no docs found

- [create](#UIBlock.create)(**ui**: `Entity`)
- [set_block_instance](#UIBlock.set_block_instance+3)(**control**: `Control`, **block**: `Block`, **instance**: `BlockInstance`)
- [set_sizes](#UIBlock.set_sizes+4)(**control**: `Control`, **label_width**: `Num`, **label_size**: `Num`, **field_height**: `Num`)
- [refresh](#UIBlock.refresh)(**control**: `Control`)

<hr/>
<endpoint module="luxe: ui/block" class="UIBlock" signature="create(ui : Entity)"></endpoint>
<signature id="UIBlock.create">UIBlock.create(**ui**: `Entity`)
<a class="headerlink" href="#UIBlock.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="set_block_instance(control : Control, block : Block, instance : BlockInstance)"></endpoint>
<signature id="UIBlock.set_block_instance+3">UIBlock.set_block_instance(**control**: `Control`, **block**: `Block`, **instance**: `BlockInstance`)
<a class="headerlink" href="#UIBlock.set_block_instance+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="set_sizes(control : Control, label_width : Num, label_size : Num, field_height : Num)"></endpoint>
<signature id="UIBlock.set_sizes+4">UIBlock.set_sizes(**control**: `Control`, **label_width**: `Num`, **label_size**: `Num`, **field_height**: `Num`)
<a class="headerlink" href="#UIBlock.set_sizes+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="refresh(control : Control)"></endpoint>
<signature id="UIBlock.refresh">UIBlock.refresh(**control**: `Control`)
<a class="headerlink" href="#UIBlock.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIBlockState
`:::js import "luxe: ui/block" for UIBlockState`
> no docs found

- [new](#UIBlockState.new+2)(**ui**: `Entity`, **control**: `Control`)
- [field_h](#UIBlockState.field_h)
- [label_w](#UIBlockState.label_w)
- [set_sizes](#UIBlockState.set_sizes+3)(**label_width**: `Num`, **label_size**: `Num`, **field_height**: `Num`)
- [set_instance](#UIBlockState.set_instance+2)(**block**: `Block`, **instance**: `BlockInstance`)
- [refresh](#UIBlockState.refresh)()
- [make_vec](#UIBlockState.make_vec)(**default**: `List`)
- [make_num](#UIBlockState.make_num)(**default**: `Num`)
- [make_text](#UIBlockState.make_text)(**default**: `String`)
- [make_path](#UIBlockState.make_path+2)(**default**: `String`, **tag**: `Num`)
- [make_bool](#UIBlockState.make_bool)(**default**: `Bool`)
- [make_options](#UIBlockState.make_options+2)(**options**: `List`, **default**: `String`)
- [make_field](#UIBlockState.make_field+5)(**block**: `Block`, **instance**: `BlockInstance`, **name**: `String`, **type**: `BlockFieldType`, **value**: `Any`)
- [make_object](#UIBlockState.make_object)(**name**: `String`)
- [make_object](#UIBlockState.make_object+2)(**name**: `String`, **title_color**: `Color`)
- [make_label](#UIBlockState.make_label+2)(**name**: `String`, **width**: `Num`)
- [make_block](#UIBlockState.make_block+3)(**block**: `Block`, **instance**: `BlockInstance`, **into**: `Control`)
- [make_block](#UIBlockState.make_block+4)(**block**: `Block`, **instance**: `BlockInstance`, **into**: `Control`, **indent**: `Num`)
- [make_group](#UIBlockState.make_group)(**name**: `Any`)

<hr/>
<endpoint module="luxe: ui/block" class="UIBlockState" signature="new(ui : Entity, control : Control)"></endpoint>
<signature id="UIBlockState.new+2">UIBlockState.new(**ui**: `Entity`, **control**: `Control`)
<a class="headerlink" href="#UIBlockState.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIBlockState`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="field_h"></endpoint>
<signature id="UIBlockState.field_h">UIBlockState.field_h
<a class="headerlink" href="#UIBlockState.field_h" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="label_w"></endpoint>
<signature id="UIBlockState.label_w">UIBlockState.label_w
<a class="headerlink" href="#UIBlockState.label_w" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="set_sizes(label_width : Num, label_size : Num, field_height : Num)"></endpoint>
<signature id="UIBlockState.set_sizes+3">UIBlockState.set_sizes(**label_width**: `Num`, **label_size**: `Num`, **field_height**: `Num`)
<a class="headerlink" href="#UIBlockState.set_sizes+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="set_instance(block : Block, instance : BlockInstance)"></endpoint>
<signature id="UIBlockState.set_instance+2">UIBlockState.set_instance(**block**: `Block`, **instance**: `BlockInstance`)
<a class="headerlink" href="#UIBlockState.set_instance+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="refresh()"></endpoint>
<signature id="UIBlockState.refresh">UIBlockState.refresh()
<a class="headerlink" href="#UIBlockState.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_vec(default : List)"></endpoint>
<signature id="UIBlockState.make_vec">UIBlockState.make_vec(**default**: `List`)
<a class="headerlink" href="#UIBlockState.make_vec" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_num(default : Num)"></endpoint>
<signature id="UIBlockState.make_num">UIBlockState.make_num(**default**: `Num`)
<a class="headerlink" href="#UIBlockState.make_num" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_text(default : String)"></endpoint>
<signature id="UIBlockState.make_text">UIBlockState.make_text(**default**: `String`)
<a class="headerlink" href="#UIBlockState.make_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_path(default : String, tag : Num)"></endpoint>
<signature id="UIBlockState.make_path+2">UIBlockState.make_path(**default**: `String`, **tag**: `Num`)
<a class="headerlink" href="#UIBlockState.make_path+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_bool(default : Bool)"></endpoint>
<signature id="UIBlockState.make_bool">UIBlockState.make_bool(**default**: `Bool`)
<a class="headerlink" href="#UIBlockState.make_bool" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_options(options : List, default : String)"></endpoint>
<signature id="UIBlockState.make_options+2">UIBlockState.make_options(**options**: `List`, **default**: `String`)
<a class="headerlink" href="#UIBlockState.make_options+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_field(block : Block, instance : BlockInstance, name : String, type : BlockFieldType, value : Any)"></endpoint>
<signature id="UIBlockState.make_field+5">UIBlockState.make_field(**block**: `Block`, **instance**: `BlockInstance`, **name**: `String`, **type**: `BlockFieldType`, **value**: `Any`)
<a class="headerlink" href="#UIBlockState.make_field+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_object(name : String)"></endpoint>
<signature id="UIBlockState.make_object">UIBlockState.make_object(**name**: `String`)
<a class="headerlink" href="#UIBlockState.make_object" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_object(name : String, title_color : Color)"></endpoint>
<signature id="UIBlockState.make_object+2">UIBlockState.make_object(**name**: `String`, **title_color**: `Color`)
<a class="headerlink" href="#UIBlockState.make_object+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_label(name : String, width : Num)"></endpoint>
<signature id="UIBlockState.make_label+2">UIBlockState.make_label(**name**: `String`, **width**: `Num`)
<a class="headerlink" href="#UIBlockState.make_label+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_block(block : Block, instance : BlockInstance, into : Control)"></endpoint>
<signature id="UIBlockState.make_block+3">UIBlockState.make_block(**block**: `Block`, **instance**: `BlockInstance`, **into**: `Control`)
<a class="headerlink" href="#UIBlockState.make_block+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_block(block : Block, instance : BlockInstance, into : Control, indent : Num)"></endpoint>
<signature id="UIBlockState.make_block+4">UIBlockState.make_block(**block**: `Block`, **instance**: `BlockInstance`, **into**: `Control`, **indent**: `Num`)
<a class="headerlink" href="#UIBlockState.make_block+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_group(name : Any)"></endpoint>
<signature id="UIBlockState.make_group">UIBlockState.make_group(**name**: `Any`)
<a class="headerlink" href="#UIBlockState.make_group" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

