## Munching Squares for Emacs

The original PDP-1 munching squares formula is:

```
lat         /Load test word.
add v       /Add from V.
dac v       /Deposit back to V.
rcl 9s      /Rotate combined AC-IO 9 bits to the left
xor v       /Exclusive-or the contents of V.
dpy-i 300   /Plot point at x = high ten bits of AC, y = high ten bits of IO.
```

The prevailing defininition from HACKMEM item 147 is:

*"Munching squares is just views of the graph Y = X XOR T for
consecutive values of T = time."*

I have adopted the latter.  But rather than drawing a complete NxN
square for successive T, I compute a list of coordinates to update.

```
                                            [][][][][][][][][][]
                                            [][][][][][][][][][]
                                        [][]    [][][][][][][][]
                                        [][]    [][][][][][][][]
                                    [][]        [][][][][][][][]
                                    [][]        [][][][][][][][]
                                [][]            [][][][][][][][]
                                [][]            [][][][][][][][]
                                [][][][][][][][]            [][]
                                [][][][][][][][]            [][]
                                [][][][][][][][]        [][]    
                                [][][][][][][][]        [][]    
                                [][][][][][][][]    [][]        
                                [][][][][][][][]    [][]        
                                [][][][][][][][][][]            
                                [][][][][][][][][][]            
            [][][][][][][][][][]                                
            [][][][][][][][][][]                                
        [][]    [][][][][][][][]                                
        [][][]  [][][][][][][][]                                
  [][][]        [][][][][][][][]                                
[]  [][]        [][][][][][][][]                                
[][]  []        [][][][][][][][]                                
[][][]          [][][][][][][][]                                
[][][][][][][][]          [][][]                                
[][][][][][][][]        []  [][]                                
[][][][][][][][]        [][]  []                                
[][][][][][][][]        [][][]                                  
[][][][][][][][]  [][][]                                        
[][][][][][][][][]  [][]                                        
[][][][][][][][][][]  []                                        
[][][][][][][][][][][]                                          
```
