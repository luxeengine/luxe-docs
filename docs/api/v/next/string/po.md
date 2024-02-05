#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.2.1`)  


---

## `luxe: string/po` module

- [PO](#po)   
- [POData](#podata)   
- [POElement](#poelement)   
- [POHeader](#poheader)   
- [POString](#postring)   

---

### PO
`:::js import "luxe: string/po" for PO`
> no docs found

- [parse_header](#PO.parse_header)(**lines**: `List`)
- [parse_elements](#PO.parse_elements)(**lines**: `List`)
- [parse](#PO.parse+2)(**asset_id**: `String`, **bytes**: `String`)

<hr/>
<endpoint module="luxe: string/po" class="PO" signature="parse_header(lines : List)"></endpoint>
<signature id="PO.parse_header">PO.parse_header(**lines**: `List`)
<a class="headerlink" href="#PO.parse_header" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Result`
> no docs found   

<endpoint module="luxe: string/po" class="PO" signature="parse_elements(lines : List)"></endpoint>
<signature id="PO.parse_elements">PO.parse_elements(**lines**: `List`)
<a class="headerlink" href="#PO.parse_elements" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> converts the lines into chunks separated by lines   

<endpoint module="luxe: string/po" class="PO" signature="parse(asset_id : String, bytes : String)"></endpoint>
<signature id="PO.parse+2">PO.parse(**asset_id**: `String`, **bytes**: `String`)
<a class="headerlink" href="#PO.parse+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Result`
> no docs found   

### POData
`:::js import "luxe: string/po" for POData`
> no docs found

- [language](#POData.language)
- [headers](#POData.headers)
- [elements](#POData.elements)
- [new](#POData.new+3)(**asset_id**: `String`, **language**: `String`, **headers**: `Map`)
- [to_string](#POData.to_string)()

<hr/>
<endpoint module="luxe: string/po" class="POData" signature="language"></endpoint>
<signature id="POData.language">POData.language
<a class="headerlink" href="#POData.language" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string/po" class="POData" signature="headers"></endpoint>
<signature id="POData.headers">POData.headers
<a class="headerlink" href="#POData.headers" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: string/po" class="POData" signature="elements"></endpoint>
<signature id="POData.elements">POData.elements
<a class="headerlink" href="#POData.elements" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: string/po" class="POData" signature="new(asset_id : String, language : String, headers : Map)"></endpoint>
<signature id="POData.new+3">POData.new(**asset_id**: `String`, **language**: `String`, **headers**: `Map`)
<a class="headerlink" href="#POData.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js POData`
> no docs found   

<endpoint module="luxe: string/po" class="POData" signature="to_string()"></endpoint>
<signature id="POData.to_string">POData.to_string()
<a class="headerlink" href="#POData.to_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### POElement
`:::js import "luxe: string/po" for POElement`
> An element inside the PO file

- [id](#POElement.id)
- [key](#POElement.key)
- [file_index](#POElement.file_index)
- [plural_id](#POElement.plural_id)
- [comments](#POElement.comments)
- [is_plural](#POElement.is_plural)
- [strings](#POElement.strings)
- [new](#POElement.new+6)(**file_index**: `Num`, **key**: `String`, **plural_id**: `String`, **id**: `String`, **strings**: `List`, **comments**: `List`)
- [update_id](#POElement.update_id)(**id**: `String`)
- [update_comments](#POElement.update_comments)(**comments**: `List`)

<hr/>
<endpoint module="luxe: string/po" class="POElement" signature="id"></endpoint>
<signature id="POElement.id">POElement.id
<a class="headerlink" href="#POElement.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string/po" class="POElement" signature="key"></endpoint>
<signature id="POElement.key">POElement.key
<a class="headerlink" href="#POElement.key" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string/po" class="POElement" signature="file_index"></endpoint>
<signature id="POElement.file_index">POElement.file_index
<a class="headerlink" href="#POElement.file_index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: string/po" class="POElement" signature="plural_id"></endpoint>
<signature id="POElement.plural_id">POElement.plural_id
<a class="headerlink" href="#POElement.plural_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string/po" class="POElement" signature="comments"></endpoint>
<signature id="POElement.comments">POElement.comments
<a class="headerlink" href="#POElement.comments" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string/po" class="POElement" signature="is_plural"></endpoint>
<signature id="POElement.is_plural">POElement.is_plural
<a class="headerlink" href="#POElement.is_plural" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: string/po" class="POElement" signature="strings"></endpoint>
<signature id="POElement.strings">POElement.strings
<a class="headerlink" href="#POElement.strings" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: string/po" class="POElement" signature="new(file_index : Num, key : String, plural_id : String, id : String, strings : List, comments : List)"></endpoint>
<signature id="POElement.new+6">POElement.new(**file_index**: `Num`, **key**: `String`, **plural_id**: `String`, **id**: `String`, **strings**: `List`, **comments**: `List`)
<a class="headerlink" href="#POElement.new+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js POElement`
> no docs found   

<endpoint module="luxe: string/po" class="POElement" signature="update_id(id : String)"></endpoint>
<signature id="POElement.update_id">POElement.update_id(**id**: `String`)
<a class="headerlink" href="#POElement.update_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: string/po" class="POElement" signature="update_comments(comments : List)"></endpoint>
<signature id="POElement.update_comments">POElement.update_comments(**comments**: `List`)
<a class="headerlink" href="#POElement.update_comments" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### POHeader
`:::js import "luxe: string/po" for POHeader`
> a single header line

- [key](#POHeader.key)
- [value](#POHeader.value)
- [file_index](#POHeader.file_index)
- [new](#POHeader.new+3)(**file_index**: `Num`, **key**: `String`, **value**: `String`)
- [update_value](#POHeader.update_value)(**value**: `String`)

<hr/>
<endpoint module="luxe: string/po" class="POHeader" signature="key"></endpoint>
<signature id="POHeader.key">POHeader.key
<a class="headerlink" href="#POHeader.key" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string/po" class="POHeader" signature="value"></endpoint>
<signature id="POHeader.value">POHeader.value
<a class="headerlink" href="#POHeader.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string/po" class="POHeader" signature="file_index"></endpoint>
<signature id="POHeader.file_index">POHeader.file_index
<a class="headerlink" href="#POHeader.file_index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: string/po" class="POHeader" signature="new(file_index : Num, key : String, value : String)"></endpoint>
<signature id="POHeader.new+3">POHeader.new(**file_index**: `Num`, **key**: `String`, **value**: `String`)
<a class="headerlink" href="#POHeader.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js POHeader`
> no docs found   

<endpoint module="luxe: string/po" class="POHeader" signature="update_value(value : String)"></endpoint>
<signature id="POHeader.update_value">POHeader.update_value(**value**: `String`)
<a class="headerlink" href="#POHeader.update_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### POString
`:::js import "luxe: string/po" for POString`
> a single msgstr, with an optional [index]

- [value](#POString.value)
- [index](#POString.index)
- [new](#POString.new+2)(**value**: `String`, **index**: `Num`)

<hr/>
<endpoint module="luxe: string/po" class="POString" signature="value"></endpoint>
<signature id="POString.value">POString.value
<a class="headerlink" href="#POString.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string/po" class="POString" signature="index"></endpoint>
<signature id="POString.index">POString.index
<a class="headerlink" href="#POString.index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: string/po" class="POString" signature="new(value : String, index : Num)"></endpoint>
<signature id="POString.new+2">POString.new(**value**: `String`, **index**: `Num`)
<a class="headerlink" href="#POString.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js POString`
> no docs found   

