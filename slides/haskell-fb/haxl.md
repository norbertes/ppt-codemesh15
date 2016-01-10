###The Road to Running Haskell at Facebook Scale

Reqs:
- Latency sensitive
- Complex expressive application logic
- Ship new code ASAP
- 1M reqs/sec

Note:
Haskell can handle it, but what about missing DSL?

Haxl is a Haskell library that simplifies access to remote data, 
such as databases or web-based services. Haxl can automatically
- batch multiple requests to the same data source,
- request data from multiple data sources concurrently,
- cache previous requests.


