Cheat Sinon.JS & Jasmine BDD
============================

A quick reference for Sinon.JS test spies, stubs and mocks as well as native Jasmine matchers, and those provided by https://github.com/froots/jasmine-sinon. Download the PDF above, or read through the text-only version below.

Yet to provide coverage for Sinon.JS fakes (timers, xhr and servers). Feel free to fork and contribute, or alternatively, let me know if you'd like access to update the www.lucidcharts.com version of the generated PDF.

Sinon.JS & Jasmine BDD Cheat Sheet
================================== 

Spy
---
```
*sinon*
  spy()
  spy(fn)
  spy(obj, 'fn')

*spy*
  callCount
  called
  calledOnce
  calledTwice
  calledThrice
  calledBefore(spy)
  calledAfter(spy)
  calledOn(obj)
  alwaysCalledOn(obj)
  calledWith(*)
  alwaysCalledWith(*)
  calledWithExactly(*)
  alwaysCalledWithExactly(*)
  threw()
  threw('err')
  threw(obj)
  alwaysThrew()
  alwaysThrew('err')
  alwaysThrew(obj)
  returned(obj)
  alwaysReturned(obj)
  thisValues
  args
  exceptions
  returnValues

*spyCall --- getCall(n)*
  calledOn(obj)
  calledWith(*)
  calledWithExactly(*)
  threw()
  threw('err')
  threw(obj)
  thisValue
  args
  exception
  returnValue

* argument list
```
Stub
----
```
*sinon*
  stub()
  stub(obj, "fn")
  stub(obj, "fn", fn
  stub(obj)

*stub*
  withArgs(*)
  returns(obj)
  throws()
  throws('err')
  throws(obj)
  callsArg(index)
  callsArgWith(index, *)
  yields(*)
  yieldsTo(property, *)
```
Mock
----
```
*sinon*
  mock(obj)
  mock()

*mock*
  verify()
  restore()
  
*expectation --- expects('fn')*
  atLeast(n)
  atMost(n)
  never()
  once()
  twice()
  thrice()
  exactly(n)
  withArgs(*)
  withExactArgs(*)
  on(obj)
  verify()
```
Matchers
========

Jasmine Matchers
----------------
```
*expect(x)*
  toEqual(y)
  toBe(y)
  toMatch(pattern)
  toBeDefined()
  toBeNull()
  toBeTruthy()
  toBeFalsy()
  toContain()
  toBeLessThan(y)
  toBeGreaterThan(y)    
  toHaveBeenCalled(y) 	
  toHaveBeenCalledWith(y)


*expect(fn)*
  toThrow(e)

*expect(e).not* - negate criteria
```
Sinon.JS Matchers
-----------------
```
*expect(spy)*
  toHaveBeen
    Called()
    CalledOnce()
    CalledTwice()
    CalledThrice()
    CalledBefore(spy)
    CalledAfter(spy)
    CalledOn(obj)
    AlwaysCalledOn(obj)
    CalledWith(*)
    AlwaysCalledWith(*)
    CalledWithExactly(*)
    AlwaysCalledWithExactly(*)
  toHaveReturned(obj)
  toHaveAlwaysReturned(obj)

*expect(spy).not* - negate criteria
```