#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.9`)  


---

## `luxe: test` module

- [BaseMatchers](#basematchers)   
- [ConsoleReporter](#consolereporter)   
- [Expectation](#expectation)   
- [FiberMatchers](#fibermatchers)   
- [Matchers](#matchers)   
- [NumMatchers](#nummatchers)   
- [RangeMatchers](#rangematchers)   
- [Reporter](#reporter)   
- [Runnable](#runnable)   
- [Skippable](#skippable)   
- [Stub](#stub)   
- [StubMatchers](#stubmatchers)   
- [Suite](#suite)   

---

### BaseMatchers
`:::js import "luxe: test" for BaseMatchers`
> no docs found

- [new](#BaseMatchers.new)(**value**: `Any`)
- [value](#BaseMatchers.value)
- [not](#BaseMatchers.not)
- [toBe](#BaseMatchers.toBe)(**klass**: `Any`)
- [toBeFalse](#BaseMatchers.toBeFalse)
- [toBeTrue](#BaseMatchers.toBeTrue)
- [toBeNull](#BaseMatchers.toBeNull)
- [toEqual](#BaseMatchers.toEqual)(**other**: `Any`)
- [toEqualDeeply](#BaseMatchers.toEqualDeeply)(**other**: `Any`)

<hr/>
<endpoint module="luxe: test" class="BaseMatchers" signature="new(value : Any)"></endpoint>
<signature id="BaseMatchers.new">BaseMatchers.new(**value**: `Any`)
<a class="headerlink" href="#BaseMatchers.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js BaseMatchers`
> no docs found   

<endpoint module="luxe: test" class="BaseMatchers" signature="value"></endpoint>
<signature id="BaseMatchers.value">BaseMatchers.value
<a class="headerlink" href="#BaseMatchers.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="BaseMatchers" signature="not"></endpoint>
<signature id="BaseMatchers.not">BaseMatchers.not
<a class="headerlink" href="#BaseMatchers.not" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="BaseMatchers" signature="toBe(klass : Any)"></endpoint>
<signature id="BaseMatchers.toBe">BaseMatchers.toBe(**klass**: `Any`)
<a class="headerlink" href="#BaseMatchers.toBe" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="BaseMatchers" signature="toBeFalse"></endpoint>
<signature id="BaseMatchers.toBeFalse">BaseMatchers.toBeFalse
<a class="headerlink" href="#BaseMatchers.toBeFalse" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="BaseMatchers" signature="toBeTrue"></endpoint>
<signature id="BaseMatchers.toBeTrue">BaseMatchers.toBeTrue
<a class="headerlink" href="#BaseMatchers.toBeTrue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="BaseMatchers" signature="toBeNull"></endpoint>
<signature id="BaseMatchers.toBeNull">BaseMatchers.toBeNull
<a class="headerlink" href="#BaseMatchers.toBeNull" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="BaseMatchers" signature="toEqual(other : Any)"></endpoint>
<signature id="BaseMatchers.toEqual">BaseMatchers.toEqual(**other**: `Any`)
<a class="headerlink" href="#BaseMatchers.toEqual" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="BaseMatchers" signature="toEqualDeeply(other : Any)"></endpoint>
<signature id="BaseMatchers.toEqualDeeply">BaseMatchers.toEqualDeeply(**other**: `Any`)
<a class="headerlink" href="#BaseMatchers.toEqualDeeply" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ConsoleReporter
`:::js import "luxe: test" for ConsoleReporter`
> no docs found

- [new](#ConsoleReporter.new)()
- [print_colors](#ConsoleReporter.print_colors=)=(v : Any)
- [epilogue](#ConsoleReporter.epilogue)()
- [runnableSkipped](#ConsoleReporter.runnableSkipped)(**skippable**: `Any`)
- [suiteStart](#ConsoleReporter.suiteStart)(**title**: `Any`)
- [suiteEnd](#ConsoleReporter.suiteEnd)(**title**: `Any`)
- [testStart](#ConsoleReporter.testStart)(**runnable**: `Any`)
- [testEnd](#ConsoleReporter.testEnd)(**runnable**: `Any`)
- [testPassed](#ConsoleReporter.testPassed)(**runnable**: `Any`)
- [testFailed](#ConsoleReporter.testFailed)(**runnable**: `Any`)
- [testError](#ConsoleReporter.testError)(**runnable**: `Any`)

<hr/>
<endpoint module="luxe: test" class="ConsoleReporter" signature="new()"></endpoint>
<signature id="ConsoleReporter.new">ConsoleReporter.new()
<a class="headerlink" href="#ConsoleReporter.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ConsoleReporter`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="print_colors=(v : Any)"></endpoint>
<signature id="ConsoleReporter.print_colors=">ConsoleReporter.print_colors=(v : Any)
<a class="headerlink" href="#ConsoleReporter.print_colors=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="epilogue()"></endpoint>
<signature id="ConsoleReporter.epilogue">ConsoleReporter.epilogue()
<a class="headerlink" href="#ConsoleReporter.epilogue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="runnableSkipped(skippable : Any)"></endpoint>
<signature id="ConsoleReporter.runnableSkipped">ConsoleReporter.runnableSkipped(**skippable**: `Any`)
<a class="headerlink" href="#ConsoleReporter.runnableSkipped" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="suiteStart(title : Any)"></endpoint>
<signature id="ConsoleReporter.suiteStart">ConsoleReporter.suiteStart(**title**: `Any`)
<a class="headerlink" href="#ConsoleReporter.suiteStart" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="suiteEnd(title : Any)"></endpoint>
<signature id="ConsoleReporter.suiteEnd">ConsoleReporter.suiteEnd(**title**: `Any`)
<a class="headerlink" href="#ConsoleReporter.suiteEnd" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="testStart(runnable : Any)"></endpoint>
<signature id="ConsoleReporter.testStart">ConsoleReporter.testStart(**runnable**: `Any`)
<a class="headerlink" href="#ConsoleReporter.testStart" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="testEnd(runnable : Any)"></endpoint>
<signature id="ConsoleReporter.testEnd">ConsoleReporter.testEnd(**runnable**: `Any`)
<a class="headerlink" href="#ConsoleReporter.testEnd" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="testPassed(runnable : Any)"></endpoint>
<signature id="ConsoleReporter.testPassed">ConsoleReporter.testPassed(**runnable**: `Any`)
<a class="headerlink" href="#ConsoleReporter.testPassed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="testFailed(runnable : Any)"></endpoint>
<signature id="ConsoleReporter.testFailed">ConsoleReporter.testFailed(**runnable**: `Any`)
<a class="headerlink" href="#ConsoleReporter.testFailed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="ConsoleReporter" signature="testError(runnable : Any)"></endpoint>
<signature id="ConsoleReporter.testError">ConsoleReporter.testError(**runnable**: `Any`)
<a class="headerlink" href="#ConsoleReporter.testError" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Expectation
`:::js import "luxe: test" for Expectation`
> no docs found

- [new](#Expectation.new+2)(**passed**: `Any`, **message**: `Any`)
- [passed](#Expectation.passed)
- [message](#Expectation.message)

<hr/>
<endpoint module="luxe: test" class="Expectation" signature="new(passed : Any, message : Any)"></endpoint>
<signature id="Expectation.new+2">Expectation.new(**passed**: `Any`, **message**: `Any`)
<a class="headerlink" href="#Expectation.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Expectation`
> no docs found   

<endpoint module="luxe: test" class="Expectation" signature="passed"></endpoint>
<signature id="Expectation.passed">Expectation.passed
<a class="headerlink" href="#Expectation.passed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Expectation" signature="message"></endpoint>
<signature id="Expectation.message">Expectation.message
<a class="headerlink" href="#Expectation.message" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### FiberMatchers
`:::js import "luxe: test" for FiberMatchers`
> no docs found

- [new](#FiberMatchers.new)(**value**: `Any`)
- [toBeARuntimeError](#FiberMatchers.toBeARuntimeError)
- [toBeARuntimeError](#FiberMatchers.toBeARuntimeError)(**errorMessage**: `Any`)
- [toBeDone](#FiberMatchers.toBeDone)

<hr/>
<endpoint module="luxe: test" class="FiberMatchers" signature="new(value : Any)"></endpoint>
<signature id="FiberMatchers.new">FiberMatchers.new(**value**: `Any`)
<a class="headerlink" href="#FiberMatchers.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js FiberMatchers`
> no docs found   

<endpoint module="luxe: test" class="FiberMatchers" signature="toBeARuntimeError"></endpoint>
<signature id="FiberMatchers.toBeARuntimeError">FiberMatchers.toBeARuntimeError
<a class="headerlink" href="#FiberMatchers.toBeARuntimeError" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="FiberMatchers" signature="toBeARuntimeError(errorMessage : Any)"></endpoint>
<signature id="FiberMatchers.toBeARuntimeError">FiberMatchers.toBeARuntimeError(**errorMessage**: `Any`)
<a class="headerlink" href="#FiberMatchers.toBeARuntimeError" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="FiberMatchers" signature="toBeDone"></endpoint>
<signature id="FiberMatchers.toBeDone">FiberMatchers.toBeDone
<a class="headerlink" href="#FiberMatchers.toBeDone" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Matchers
`:::js import "luxe: test" for Matchers`
> no docs found

- [new](#Matchers.new)(**value**: `Any`)

<hr/>
<endpoint module="luxe: test" class="Matchers" signature="new(value : Any)"></endpoint>
<signature id="Matchers.new">Matchers.new(**value**: `Any`)
<a class="headerlink" href="#Matchers.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Matchers`
> no docs found   

### NumMatchers
`:::js import "luxe: test" for NumMatchers`
> no docs found

- [new](#NumMatchers.new)(**value**: `Any`)
- [toBeGreaterThan](#NumMatchers.toBeGreaterThan)(**other**: `Any`)
- [toBeLessThan](#NumMatchers.toBeLessThan)(**other**: `Any`)
- [toBeBetween](#NumMatchers.toBeBetween+2)(**min**: `Any`, **max**: `Any`)

<hr/>
<endpoint module="luxe: test" class="NumMatchers" signature="new(value : Any)"></endpoint>
<signature id="NumMatchers.new">NumMatchers.new(**value**: `Any`)
<a class="headerlink" href="#NumMatchers.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js NumMatchers`
> no docs found   

<endpoint module="luxe: test" class="NumMatchers" signature="toBeGreaterThan(other : Any)"></endpoint>
<signature id="NumMatchers.toBeGreaterThan">NumMatchers.toBeGreaterThan(**other**: `Any`)
<a class="headerlink" href="#NumMatchers.toBeGreaterThan" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="NumMatchers" signature="toBeLessThan(other : Any)"></endpoint>
<signature id="NumMatchers.toBeLessThan">NumMatchers.toBeLessThan(**other**: `Any`)
<a class="headerlink" href="#NumMatchers.toBeLessThan" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="NumMatchers" signature="toBeBetween(min : Any, max : Any)"></endpoint>
<signature id="NumMatchers.toBeBetween+2">NumMatchers.toBeBetween(**min**: `Any`, **max**: `Any`)
<a class="headerlink" href="#NumMatchers.toBeBetween+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### RangeMatchers
`:::js import "luxe: test" for RangeMatchers`
> no docs found

- [new](#RangeMatchers.new)(**value**: `Any`)
- [toContain](#RangeMatchers.toContain)(**other**: `Any`)
- [toBeContainedBy](#RangeMatchers.toBeContainedBy)(**other**: `Any`)

<hr/>
<endpoint module="luxe: test" class="RangeMatchers" signature="new(value : Any)"></endpoint>
<signature id="RangeMatchers.new">RangeMatchers.new(**value**: `Any`)
<a class="headerlink" href="#RangeMatchers.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RangeMatchers`
> no docs found   

<endpoint module="luxe: test" class="RangeMatchers" signature="toContain(other : Any)"></endpoint>
<signature id="RangeMatchers.toContain">RangeMatchers.toContain(**other**: `Any`)
<a class="headerlink" href="#RangeMatchers.toContain" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="RangeMatchers" signature="toBeContainedBy(other : Any)"></endpoint>
<signature id="RangeMatchers.toBeContainedBy">RangeMatchers.toBeContainedBy(**other**: `Any`)
<a class="headerlink" href="#RangeMatchers.toBeContainedBy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Reporter
`:::js import "luxe: test" for Reporter`
> no docs found

- [epilogue](#Reporter.epilogue)()
- [runnableSkipped](#Reporter.runnableSkipped)(**skippable**: `Any`)
- [suiteStart](#Reporter.suiteStart)(**title**: `Any`)
- [suiteEnd](#Reporter.suiteEnd)(**title**: `Any`)
- [testStart](#Reporter.testStart)(**runnable**: `Any`)
- [testPassed](#Reporter.testPassed)(**runnable**: `Any`)
- [testFailed](#Reporter.testFailed)(**runnable**: `Any`)
- [testError](#Reporter.testError)(**runnable**: `Any`)
- [testEnd](#Reporter.testEnd)(**runnable**: `Any`)

<hr/>
<endpoint module="luxe: test" class="Reporter" signature="epilogue()"></endpoint>
<signature id="Reporter.epilogue">Reporter.epilogue()
<a class="headerlink" href="#Reporter.epilogue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Reporter" signature="runnableSkipped(skippable : Any)"></endpoint>
<signature id="Reporter.runnableSkipped">Reporter.runnableSkipped(**skippable**: `Any`)
<a class="headerlink" href="#Reporter.runnableSkipped" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Reporter" signature="suiteStart(title : Any)"></endpoint>
<signature id="Reporter.suiteStart">Reporter.suiteStart(**title**: `Any`)
<a class="headerlink" href="#Reporter.suiteStart" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Reporter" signature="suiteEnd(title : Any)"></endpoint>
<signature id="Reporter.suiteEnd">Reporter.suiteEnd(**title**: `Any`)
<a class="headerlink" href="#Reporter.suiteEnd" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Reporter" signature="testStart(runnable : Any)"></endpoint>
<signature id="Reporter.testStart">Reporter.testStart(**runnable**: `Any`)
<a class="headerlink" href="#Reporter.testStart" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Reporter" signature="testPassed(runnable : Any)"></endpoint>
<signature id="Reporter.testPassed">Reporter.testPassed(**runnable**: `Any`)
<a class="headerlink" href="#Reporter.testPassed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Reporter" signature="testFailed(runnable : Any)"></endpoint>
<signature id="Reporter.testFailed">Reporter.testFailed(**runnable**: `Any`)
<a class="headerlink" href="#Reporter.testFailed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Reporter" signature="testError(runnable : Any)"></endpoint>
<signature id="Reporter.testError">Reporter.testError(**runnable**: `Any`)
<a class="headerlink" href="#Reporter.testError" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Reporter" signature="testEnd(runnable : Any)"></endpoint>
<signature id="Reporter.testEnd">Reporter.testEnd(**runnable**: `Any`)
<a class="headerlink" href="#Reporter.testEnd" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Runnable
`:::js import "luxe: test" for Runnable`
> no docs found

- [new](#Runnable.new+4)(**title**: `Any`, **beforeEaches**: `Any`, **afterEaches**: `Any`, **fn**: `Any`)
- [duration](#Runnable.duration)
- [error](#Runnable.error)
- [expectations](#Runnable.expectations)
- [hasRun](#Runnable.hasRun)
- [run](#Runnable.run)()
- [title](#Runnable.title)

<hr/>
<endpoint module="luxe: test" class="Runnable" signature="new(title : Any, beforeEaches : Any, afterEaches : Any, fn : Any)"></endpoint>
<signature id="Runnable.new+4">Runnable.new(**title**: `Any`, **beforeEaches**: `Any`, **afterEaches**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Runnable.new+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Runnable`
> no docs found   

<endpoint module="luxe: test" class="Runnable" signature="duration"></endpoint>
<signature id="Runnable.duration">Runnable.duration
<a class="headerlink" href="#Runnable.duration" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Runnable" signature="error"></endpoint>
<signature id="Runnable.error">Runnable.error
<a class="headerlink" href="#Runnable.error" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Runnable" signature="expectations"></endpoint>
<signature id="Runnable.expectations">Runnable.expectations
<a class="headerlink" href="#Runnable.expectations" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Runnable" signature="hasRun"></endpoint>
<signature id="Runnable.hasRun">Runnable.hasRun
<a class="headerlink" href="#Runnable.hasRun" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Runnable" signature="run()"></endpoint>
<signature id="Runnable.run">Runnable.run()
<a class="headerlink" href="#Runnable.run" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Runnable" signature="title"></endpoint>
<signature id="Runnable.title">Runnable.title
<a class="headerlink" href="#Runnable.title" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Skippable
`:::js import "luxe: test" for Skippable`
> no docs found

- [new](#Skippable.new)(**title**: `Any`)
- [run](#Skippable.run)
- [title](#Skippable.title)

<hr/>
<endpoint module="luxe: test" class="Skippable" signature="new(title : Any)"></endpoint>
<signature id="Skippable.new">Skippable.new(**title**: `Any`)
<a class="headerlink" href="#Skippable.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Skippable`
> no docs found   

<endpoint module="luxe: test" class="Skippable" signature="run"></endpoint>
<signature id="Skippable.run">Skippable.run
<a class="headerlink" href="#Skippable.run" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Skippable" signature="title"></endpoint>
<signature id="Skippable.title">Skippable.title
<a class="headerlink" href="#Skippable.title" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Stub
`:::js import "luxe: test" for Stub`
> no docs found

- [new](#Stub.new)(**name**: `Any`)
- [new](#Stub.new+2)(**name**: `Any`, **fakeFn**: `Any`)
- [andCallFake](#Stub.andCallFake+2)(**name**: `Any`, **fakeFn**: `Any`)
- [andReturnValue](#Stub.andReturnValue+2)(**name**: `Any`, **returnValue**: `Any`)
- [called](#Stub.called)
- [calls](#Stub.calls)
- [firstCall](#Stub.firstCall)
- [mostRecentCall](#Stub.mostRecentCall)
- [name](#Stub.name)
- [reset](#Stub.reset)
- [call](#Stub.call)
- [call](#Stub.call)()
- [call](#Stub.call)(**a**: `Any`)
- [call](#Stub.call+2)(**a**: `Any`, **b**: `Any`)
- [call](#Stub.call+3)(**a**: `Any`, **b**: `Any`, **c**: `Any`)
- [call](#Stub.call+4)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`)
- [call](#Stub.call+5)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`)
- [call](#Stub.call+6)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`)
- [call](#Stub.call+7)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`)
- [call](#Stub.call+8)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`)
- [call](#Stub.call+9)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`)
- [call](#Stub.call+10)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`)
- [call](#Stub.call+11)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`)
- [call](#Stub.call+12)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`)
- [call](#Stub.call+13)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`)
- [call](#Stub.call+14)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`, **n**: `Any`)
- [call](#Stub.call+15)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`, **n**: `Any`, **o**: `Any`)
- [call](#Stub.call+16)(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`, **n**: `Any`, **o**: `Any`, **p**: `Any`)

<hr/>
<endpoint module="luxe: test" class="Stub" signature="new(name : Any)"></endpoint>
<signature id="Stub.new">Stub.new(**name**: `Any`)
<a class="headerlink" href="#Stub.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Stub`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="new(name : Any, fakeFn : Any)"></endpoint>
<signature id="Stub.new+2">Stub.new(**name**: `Any`, **fakeFn**: `Any`)
<a class="headerlink" href="#Stub.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Stub`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="andCallFake(name : Any, fakeFn : Any)"></endpoint>
<signature id="Stub.andCallFake+2">Stub.andCallFake(**name**: `Any`, **fakeFn**: `Any`)
<a class="headerlink" href="#Stub.andCallFake+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="andReturnValue(name : Any, returnValue : Any)"></endpoint>
<signature id="Stub.andReturnValue+2">Stub.andReturnValue(**name**: `Any`, **returnValue**: `Any`)
<a class="headerlink" href="#Stub.andReturnValue+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="called"></endpoint>
<signature id="Stub.called">Stub.called
<a class="headerlink" href="#Stub.called" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="calls"></endpoint>
<signature id="Stub.calls">Stub.calls
<a class="headerlink" href="#Stub.calls" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="firstCall"></endpoint>
<signature id="Stub.firstCall">Stub.firstCall
<a class="headerlink" href="#Stub.firstCall" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="mostRecentCall"></endpoint>
<signature id="Stub.mostRecentCall">Stub.mostRecentCall
<a class="headerlink" href="#Stub.mostRecentCall" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="name"></endpoint>
<signature id="Stub.name">Stub.name
<a class="headerlink" href="#Stub.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="reset"></endpoint>
<signature id="Stub.reset">Stub.reset
<a class="headerlink" href="#Stub.reset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call"></endpoint>
<signature id="Stub.call">Stub.call
<a class="headerlink" href="#Stub.call" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call()"></endpoint>
<signature id="Stub.call">Stub.call()
<a class="headerlink" href="#Stub.call" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any)"></endpoint>
<signature id="Stub.call">Stub.call(**a**: `Any`)
<a class="headerlink" href="#Stub.call" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any)"></endpoint>
<signature id="Stub.call+2">Stub.call(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#Stub.call+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any)"></endpoint>
<signature id="Stub.call+3">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`)
<a class="headerlink" href="#Stub.call+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any)"></endpoint>
<signature id="Stub.call+4">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`)
<a class="headerlink" href="#Stub.call+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any)"></endpoint>
<signature id="Stub.call+5">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`)
<a class="headerlink" href="#Stub.call+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any)"></endpoint>
<signature id="Stub.call+6">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`)
<a class="headerlink" href="#Stub.call+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any)"></endpoint>
<signature id="Stub.call+7">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`)
<a class="headerlink" href="#Stub.call+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any, h : Any)"></endpoint>
<signature id="Stub.call+8">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`)
<a class="headerlink" href="#Stub.call+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any, h : Any, i : Any)"></endpoint>
<signature id="Stub.call+9">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`)
<a class="headerlink" href="#Stub.call+9" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any, h : Any, i : Any, j : Any)"></endpoint>
<signature id="Stub.call+10">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`)
<a class="headerlink" href="#Stub.call+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any, h : Any, i : Any, j : Any, k : Any)"></endpoint>
<signature id="Stub.call+11">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`)
<a class="headerlink" href="#Stub.call+11" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any, h : Any, i : Any, j : Any, k : Any, l : Any)"></endpoint>
<signature id="Stub.call+12">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`)
<a class="headerlink" href="#Stub.call+12" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any, h : Any, i : Any, j : Any, k : Any, l : Any, m : Any)"></endpoint>
<signature id="Stub.call+13">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`)
<a class="headerlink" href="#Stub.call+13" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any, h : Any, i : Any, j : Any, k : Any, l : Any, m : Any, n : Any)"></endpoint>
<signature id="Stub.call+14">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`, **n**: `Any`)
<a class="headerlink" href="#Stub.call+14" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any, h : Any, i : Any, j : Any, k : Any, l : Any, m : Any, n : Any, o : Any)"></endpoint>
<signature id="Stub.call+15">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`, **n**: `Any`, **o**: `Any`)
<a class="headerlink" href="#Stub.call+15" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Stub" signature="call(a : Any, b : Any, c : Any, d : Any, e : Any, f : Any, g : Any, h : Any, i : Any, j : Any, k : Any, l : Any, m : Any, n : Any, o : Any, p : Any)"></endpoint>
<signature id="Stub.call+16">Stub.call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`, **n**: `Any`, **o**: `Any`, **p**: `Any`)
<a class="headerlink" href="#Stub.call+16" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### StubMatchers
`:::js import "luxe: test" for StubMatchers`
> no docs found

- [new](#StubMatchers.new)(**value**: `Any`)
- [toHaveBeenCalled](#StubMatchers.toHaveBeenCalled)
- [toHaveBeenCalled](#StubMatchers.toHaveBeenCalled)(**times**: `Any`)
- [toHaveBeenCalledWith](#StubMatchers.toHaveBeenCalledWith)(**args**: `Any`)

<hr/>
<endpoint module="luxe: test" class="StubMatchers" signature="new(value : Any)"></endpoint>
<signature id="StubMatchers.new">StubMatchers.new(**value**: `Any`)
<a class="headerlink" href="#StubMatchers.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js StubMatchers`
> no docs found   

<endpoint module="luxe: test" class="StubMatchers" signature="toHaveBeenCalled"></endpoint>
<signature id="StubMatchers.toHaveBeenCalled">StubMatchers.toHaveBeenCalled
<a class="headerlink" href="#StubMatchers.toHaveBeenCalled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="StubMatchers" signature="toHaveBeenCalled(times : Any)"></endpoint>
<signature id="StubMatchers.toHaveBeenCalled">StubMatchers.toHaveBeenCalled(**times**: `Any`)
<a class="headerlink" href="#StubMatchers.toHaveBeenCalled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="StubMatchers" signature="toHaveBeenCalledWith(args : Any)"></endpoint>
<signature id="StubMatchers.toHaveBeenCalledWith">StubMatchers.toHaveBeenCalledWith(**args**: `Any`)
<a class="headerlink" href="#StubMatchers.toHaveBeenCalledWith" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Suite
`:::js import "luxe: test" for Suite`
> no docs found

- [new](#Suite.new+2)(**name**: `Any`, **block**: `Any`)
- [new](#Suite.new+4)(**name**: `Any`, **beforeEaches**: `Any`, **afterEaches**: `Any`, **block**: `Any`)
- [afterEach](#Suite.afterEach)
- [afterEach](#Suite.afterEach)(**block**: `Any`)
- [beforeEach](#Suite.beforeEach)
- [beforeEach](#Suite.beforeEach)(**block**: `Any`)
- [run](#Suite.run)(**reporter**: `Any`)
- [should](#Suite.should)(**name**: `Any`)
- [should](#Suite.should+2)(**name**: `Any`, **block**: `Any`)
- [skip](#Suite.skip)(**block**: `Any`)
- [suite](#Suite.suite)(**name**: `Any`)
- [suite](#Suite.suite+2)(**name**: `Any`, **block**: `Any`)
- [title](#Suite.title)

<hr/>
<endpoint module="luxe: test" class="Suite" signature="new(name : Any, block : Any)"></endpoint>
<signature id="Suite.new+2">Suite.new(**name**: `Any`, **block**: `Any`)
<a class="headerlink" href="#Suite.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Suite`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="new(name : Any, beforeEaches : Any, afterEaches : Any, block : Any)"></endpoint>
<signature id="Suite.new+4">Suite.new(**name**: `Any`, **beforeEaches**: `Any`, **afterEaches**: `Any`, **block**: `Any`)
<a class="headerlink" href="#Suite.new+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Suite`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="afterEach"></endpoint>
<signature id="Suite.afterEach">Suite.afterEach
<a class="headerlink" href="#Suite.afterEach" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="afterEach(block : Any)"></endpoint>
<signature id="Suite.afterEach">Suite.afterEach(**block**: `Any`)
<a class="headerlink" href="#Suite.afterEach" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="beforeEach"></endpoint>
<signature id="Suite.beforeEach">Suite.beforeEach
<a class="headerlink" href="#Suite.beforeEach" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="beforeEach(block : Any)"></endpoint>
<signature id="Suite.beforeEach">Suite.beforeEach(**block**: `Any`)
<a class="headerlink" href="#Suite.beforeEach" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="run(reporter : Any)"></endpoint>
<signature id="Suite.run">Suite.run(**reporter**: `Any`)
<a class="headerlink" href="#Suite.run" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="should(name : Any)"></endpoint>
<signature id="Suite.should">Suite.should(**name**: `Any`)
<a class="headerlink" href="#Suite.should" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="should(name : Any, block : Any)"></endpoint>
<signature id="Suite.should+2">Suite.should(**name**: `Any`, **block**: `Any`)
<a class="headerlink" href="#Suite.should+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="skip(block : Any)"></endpoint>
<signature id="Suite.skip">Suite.skip(**block**: `Any`)
<a class="headerlink" href="#Suite.skip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="suite(name : Any)"></endpoint>
<signature id="Suite.suite">Suite.suite(**name**: `Any`)
<a class="headerlink" href="#Suite.suite" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="suite(name : Any, block : Any)"></endpoint>
<signature id="Suite.suite+2">Suite.suite(**name**: `Any`, **block**: `Any`)
<a class="headerlink" href="#Suite.suite+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: test" class="Suite" signature="title"></endpoint>
<signature id="Suite.title">Suite.title
<a class="headerlink" href="#Suite.title" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

