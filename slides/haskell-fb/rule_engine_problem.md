###The Road to Running Haskell at Facebook Scale

Rule Engine to prevent spambots and fake accounts. 
1. Guy posting about Monads
2. More than 100 friends
3. More than half of friends like C++
4. Block, else allow

Note:
It's very slow and takes lots of requests.

Pure functions + Data fetching: are goal for performance, but Data fetching @ 
real time is impossible
