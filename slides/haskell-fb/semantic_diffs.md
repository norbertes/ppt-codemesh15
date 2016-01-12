###The Road to Running Haskell at Facebook Scale

Semantic diffs


    fxl floor(inf) // -387489237598237489273
    haxl floor(1.0/0.0) // 972391293819283192038901283901289038

    fxl round(0.5) // 0
    haxl round(0.5) // 1

    parseJson "\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\.."

Note:
'One in a million happens all the time'
'One in every billion happens in one hour'


parseJson lib used by them, if you will send 3mbs of slashes allocates 32gb's of memory
