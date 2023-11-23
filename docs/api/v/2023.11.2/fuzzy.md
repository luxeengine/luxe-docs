#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.2`)  


---

## `luxe: fuzzy` module

- [Fuzzy](#fuzzy)   
- [FuzzyResult](#fuzzyresult)   
- [FuzzyScore](#fuzzyscore)   

---

### Fuzzy
`:::js import "luxe: fuzzy" for Fuzzy`
> no docs found

- [sorted](#Fuzzy.sorted+2)(**pattern**: `String`, **items**: `List`)
- [matches](#Fuzzy.matches+2)(**pattern**: `String`, **items**: `List`)
- [matches](#Fuzzy.matches+3)(**pattern**: `String`, **items**: `List`, **fn**: `Fn`)
- [match](#Fuzzy.match+2)(**pattern**: `String`, **str**: `String`)
- [match_at](#Fuzzy.match_at+4)(**pattern**: `List`, **str**: `List`, **pattern_idx**: `Any`, **str_idx**: `Any`)
- [match_simple](#Fuzzy.match_simple+2)(**pattern**: `String`, **str**: `String`)
- [is_camel_case](#Fuzzy.is_camel_case+2)(**c0**: `Num`, **c1**: `Num`)
- [match_recursive](#Fuzzy.match_recursive+10)(**pattern**: `List`, **str**: `List`, **pattern_idx**: `Num`, **str_idx**: `Num`, **srcMatches**: `List`, **matches**: `List`, **maxMatches**: `Num`, **nextMatch**: `Num`, **count**: `Num`, **limit**: `Num`)

<hr/>
<endpoint module="luxe: fuzzy" class="Fuzzy" signature="sorted(pattern : String, items : List)"></endpoint>
<signature id="Fuzzy.sorted+2">Fuzzy.sorted(**pattern**: `String`, **items**: `List`)
<a class="headerlink" href="#Fuzzy.sorted+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: fuzzy" class="Fuzzy" signature="matches(pattern : String, items : List)"></endpoint>
<signature id="Fuzzy.matches+2">Fuzzy.matches(**pattern**: `String`, **items**: `List`)
<a class="headerlink" href="#Fuzzy.matches+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: fuzzy" class="Fuzzy" signature="matches(pattern : String, items : List, fn : Fn)"></endpoint>
<signature id="Fuzzy.matches+3">Fuzzy.matches(**pattern**: `String`, **items**: `List`, **fn**: `Fn`)
<a class="headerlink" href="#Fuzzy.matches+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: fuzzy" class="Fuzzy" signature="match(pattern : String, str : String)"></endpoint>
<signature id="Fuzzy.match+2">Fuzzy.match(**pattern**: `String`, **str**: `String`)
<a class="headerlink" href="#Fuzzy.match+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Result`
> no docs found   

<endpoint module="luxe: fuzzy" class="Fuzzy" signature="match_at(pattern : List, str : List, pattern_idx : Any, str_idx : Any)"></endpoint>
<signature id="Fuzzy.match_at+4">Fuzzy.match_at(**pattern**: `List`, **str**: `List`, **pattern_idx**: `Any`, **str_idx**: `Any`)
<a class="headerlink" href="#Fuzzy.match_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> returns true if character at two positions is the same   

<endpoint module="luxe: fuzzy" class="Fuzzy" signature="match_simple(pattern : String, str : String)"></endpoint>
<signature id="Fuzzy.match_simple+2">Fuzzy.match_simple(**pattern**: `String`, **str**: `String`)
<a class="headerlink" href="#Fuzzy.match_simple+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> returns true if each character in pattern is found sequentially within str   

<endpoint module="luxe: fuzzy" class="Fuzzy" signature="is_camel_case(c0 : Num, c1 : Num)"></endpoint>
<signature id="Fuzzy.is_camel_case+2">Fuzzy.is_camel_case(**c0**: `Num`, **c1**: `Num`)
<a class="headerlink" href="#Fuzzy.is_camel_case+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: fuzzy" class="Fuzzy" signature="match_recursive(pattern : List, str : List, pattern_idx : Num, str_idx : Num, srcMatches : List, matches : List, maxMatches : Num, nextMatch : Num, count : Num, limit : Num)"></endpoint>
<signature id="Fuzzy.match_recursive+10">Fuzzy.match_recursive(**pattern**: `List`, **str**: `List`, **pattern_idx**: `Num`, **str_idx**: `Num`, **srcMatches**: `List`, **matches**: `List`, **maxMatches**: `Num`, **nextMatch**: `Num`, **count**: `Num`, **limit**: `Num`)
<a class="headerlink" href="#Fuzzy.match_recursive+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Result`
> no docs found   

### FuzzyResult
`:::js import "luxe: fuzzy" for FuzzyResult`
> no docs found

- [item](#FuzzyResult.item)
- [score](#FuzzyResult.score)
- [matches](#FuzzyResult.matches)
- [new](#FuzzyResult.new+3)(**item**: `String`, **score**: `Num`, **matches**: `List`)

<hr/>
<endpoint module="luxe: fuzzy" class="FuzzyResult" signature="item"></endpoint>
<signature id="FuzzyResult.item">FuzzyResult.item
<a class="headerlink" href="#FuzzyResult.item" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: fuzzy" class="FuzzyResult" signature="score"></endpoint>
<signature id="FuzzyResult.score">FuzzyResult.score
<a class="headerlink" href="#FuzzyResult.score" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: fuzzy" class="FuzzyResult" signature="matches"></endpoint>
<signature id="FuzzyResult.matches">FuzzyResult.matches
<a class="headerlink" href="#FuzzyResult.matches" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: fuzzy" class="FuzzyResult" signature="new(item : String, score : Num, matches : List)"></endpoint>
<signature id="FuzzyResult.new+3">FuzzyResult.new(**item**: `String`, **score**: `Num`, **matches**: `List`)
<a class="headerlink" href="#FuzzyResult.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js FuzzyResult`
> no docs found   

### FuzzyScore
`:::js import "luxe: fuzzy" for FuzzyScore`
> no docs found

- [sequential_bonus](#FuzzyScore.sequential_bonus)
- [separator_bonus](#FuzzyScore.separator_bonus)
- [camel_bonus](#FuzzyScore.camel_bonus)
- [first_letter_bonus](#FuzzyScore.first_letter_bonus)
- [leading_letter_penalty](#FuzzyScore.leading_letter_penalty)
- [max_leading_letter_penalty](#FuzzyScore.max_leading_letter_penalty)
- [unmatched_letter_penalty](#FuzzyScore.unmatched_letter_penalty)

<hr/>
<endpoint module="luxe: fuzzy" class="FuzzyScore" signature="sequential_bonus"></endpoint>
<signature id="FuzzyScore.sequential_bonus">FuzzyScore.sequential_bonus
<a class="headerlink" href="#FuzzyScore.sequential_bonus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: fuzzy" class="FuzzyScore" signature="separator_bonus"></endpoint>
<signature id="FuzzyScore.separator_bonus">FuzzyScore.separator_bonus
<a class="headerlink" href="#FuzzyScore.separator_bonus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: fuzzy" class="FuzzyScore" signature="camel_bonus"></endpoint>
<signature id="FuzzyScore.camel_bonus">FuzzyScore.camel_bonus
<a class="headerlink" href="#FuzzyScore.camel_bonus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: fuzzy" class="FuzzyScore" signature="first_letter_bonus"></endpoint>
<signature id="FuzzyScore.first_letter_bonus">FuzzyScore.first_letter_bonus
<a class="headerlink" href="#FuzzyScore.first_letter_bonus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: fuzzy" class="FuzzyScore" signature="leading_letter_penalty"></endpoint>
<signature id="FuzzyScore.leading_letter_penalty">FuzzyScore.leading_letter_penalty
<a class="headerlink" href="#FuzzyScore.leading_letter_penalty" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: fuzzy" class="FuzzyScore" signature="max_leading_letter_penalty"></endpoint>
<signature id="FuzzyScore.max_leading_letter_penalty">FuzzyScore.max_leading_letter_penalty
<a class="headerlink" href="#FuzzyScore.max_leading_letter_penalty" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: fuzzy" class="FuzzyScore" signature="unmatched_letter_penalty"></endpoint>
<signature id="FuzzyScore.unmatched_letter_penalty">FuzzyScore.unmatched_letter_penalty
<a class="headerlink" href="#FuzzyScore.unmatched_letter_penalty" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

