#What's miniKanren?

### veneer - Browser based miniKanren editor \w REPL
http://tca.github.io/veneer/editor.html

Note:
###
First program:
  (== 5 5)
  Answer: Yes

  (== 5 6)
  Answer: No
  
###
Variables doesn't have to be defined
  (== X 5) ?

###
Find two vars
(== (list x)  y) 
    Answer: Yes, 0 (0)
    
###
conde - every condition, najpierw pokaże wynik dla 1, 
następnie 'wyczyści program' i pokaże wynik dla 2 części 
(conde
       ((== 5 x))
       ((== 6 x)))

###
W rachunku lambda każde wyrażenie określa funkcję jednoargumentową. 
Z kolei argumentem tej funkcji jest również funkcja jednoargumentowa, 
wartością funkcji jest znów funkcja jednoargumentowa

(define fn
  (lambda (term)
      (fresh (x t)
        (== `(lambda (,x) ,t) term)))  

)

(fn `(lambda (z) z))

define - tworzy funkcję
fresh - definiuje/czyści wartość zmiennej
` - tworzy listę z wyrażenia (interpolacja)
, - oznacza, że wartość zostanie dynamicznie wypełniona

###
Rachunek lambda jest przydatny do badania algorytmów. 
Wszystkie algorytmy, które dadzą się zapisać w rachunku lambda, dadzą się zaimplementować na maszynie Turinga i odwrotnie.

Istnieje wiele rodzajów rachunku lambda, z czego najprostszym jest rachunek lambda bez typów, 
stanowiący pierwotną inspirację dla powstania programowania funkcyjnego (Lisp). 

Rachunek lambda z typami jest podstawą dzisiejszych systemów typów w językach programowania.


; x <- var
; (lambda (x) y) <- abstraction
; (f g) <- application

(define lc-fn
  (lambda (term)
      (conde 
        ((symbolo term))
        ((fresh (x t)
          (== `(lambda (,x) ,t) term)))
        ((fresh (e1 e2)
          (== `(,e1 ,e2) term))))
      )

)

(lc-fn term)


symbolo - constraint check czy term jest symbolem (scheme)
application - wywołanie funkcji na argumencie z danej domeny i otrzymanie wartości z jej przedziału
