###The Road to Running Haskell at Facebook Scale

Reqs:
- Latency sensitive
- Complex expressive application logic
- Ship new code ASAP
- 100K reqs/sec

Note:
- batch all requests
- no concurency
- dynamic loader
- fast enough

They wrote their own language FXL, which was doin all the stuff, but 
scale was the problem. They had to go into Milion requests per sec.

They were stuck by hardware and language constructs. 

So they had to drop totaly their language. They askd them 
