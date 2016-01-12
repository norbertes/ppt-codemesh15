###The Road to Running Haskell at Facebook Scale

What about servers?
- Written in C++
- Don't want to rewrite them, because they're fine
- Foreign Function Interface

> foreign import ccall unsafe "SomeFn"


Note:
C++ dont like it, they had seg_faults inside seg_faults

unsafe very performant, but doesnt care about packaging runtime
safe is opposite.

