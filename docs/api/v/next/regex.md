#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: regex` module

- [RegexInfo](#regexinfo)   
- [RegexMatch](#regexmatch)   
- [RegexSubMatch](#regexsubmatch)   

---

### RegexInfo
`:::js import "luxe: regex" for RegexInfo`
> A regular expression result, containing one or more matches

- [matched](#RegexInfo.matched)
- [match](#RegexInfo.match)
- [[index : Num]](#RegexInfo.[index : Num])

<hr/>
<endpoint module="luxe: regex" class="RegexInfo" signature="matched"></endpoint>
<signature id="RegexInfo.matched">RegexInfo.matched
<a class="headerlink" href="#RegexInfo.matched" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> True if there was any match   

<endpoint module="luxe: regex" class="RegexInfo" signature="match"></endpoint>
<signature id="RegexInfo.match">RegexInfo.match
<a class="headerlink" href="#RegexInfo.match" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Returns the match results, a List of `RegexMatch`. Only valid if `matched` is true   

<endpoint module="luxe: regex" class="RegexInfo" signature="[index : Num]"></endpoint>
<signature id="RegexInfo.[index : Num]">RegexInfo [index : Num]
<a class="headerlink" href="#RegexInfo.[index : Num]" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RegexMatch`
> Convenience to access a specific match by index   

### RegexMatch
`:::js import "luxe: regex" for RegexMatch`
> A single match in a regular expression result.

- [subcount](#RegexMatch.subcount)
- [string](#RegexMatch.string)
- [offset](#RegexMatch.offset)
- [count](#RegexMatch.count)
- [index](#RegexMatch.index)
- [[index : Num]](#RegexMatch.[index : Num])

<hr/>
<endpoint module="luxe: regex" class="RegexMatch" signature="subcount"></endpoint>
<signature id="RegexMatch.subcount">RegexMatch.subcount
<a class="headerlink" href="#RegexMatch.subcount" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Number of sub matches (groups), not including 0 which is the full match   

<endpoint module="luxe: regex" class="RegexMatch" signature="string"></endpoint>
<signature id="RegexMatch.string">RegexMatch.string
<a class="headerlink" href="#RegexMatch.string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> The matched string   

<endpoint module="luxe: regex" class="RegexMatch" signature="offset"></endpoint>
<signature id="RegexMatch.offset">RegexMatch.offset
<a class="headerlink" href="#RegexMatch.offset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The offset of the match in the original string   

<endpoint module="luxe: regex" class="RegexMatch" signature="count"></endpoint>
<signature id="RegexMatch.count">RegexMatch.count
<a class="headerlink" href="#RegexMatch.count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The length of the match string   

<endpoint module="luxe: regex" class="RegexMatch" signature="index"></endpoint>
<signature id="RegexMatch.index">RegexMatch.index
<a class="headerlink" href="#RegexMatch.index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Index of this match in the match results   

<endpoint module="luxe: regex" class="RegexMatch" signature="[index : Num]"></endpoint>
<signature id="RegexMatch.[index : Num]">RegexMatch [index : Num]
<a class="headerlink" href="#RegexMatch.[index : Num]" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RegexSubMatch`
> Access to a specific group/sub match by index. 0 is the full match, groups are 1-indexed   

### RegexSubMatch
`:::js import "luxe: regex" for RegexSubMatch`
> A single group/sub match in a regular expression match.

- [count](#RegexSubMatch.count)
- [offset](#RegexSubMatch.offset)
- [string](#RegexSubMatch.string)
- [index](#RegexSubMatch.index)
- [[index : Num]](#RegexSubMatch.[index : Num])

<hr/>
<endpoint module="luxe: regex" class="RegexSubMatch" signature="count"></endpoint>
<signature id="RegexSubMatch.count">RegexSubMatch.count
<a class="headerlink" href="#RegexSubMatch.count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The length of the sub/group   

<endpoint module="luxe: regex" class="RegexSubMatch" signature="offset"></endpoint>
<signature id="RegexSubMatch.offset">RegexSubMatch.offset
<a class="headerlink" href="#RegexSubMatch.offset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The offset of the sub/group in the original match   

<endpoint module="luxe: regex" class="RegexSubMatch" signature="string"></endpoint>
<signature id="RegexSubMatch.string">RegexSubMatch.string
<a class="headerlink" href="#RegexSubMatch.string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> The string of the sub/group   

<endpoint module="luxe: regex" class="RegexSubMatch" signature="index"></endpoint>
<signature id="RegexSubMatch.index">RegexSubMatch.index
<a class="headerlink" href="#RegexSubMatch.index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The index of this sub/group in the match   

<endpoint module="luxe: regex" class="RegexSubMatch" signature="[index : Num]"></endpoint>
<signature id="RegexSubMatch.[index : Num]">RegexSubMatch [index : Num]
<a class="headerlink" href="#RegexSubMatch.[index : Num]" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> Returns info about this sub match by index. 0 returns `count`, 1 returns `offset`, 2 returns `string`   

