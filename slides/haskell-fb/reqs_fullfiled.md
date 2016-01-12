###The Road to Running Haskell at Facebook Scale

Reqs:
- Latency sensitive (Haxl)
- Complex expressive application logic (Haxl)
- Ship new code ASAP (GHC)
- 1M reqs/sec

Note:
GHC (glasgow haskell compiler) runtime has built-in linker
You can run new code without restarting a server 
(why? think of how many people are using simultainusely fb, and you close their connection,
also remember they're shipping X times per day)
