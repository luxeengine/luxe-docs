#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.2.3`)  


---

## `luxe: semver` module

- [Comparator](#comparator)   
- [SemVer](#semver)   
- [SemVerRange](#semverrange)   
- [SemVerSubset](#semversubset)   
- [SemVerSubsetInterval](#semversubsetinterval)   

---

### Comparator
`:::js import "luxe: semver" for Comparator`
> no docs found

- [value](#Comparator.value)
- [semver](#Comparator.semver)
- [operator](#Comparator.operator)
- [loose](#Comparator.loose)
- [any](#Comparator.any)
- [new](#Comparator.new)(**comp**: `Any`)
- [new](#Comparator.new+2)(**comp**: `Any`, **loose**: `Any`)
- [create](#Comparator.create+2)(**comp**: `Any`, **loose**: `Any`)
- [inverted](#Comparator.inverted)()
- [test](#Comparator.test)(**version**: `Any`)
- [parse](#Comparator.parse)(**comp**: `Any`)
- [debug](#Comparator.debug)(**a**: `Any`)
- [intersects](#Comparator.intersects)(**comp**: `Any`)
- [intersects](#Comparator.intersects+2)(**comp**: `Any`, **loose**: `Any`)

<hr/>
<endpoint module="luxe: semver" class="Comparator" signature="value"></endpoint>
<signature id="Comparator.value">Comparator.value
<a class="headerlink" href="#Comparator.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="semver"></endpoint>
<signature id="Comparator.semver">Comparator.semver
<a class="headerlink" href="#Comparator.semver" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="operator"></endpoint>
<signature id="Comparator.operator">Comparator.operator
<a class="headerlink" href="#Comparator.operator" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="loose"></endpoint>
<signature id="Comparator.loose">Comparator.loose
<a class="headerlink" href="#Comparator.loose" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="any"></endpoint>
<signature id="Comparator.any">Comparator.any
<a class="headerlink" href="#Comparator.any" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="new(comp : Any)"></endpoint>
<signature id="Comparator.new">Comparator.new(**comp**: `Any`)
<a class="headerlink" href="#Comparator.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Comparator`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="new(comp : Any, loose : Any)"></endpoint>
<signature id="Comparator.new+2">Comparator.new(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#Comparator.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Comparator`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="create(comp : Any, loose : Any)"></endpoint>
<signature id="Comparator.create+2">Comparator.create(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#Comparator.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Comparator`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="inverted()"></endpoint>
<signature id="Comparator.inverted">Comparator.inverted()
<a class="headerlink" href="#Comparator.inverted" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="test(version : Any)"></endpoint>
<signature id="Comparator.test">Comparator.test(**version**: `Any`)
<a class="headerlink" href="#Comparator.test" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="parse(comp : Any)"></endpoint>
<signature id="Comparator.parse">Comparator.parse(**comp**: `Any`)
<a class="headerlink" href="#Comparator.parse" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="debug(a : Any)"></endpoint>
<signature id="Comparator.debug">Comparator.debug(**a**: `Any`)
<a class="headerlink" href="#Comparator.debug" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="intersects(comp : Any)"></endpoint>
<signature id="Comparator.intersects">Comparator.intersects(**comp**: `Any`)
<a class="headerlink" href="#Comparator.intersects" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="Comparator" signature="intersects(comp : Any, loose : Any)"></endpoint>
<signature id="Comparator.intersects+2">Comparator.intersects(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#Comparator.intersects+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SemVer
`:::js import "luxe: semver" for SemVer`
> no docs found

- [SPEC](#SemVer.SPEC)
- [loose](#SemVer.loose)
- [version](#SemVer.version)
- [major](#SemVer.major)
- [minor](#SemVer.minor)
- [patch](#SemVer.patch)
- [prerelease](#SemVer.prerelease)
- [raw](#SemVer.raw)
- [new](#SemVer.new)(**version**: `Any`)
- [new](#SemVer.new+2)(**version**: `Any`, **loose**: `Any`)
- [create](#SemVer.create+2)(**version**: `Any`, **loose**: `Any`)
- [format](#SemVer.format)()
- [!=](#SemVer.!=)(**other**: `Any`)
- [==](#SemVer.==)(**other**: `Any`)
- [<=](#SemVer.<=)(**other**: `Any`)
- [>=](#SemVer.>=)(**other**: `Any`)
- [>](#SemVer.>)(**other**: `Any`)
- [<](#SemVer.<)(**other**: `Any`)
- [inc](#SemVer.inc)(**release**: `Any`)
- [inc](#SemVer.inc+2)(**release**: `Any`, **identifier**: `Any`)
- [compare](#SemVer.compare)(**other**: `Any`)
- [inc](#SemVer.inc+2)(**version**: `Any`, **release**: `Any`)
- [inc](#SemVer.inc+3)(**version**: `Any`, **release**: `Any`, **identifier**: `Any`)
- [inc](#SemVer.inc+4)(**version**: `Any`, **release**: `Any`, **loose**: `Any`, **identifier**: `Any`)
- [parse](#SemVer.parse)(**version**: `Any`)
- [parse](#SemVer.parse+2)(**version**: `Any`, **loose**: `Any`)
- [valid](#SemVer.valid)(**version**: `Any`)
- [valid](#SemVer.valid+2)(**version**: `Any`, **loose**: `Any`)
- [clean](#SemVer.clean)(**version**: `Any`)
- [clean](#SemVer.clean+2)(**version**: `Any`, **loose**: `Any`)
- [diff](#SemVer.diff+2)(**version1**: `Any`, **version2**: `Any`)
- [major](#SemVer.major)(**a**: `Any`)
- [major](#SemVer.major+2)(**a**: `Any`, **loose**: `Any`)
- [minor](#SemVer.minor)(**a**: `Any`)
- [minor](#SemVer.minor+2)(**a**: `Any`, **loose**: `Any`)
- [patch](#SemVer.patch)(**a**: `Any`)
- [patch](#SemVer.patch+2)(**a**: `Any`, **loose**: `Any`)
- [prerelease](#SemVer.prerelease)(**a**: `Any`)
- [prerelease](#SemVer.prerelease+2)(**a**: `Any`, **loose**: `Any`)
- [compare](#SemVer.compare+2)(**a**: `Any`, **b**: `Any`)
- [compare](#SemVer.compare+3)(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
- [rcompare](#SemVer.rcompare+2)(**a**: `Any`, **b**: `Any`)
- [rcompare](#SemVer.rcompare+3)(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
- [sort](#SemVer.sort)(**list**: `Any`)
- [sort](#SemVer.sort+2)(**list**: `Any`, **loose**: `Any`)
- [rsort](#SemVer.rsort)(**list**: `Any`)
- [rsort](#SemVer.rsort+2)(**list**: `Any`, **loose**: `Any`)
- [gt](#SemVer.gt+2)(**a**: `Any`, **b**: `Any`)
- [gt](#SemVer.gt+3)(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
- [lt](#SemVer.lt+2)(**a**: `Any`, **b**: `Any`)
- [lt](#SemVer.lt+3)(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
- [gte](#SemVer.gte+2)(**a**: `Any`, **b**: `Any`)
- [gte](#SemVer.gte+3)(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
- [lte](#SemVer.lte+2)(**a**: `Any`, **b**: `Any`)
- [lte](#SemVer.lte+3)(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
- [eq](#SemVer.eq+2)(**a**: `Any`, **b**: `Any`)
- [eq](#SemVer.eq+3)(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
- [neq](#SemVer.neq+2)(**a**: `Any`, **b**: `Any`)
- [neq](#SemVer.neq+3)(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
- [cmp](#SemVer.cmp+3)(**a**: `Any`, **op**: `Any`, **b**: `Any`)
- [cmp](#SemVer.cmp+4)(**a**: `Any`, **op**: `Any`, **b**: `Any`, **loose**: `Any`)
- [max_satisfying](#SemVer.max_satisfying+2)(**versions**: `Any`, **range**: `Any`)
- [max_satisfying](#SemVer.max_satisfying+3)(**versions**: `Any`, **range**: `Any`, **loose**: `Any`)
- [min_satisfying](#SemVer.min_satisfying+2)(**versions**: `Any`, **range**: `Any`)
- [min_satisfying](#SemVer.min_satisfying+3)(**versions**: `Any`, **range**: `Any`, **loose**: `Any`)
- [satisfies](#SemVer.satisfies+2)(**version**: `Any`, **range**: `Any`)
- [satisfies](#SemVer.satisfies+3)(**version**: `Any`, **range**: `Any`, **loose**: `Any`)
- [valid_range](#SemVer.valid_range)(**range**: `Any`)
- [valid_range](#SemVer.valid_range+2)(**range**: `Any`, **loose**: `Any`)
- [ltr](#SemVer.ltr+2)(**version**: `Any`, **range**: `Any`)
- [ltr](#SemVer.ltr+3)(**version**: `Any`, **range**: `Any`, **loose**: `Any`)
- [gtr](#SemVer.gtr+2)(**version**: `Any`, **range**: `Any`)
- [gtr](#SemVer.gtr+3)(**version**: `Any`, **range**: `Any`, **loose**: `Any`)
- [outside](#SemVer.outside+3)(**version**: `Any`, **range**: `Any`, **hilo**: `Any`)
- [outside](#SemVer.outside+4)(**version**: `Any`, **range**: `Any`, **hilo**: `Any`, **loose**: `Any`)
- [debug](#SemVer.debug)(**a**: `Any`)
- [compare_main](#SemVer.compare_main)(**other**: `Any`)
- [first_not_zero](#SemVer.first_not_zero+2)(**a**: `Any`, **b**: `Any`)
- [first_not_zero](#SemVer.first_not_zero+3)(**a**: `Any`, **b**: `Any`, **c**: `Any`)
- [compare_pre](#SemVer.compare_pre)(**other**: `Any`)
- [compare_identifiers](#SemVer.compare_identifiers+2)(**a**: `Any`, **b**: `Any`)

<hr/>
<endpoint module="luxe: semver" class="SemVer" signature="SPEC"></endpoint>
<signature id="SemVer.SPEC">SemVer.SPEC
<a class="headerlink" href="#SemVer.SPEC" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="loose"></endpoint>
<signature id="SemVer.loose">SemVer.loose
<a class="headerlink" href="#SemVer.loose" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="version"></endpoint>
<signature id="SemVer.version">SemVer.version
<a class="headerlink" href="#SemVer.version" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="major"></endpoint>
<signature id="SemVer.major">SemVer.major
<a class="headerlink" href="#SemVer.major" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="minor"></endpoint>
<signature id="SemVer.minor">SemVer.minor
<a class="headerlink" href="#SemVer.minor" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="patch"></endpoint>
<signature id="SemVer.patch">SemVer.patch
<a class="headerlink" href="#SemVer.patch" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="prerelease"></endpoint>
<signature id="SemVer.prerelease">SemVer.prerelease
<a class="headerlink" href="#SemVer.prerelease" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="raw"></endpoint>
<signature id="SemVer.raw">SemVer.raw
<a class="headerlink" href="#SemVer.raw" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="new(version : Any)"></endpoint>
<signature id="SemVer.new">SemVer.new(**version**: `Any`)
<a class="headerlink" href="#SemVer.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SemVer`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="new(version : Any, loose : Any)"></endpoint>
<signature id="SemVer.new+2">SemVer.new(**version**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SemVer`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="create(version : Any, loose : Any)"></endpoint>
<signature id="SemVer.create+2">SemVer.create(**version**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SemVer`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="format()"></endpoint>
<signature id="SemVer.format">SemVer.format()
<a class="headerlink" href="#SemVer.format" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="!=(other : Any)"></endpoint>
<signature id="SemVer.!=">SemVer !=(**other**: `Any`)
<a class="headerlink" href="#SemVer.!=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="==(other : Any)"></endpoint>
<signature id="SemVer.==">SemVer ==(**other**: `Any`)
<a class="headerlink" href="#SemVer.==" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="<=(other : Any)"></endpoint>
<signature id="SemVer.<=">SemVer <=(**other**: `Any`)
<a class="headerlink" href="#SemVer.<=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature=">=(other : Any)"></endpoint>
<signature id="SemVer.>=">SemVer >=(**other**: `Any`)
<a class="headerlink" href="#SemVer.>=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature=">(other : Any)"></endpoint>
<signature id="SemVer.>">SemVer >(**other**: `Any`)
<a class="headerlink" href="#SemVer.>" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="<(other : Any)"></endpoint>
<signature id="SemVer.<">SemVer <(**other**: `Any`)
<a class="headerlink" href="#SemVer.<" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="inc(release : Any)"></endpoint>
<signature id="SemVer.inc">SemVer.inc(**release**: `Any`)
<a class="headerlink" href="#SemVer.inc" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="inc(release : Any, identifier : Any)"></endpoint>
<signature id="SemVer.inc+2">SemVer.inc(**release**: `Any`, **identifier**: `Any`)
<a class="headerlink" href="#SemVer.inc+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="compare(other : Any)"></endpoint>
<signature id="SemVer.compare">SemVer.compare(**other**: `Any`)
<a class="headerlink" href="#SemVer.compare" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="inc(version : Any, release : Any)"></endpoint>
<signature id="SemVer.inc+2">SemVer.inc(**version**: `Any`, **release**: `Any`)
<a class="headerlink" href="#SemVer.inc+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="inc(version : Any, release : Any, identifier : Any)"></endpoint>
<signature id="SemVer.inc+3">SemVer.inc(**version**: `Any`, **release**: `Any`, **identifier**: `Any`)
<a class="headerlink" href="#SemVer.inc+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="inc(version : Any, release : Any, loose : Any, identifier : Any)"></endpoint>
<signature id="SemVer.inc+4">SemVer.inc(**version**: `Any`, **release**: `Any`, **loose**: `Any`, **identifier**: `Any`)
<a class="headerlink" href="#SemVer.inc+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="parse(version : Any)"></endpoint>
<signature id="SemVer.parse">SemVer.parse(**version**: `Any`)
<a class="headerlink" href="#SemVer.parse" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="parse(version : Any, loose : Any)"></endpoint>
<signature id="SemVer.parse+2">SemVer.parse(**version**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.parse+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="valid(version : Any)"></endpoint>
<signature id="SemVer.valid">SemVer.valid(**version**: `Any`)
<a class="headerlink" href="#SemVer.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="valid(version : Any, loose : Any)"></endpoint>
<signature id="SemVer.valid+2">SemVer.valid(**version**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.valid+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="clean(version : Any)"></endpoint>
<signature id="SemVer.clean">SemVer.clean(**version**: `Any`)
<a class="headerlink" href="#SemVer.clean" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="clean(version : Any, loose : Any)"></endpoint>
<signature id="SemVer.clean+2">SemVer.clean(**version**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.clean+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="diff(version1 : Any, version2 : Any)"></endpoint>
<signature id="SemVer.diff+2">SemVer.diff(**version1**: `Any`, **version2**: `Any`)
<a class="headerlink" href="#SemVer.diff+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="major(a : Any)"></endpoint>
<signature id="SemVer.major">SemVer.major(**a**: `Any`)
<a class="headerlink" href="#SemVer.major" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="major(a : Any, loose : Any)"></endpoint>
<signature id="SemVer.major+2">SemVer.major(**a**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.major+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="minor(a : Any)"></endpoint>
<signature id="SemVer.minor">SemVer.minor(**a**: `Any`)
<a class="headerlink" href="#SemVer.minor" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="minor(a : Any, loose : Any)"></endpoint>
<signature id="SemVer.minor+2">SemVer.minor(**a**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.minor+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="patch(a : Any)"></endpoint>
<signature id="SemVer.patch">SemVer.patch(**a**: `Any`)
<a class="headerlink" href="#SemVer.patch" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="patch(a : Any, loose : Any)"></endpoint>
<signature id="SemVer.patch+2">SemVer.patch(**a**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.patch+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="prerelease(a : Any)"></endpoint>
<signature id="SemVer.prerelease">SemVer.prerelease(**a**: `Any`)
<a class="headerlink" href="#SemVer.prerelease" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="prerelease(a : Any, loose : Any)"></endpoint>
<signature id="SemVer.prerelease+2">SemVer.prerelease(**a**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.prerelease+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="compare(a : Any, b : Any)"></endpoint>
<signature id="SemVer.compare+2">SemVer.compare(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.compare+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="compare(a : Any, b : Any, loose : Any)"></endpoint>
<signature id="SemVer.compare+3">SemVer.compare(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.compare+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="rcompare(a : Any, b : Any)"></endpoint>
<signature id="SemVer.rcompare+2">SemVer.rcompare(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.rcompare+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="rcompare(a : Any, b : Any, loose : Any)"></endpoint>
<signature id="SemVer.rcompare+3">SemVer.rcompare(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.rcompare+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="sort(list : Any)"></endpoint>
<signature id="SemVer.sort">SemVer.sort(**list**: `Any`)
<a class="headerlink" href="#SemVer.sort" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="sort(list : Any, loose : Any)"></endpoint>
<signature id="SemVer.sort+2">SemVer.sort(**list**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.sort+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="rsort(list : Any)"></endpoint>
<signature id="SemVer.rsort">SemVer.rsort(**list**: `Any`)
<a class="headerlink" href="#SemVer.rsort" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="rsort(list : Any, loose : Any)"></endpoint>
<signature id="SemVer.rsort+2">SemVer.rsort(**list**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.rsort+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="gt(a : Any, b : Any)"></endpoint>
<signature id="SemVer.gt+2">SemVer.gt(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.gt+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="gt(a : Any, b : Any, loose : Any)"></endpoint>
<signature id="SemVer.gt+3">SemVer.gt(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.gt+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="lt(a : Any, b : Any)"></endpoint>
<signature id="SemVer.lt+2">SemVer.lt(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.lt+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="lt(a : Any, b : Any, loose : Any)"></endpoint>
<signature id="SemVer.lt+3">SemVer.lt(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.lt+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="gte(a : Any, b : Any)"></endpoint>
<signature id="SemVer.gte+2">SemVer.gte(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.gte+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="gte(a : Any, b : Any, loose : Any)"></endpoint>
<signature id="SemVer.gte+3">SemVer.gte(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.gte+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="lte(a : Any, b : Any)"></endpoint>
<signature id="SemVer.lte+2">SemVer.lte(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.lte+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="lte(a : Any, b : Any, loose : Any)"></endpoint>
<signature id="SemVer.lte+3">SemVer.lte(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.lte+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="eq(a : Any, b : Any)"></endpoint>
<signature id="SemVer.eq+2">SemVer.eq(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.eq+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="eq(a : Any, b : Any, loose : Any)"></endpoint>
<signature id="SemVer.eq+3">SemVer.eq(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.eq+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="neq(a : Any, b : Any)"></endpoint>
<signature id="SemVer.neq+2">SemVer.neq(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.neq+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="neq(a : Any, b : Any, loose : Any)"></endpoint>
<signature id="SemVer.neq+3">SemVer.neq(**a**: `Any`, **b**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.neq+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="cmp(a : Any, op : Any, b : Any)"></endpoint>
<signature id="SemVer.cmp+3">SemVer.cmp(**a**: `Any`, **op**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.cmp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="cmp(a : Any, op : Any, b : Any, loose : Any)"></endpoint>
<signature id="SemVer.cmp+4">SemVer.cmp(**a**: `Any`, **op**: `Any`, **b**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.cmp+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="max_satisfying(versions : Any, range : Any)"></endpoint>
<signature id="SemVer.max_satisfying+2">SemVer.max_satisfying(**versions**: `Any`, **range**: `Any`)
<a class="headerlink" href="#SemVer.max_satisfying+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="max_satisfying(versions : Any, range : Any, loose : Any)"></endpoint>
<signature id="SemVer.max_satisfying+3">SemVer.max_satisfying(**versions**: `Any`, **range**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.max_satisfying+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="min_satisfying(versions : Any, range : Any)"></endpoint>
<signature id="SemVer.min_satisfying+2">SemVer.min_satisfying(**versions**: `Any`, **range**: `Any`)
<a class="headerlink" href="#SemVer.min_satisfying+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="min_satisfying(versions : Any, range : Any, loose : Any)"></endpoint>
<signature id="SemVer.min_satisfying+3">SemVer.min_satisfying(**versions**: `Any`, **range**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.min_satisfying+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="satisfies(version : Any, range : Any)"></endpoint>
<signature id="SemVer.satisfies+2">SemVer.satisfies(**version**: `Any`, **range**: `Any`)
<a class="headerlink" href="#SemVer.satisfies+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="satisfies(version : Any, range : Any, loose : Any)"></endpoint>
<signature id="SemVer.satisfies+3">SemVer.satisfies(**version**: `Any`, **range**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.satisfies+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="valid_range(range : Any)"></endpoint>
<signature id="SemVer.valid_range">SemVer.valid_range(**range**: `Any`)
<a class="headerlink" href="#SemVer.valid_range" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="valid_range(range : Any, loose : Any)"></endpoint>
<signature id="SemVer.valid_range+2">SemVer.valid_range(**range**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.valid_range+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="ltr(version : Any, range : Any)"></endpoint>
<signature id="SemVer.ltr+2">SemVer.ltr(**version**: `Any`, **range**: `Any`)
<a class="headerlink" href="#SemVer.ltr+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="ltr(version : Any, range : Any, loose : Any)"></endpoint>
<signature id="SemVer.ltr+3">SemVer.ltr(**version**: `Any`, **range**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.ltr+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="gtr(version : Any, range : Any)"></endpoint>
<signature id="SemVer.gtr+2">SemVer.gtr(**version**: `Any`, **range**: `Any`)
<a class="headerlink" href="#SemVer.gtr+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="gtr(version : Any, range : Any, loose : Any)"></endpoint>
<signature id="SemVer.gtr+3">SemVer.gtr(**version**: `Any`, **range**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.gtr+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="outside(version : Any, range : Any, hilo : Any)"></endpoint>
<signature id="SemVer.outside+3">SemVer.outside(**version**: `Any`, **range**: `Any`, **hilo**: `Any`)
<a class="headerlink" href="#SemVer.outside+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="outside(version : Any, range : Any, hilo : Any, loose : Any)"></endpoint>
<signature id="SemVer.outside+4">SemVer.outside(**version**: `Any`, **range**: `Any`, **hilo**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVer.outside+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="debug(a : Any)"></endpoint>
<signature id="SemVer.debug">SemVer.debug(**a**: `Any`)
<a class="headerlink" href="#SemVer.debug" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="compare_main(other : Any)"></endpoint>
<signature id="SemVer.compare_main">SemVer.compare_main(**other**: `Any`)
<a class="headerlink" href="#SemVer.compare_main" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="first_not_zero(a : Any, b : Any)"></endpoint>
<signature id="SemVer.first_not_zero+2">SemVer.first_not_zero(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.first_not_zero+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="first_not_zero(a : Any, b : Any, c : Any)"></endpoint>
<signature id="SemVer.first_not_zero+3">SemVer.first_not_zero(**a**: `Any`, **b**: `Any`, **c**: `Any`)
<a class="headerlink" href="#SemVer.first_not_zero+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="compare_pre(other : Any)"></endpoint>
<signature id="SemVer.compare_pre">SemVer.compare_pre(**other**: `Any`)
<a class="headerlink" href="#SemVer.compare_pre" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVer" signature="compare_identifiers(a : Any, b : Any)"></endpoint>
<signature id="SemVer.compare_identifiers+2">SemVer.compare_identifiers(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVer.compare_identifiers+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SemVerRange
`:::js import "luxe: semver" for SemVerRange`
> no docs found

- [any](#SemVerRange.any)
- [empty](#SemVerRange.empty)
- [debug](#SemVerRange.debug)(**a**: `Any`)
- [set](#SemVerRange.set)
- [loose](#SemVerRange.loose)
- [range](#SemVerRange.range)
- [raw](#SemVerRange.raw)
- [isEmpty](#SemVerRange.isEmpty)
- [isAny](#SemVerRange.isAny)
- [new](#SemVerRange.new)(**range**: `Any`)
- [new](#SemVerRange.new+2)(**range**: `Any`, **loose**: `Any`)
- [create](#SemVerRange.create+2)(**range**: `Any`, **loose**: `Any`)
- [format](#SemVerRange.format)()
- [union](#SemVerRange.union)(**other**: `Any`)
- [intersects](#SemVerRange.intersects)(**range**: `Any`)
- [intersects](#SemVerRange.intersects+2)(**range**: `Any`, **loose**: `Any`)
- [pick_not_infinite](#SemVerRange.pick_not_infinite+2)(**a**: `Any`, **b**: `Any`)
- [pick_infinite](#SemVerRange.pick_infinite+2)(**a**: `Any`, **b**: `Any`)
- [comparator_intersection](#SemVerRange.comparator_intersection+2)(**a**: `Any`, **b**: `Any`)
- [intersection](#SemVerRange.intersection)(**other**: `Any`)
- [inverted](#SemVerRange.inverted)()
- [subset_contains](#SemVerRange.subset_contains)(**other**: `Any`)
- [subset_contains](#SemVerRange.subset_contains+2)(**other**: `Any`, **loose**: `Any`)
- [subset_of](#SemVerRange.subset_of)(**other**: `Any`)
- [subset_of](#SemVerRange.subset_of+2)(**other**: `Any`, **loose**: `Any`)
- [subset](#SemVerRange.subset+2)(**needle**: `Any`, **haystack**: `Any`)
- [subset](#SemVerRange.subset+3)(**needle**: `Any`, **haystack**: `Any`, **loose**: `Any`)
- [test](#SemVerRange.test)(**version**: `Any`)
- [is_x](#SemVerRange.is_x)(**id**: `Any`)
- [test_set](#SemVerRange.test_set+2)(**set**: `Any`, **version**: `Any`)
- [parse_range](#SemVerRange.parse_range)(**range**: `Any`)
- [parse_comparator](#SemVerRange.parse_comparator+2)(**comp**: `Any`, **loose**: `Any`)
- [replace_carets](#SemVerRange.replace_carets+2)(**comp**: `Any`, **loose**: `Any`)
- [replace_caret](#SemVerRange.replace_caret+2)(**comp**: `Any`, **loose**: `Any`)
- [replace_tildes](#SemVerRange.replace_tildes+2)(**comp**: `Any`, **loose**: `Any`)
- [replace_tilde](#SemVerRange.replace_tilde+2)(**comp**: `Any`, **loose**: `Any`)
- [replace_x_ranges](#SemVerRange.replace_x_ranges+2)(**comp**: `Any`, **loose**: `Any`)
- [replace_x_range](#SemVerRange.replace_x_range+2)(**comp**: `Any`, **loose**: `Any`)
- [replace_stars](#SemVerRange.replace_stars+2)(**comp**: `Any`, **loose**: `Any`)

<hr/>
<endpoint module="luxe: semver" class="SemVerRange" signature="any"></endpoint>
<signature id="SemVerRange.any">SemVerRange.any
<a class="headerlink" href="#SemVerRange.any" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="empty"></endpoint>
<signature id="SemVerRange.empty">SemVerRange.empty
<a class="headerlink" href="#SemVerRange.empty" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="debug(a : Any)"></endpoint>
<signature id="SemVerRange.debug">SemVerRange.debug(**a**: `Any`)
<a class="headerlink" href="#SemVerRange.debug" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="set"></endpoint>
<signature id="SemVerRange.set">SemVerRange.set
<a class="headerlink" href="#SemVerRange.set" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="loose"></endpoint>
<signature id="SemVerRange.loose">SemVerRange.loose
<a class="headerlink" href="#SemVerRange.loose" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="range"></endpoint>
<signature id="SemVerRange.range">SemVerRange.range
<a class="headerlink" href="#SemVerRange.range" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="raw"></endpoint>
<signature id="SemVerRange.raw">SemVerRange.raw
<a class="headerlink" href="#SemVerRange.raw" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="isEmpty"></endpoint>
<signature id="SemVerRange.isEmpty">SemVerRange.isEmpty
<a class="headerlink" href="#SemVerRange.isEmpty" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="isAny"></endpoint>
<signature id="SemVerRange.isAny">SemVerRange.isAny
<a class="headerlink" href="#SemVerRange.isAny" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="new(range : Any)"></endpoint>
<signature id="SemVerRange.new">SemVerRange.new(**range**: `Any`)
<a class="headerlink" href="#SemVerRange.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SemVerRange`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="new(range : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.new+2">SemVerRange.new(**range**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SemVerRange`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="create(range : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.create+2">SemVerRange.create(**range**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SemVerRange`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="format()"></endpoint>
<signature id="SemVerRange.format">SemVerRange.format()
<a class="headerlink" href="#SemVerRange.format" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="union(other : Any)"></endpoint>
<signature id="SemVerRange.union">SemVerRange.union(**other**: `Any`)
<a class="headerlink" href="#SemVerRange.union" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="intersects(range : Any)"></endpoint>
<signature id="SemVerRange.intersects">SemVerRange.intersects(**range**: `Any`)
<a class="headerlink" href="#SemVerRange.intersects" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="intersects(range : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.intersects+2">SemVerRange.intersects(**range**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.intersects+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="pick_not_infinite(a : Any, b : Any)"></endpoint>
<signature id="SemVerRange.pick_not_infinite+2">SemVerRange.pick_not_infinite(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVerRange.pick_not_infinite+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="pick_infinite(a : Any, b : Any)"></endpoint>
<signature id="SemVerRange.pick_infinite+2">SemVerRange.pick_infinite(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVerRange.pick_infinite+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="comparator_intersection(a : Any, b : Any)"></endpoint>
<signature id="SemVerRange.comparator_intersection+2">SemVerRange.comparator_intersection(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#SemVerRange.comparator_intersection+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="intersection(other : Any)"></endpoint>
<signature id="SemVerRange.intersection">SemVerRange.intersection(**other**: `Any`)
<a class="headerlink" href="#SemVerRange.intersection" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="inverted()"></endpoint>
<signature id="SemVerRange.inverted">SemVerRange.inverted()
<a class="headerlink" href="#SemVerRange.inverted" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="subset_contains(other : Any)"></endpoint>
<signature id="SemVerRange.subset_contains">SemVerRange.subset_contains(**other**: `Any`)
<a class="headerlink" href="#SemVerRange.subset_contains" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="subset_contains(other : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.subset_contains+2">SemVerRange.subset_contains(**other**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.subset_contains+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="subset_of(other : Any)"></endpoint>
<signature id="SemVerRange.subset_of">SemVerRange.subset_of(**other**: `Any`)
<a class="headerlink" href="#SemVerRange.subset_of" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="subset_of(other : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.subset_of+2">SemVerRange.subset_of(**other**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.subset_of+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="subset(needle : Any, haystack : Any)"></endpoint>
<signature id="SemVerRange.subset+2">SemVerRange.subset(**needle**: `Any`, **haystack**: `Any`)
<a class="headerlink" href="#SemVerRange.subset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="subset(needle : Any, haystack : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.subset+3">SemVerRange.subset(**needle**: `Any`, **haystack**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.subset+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="test(version : Any)"></endpoint>
<signature id="SemVerRange.test">SemVerRange.test(**version**: `Any`)
<a class="headerlink" href="#SemVerRange.test" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="is_x(id : Any)"></endpoint>
<signature id="SemVerRange.is_x">SemVerRange.is_x(**id**: `Any`)
<a class="headerlink" href="#SemVerRange.is_x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="test_set(set : Any, version : Any)"></endpoint>
<signature id="SemVerRange.test_set+2">SemVerRange.test_set(**set**: `Any`, **version**: `Any`)
<a class="headerlink" href="#SemVerRange.test_set+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="parse_range(range : Any)"></endpoint>
<signature id="SemVerRange.parse_range">SemVerRange.parse_range(**range**: `Any`)
<a class="headerlink" href="#SemVerRange.parse_range" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="parse_comparator(comp : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.parse_comparator+2">SemVerRange.parse_comparator(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.parse_comparator+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="replace_carets(comp : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.replace_carets+2">SemVerRange.replace_carets(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.replace_carets+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="replace_caret(comp : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.replace_caret+2">SemVerRange.replace_caret(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.replace_caret+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="replace_tildes(comp : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.replace_tildes+2">SemVerRange.replace_tildes(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.replace_tildes+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="replace_tilde(comp : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.replace_tilde+2">SemVerRange.replace_tilde(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.replace_tilde+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="replace_x_ranges(comp : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.replace_x_ranges+2">SemVerRange.replace_x_ranges(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.replace_x_ranges+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="replace_x_range(comp : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.replace_x_range+2">SemVerRange.replace_x_range(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.replace_x_range+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerRange" signature="replace_stars(comp : Any, loose : Any)"></endpoint>
<signature id="SemVerRange.replace_stars+2">SemVerRange.replace_stars(**comp**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerRange.replace_stars+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SemVerSubset
`:::js import "luxe: semver" for SemVerSubset`
> no docs found

- [subset](#SemVerSubset.subset+2)(**needle**: `Any`, **haystack**: `Any`)
- [subset](#SemVerSubset.subset+3)(**needle**: `Any`, **haystack**: `Any`, **loose**: `Any`)
- [gen_interval](#SemVerSubset.gen_interval)(**comparators**: `Any`)
- [orderEq](#SemVerSubset.orderEq+2)(**v1**: `Any`, **v2**: `Any`)
- [orderGt](#SemVerSubset.orderGt+2)(**v1**: `Any`, **v2**: `Any`)
- [orderLt](#SemVerSubset.orderLt+2)(**v1**: `Any`, **v2**: `Any`)
- [isSubset](#SemVerSubset.isSubset+2)(**needle**: `Any`, **haystack**: `Any`)

<hr/>
<endpoint module="luxe: semver" class="SemVerSubset" signature="subset(needle : Any, haystack : Any)"></endpoint>
<signature id="SemVerSubset.subset+2">SemVerSubset.subset(**needle**: `Any`, **haystack**: `Any`)
<a class="headerlink" href="#SemVerSubset.subset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubset" signature="subset(needle : Any, haystack : Any, loose : Any)"></endpoint>
<signature id="SemVerSubset.subset+3">SemVerSubset.subset(**needle**: `Any`, **haystack**: `Any`, **loose**: `Any`)
<a class="headerlink" href="#SemVerSubset.subset+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubset" signature="gen_interval(comparators : Any)"></endpoint>
<signature id="SemVerSubset.gen_interval">SemVerSubset.gen_interval(**comparators**: `Any`)
<a class="headerlink" href="#SemVerSubset.gen_interval" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubset" signature="orderEq(v1 : Any, v2 : Any)"></endpoint>
<signature id="SemVerSubset.orderEq+2">SemVerSubset.orderEq(**v1**: `Any`, **v2**: `Any`)
<a class="headerlink" href="#SemVerSubset.orderEq+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubset" signature="orderGt(v1 : Any, v2 : Any)"></endpoint>
<signature id="SemVerSubset.orderGt+2">SemVerSubset.orderGt(**v1**: `Any`, **v2**: `Any`)
<a class="headerlink" href="#SemVerSubset.orderGt+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubset" signature="orderLt(v1 : Any, v2 : Any)"></endpoint>
<signature id="SemVerSubset.orderLt+2">SemVerSubset.orderLt(**v1**: `Any`, **v2**: `Any`)
<a class="headerlink" href="#SemVerSubset.orderLt+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubset" signature="isSubset(needle : Any, haystack : Any)"></endpoint>
<signature id="SemVerSubset.isSubset+2">SemVerSubset.isSubset(**needle**: `Any`, **haystack**: `Any`)
<a class="headerlink" href="#SemVerSubset.isSubset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SemVerSubsetInterval
`:::js import "luxe: semver" for SemVerSubsetInterval`
> no docs found

- [left](#SemVerSubsetInterval.left)
- [right](#SemVerSubsetInterval.right)
- [leftValue](#SemVerSubsetInterval.leftValue)
- [rightValue](#SemVerSubsetInterval.rightValue)
- [new](#SemVerSubsetInterval.new+4)(**left**: `Any`, **leftValue**: `Any`, **rightValue**: `Any`, **right**: `Any`)

<hr/>
<endpoint module="luxe: semver" class="SemVerSubsetInterval" signature="left"></endpoint>
<signature id="SemVerSubsetInterval.left">SemVerSubsetInterval.left
<a class="headerlink" href="#SemVerSubsetInterval.left" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubsetInterval" signature="right"></endpoint>
<signature id="SemVerSubsetInterval.right">SemVerSubsetInterval.right
<a class="headerlink" href="#SemVerSubsetInterval.right" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubsetInterval" signature="leftValue"></endpoint>
<signature id="SemVerSubsetInterval.leftValue">SemVerSubsetInterval.leftValue
<a class="headerlink" href="#SemVerSubsetInterval.leftValue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubsetInterval" signature="rightValue"></endpoint>
<signature id="SemVerSubsetInterval.rightValue">SemVerSubsetInterval.rightValue
<a class="headerlink" href="#SemVerSubsetInterval.rightValue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: semver" class="SemVerSubsetInterval" signature="new(left : Any, leftValue : Any, rightValue : Any, right : Any)"></endpoint>
<signature id="SemVerSubsetInterval.new+4">SemVerSubsetInterval.new(**left**: `Any`, **leftValue**: `Any`, **rightValue**: `Any`, **right**: `Any`)
<a class="headerlink" href="#SemVerSubsetInterval.new+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SemVerSubsetInterval`
> no docs found   

