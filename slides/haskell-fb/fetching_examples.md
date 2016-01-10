###The Road to Running Haskell at Facebook Scale

Data Fetching problems:

    // find common friends
    intersect(friendsOf(x), friendsOf(y))
    
    // classic n+1 problem
    map(accountAge, friendOf(x))
    
    // ... combo
    map(accountAge, intersect(friendsOf(x), friendsOf(y)))
    
Note:
problem: they don't run concurently
problem: they want easy syntax which describe what's going on - expressive code
