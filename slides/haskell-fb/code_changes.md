###The Road to Running Haskell at Facebook Scale

    // 'naive'
    friendsOf :: Id -> [Id]
    // Haxl
    friendsOf :: Id -> Haxl [Id]
    
    // 'naive'
    map friendsOf [id1, id2, ..]
    // Haxl
    mapM friendsOf [id1, id2, ..]
    
