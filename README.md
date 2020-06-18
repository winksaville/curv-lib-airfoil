# lib-airfoil

**********************************************
A library to manipulate airfoil sections.

An airfoil section is defined by the type:
  airfoil = [[x: float, y: float], ...]

Assumptions concerning airfoil:
  First index is trailing edge and each
  subsequent point is the next point in
  the counter clockwise direction.
**********************************************


```
teIdx af = 0;
    /// Return index of the trailing edge point.

tePt af = af[teIdx(af)];
    /// Return [x,y] of trailing edge

teX af = tePt(af)[X];
    /// Return X coordiante of trailing edge

teY af = tePt(af)[Y];
    /// Return Y coordiante of trailing edge

leIdx af
    /// Return index of the leading edge point

lePt af = af[leIdx(af)];
    /// Return [x,y] of leading edge

leX af = lePt(af)[X];
    /// Return X coordiante of leading edge

leY af = lePt(af)[Y];
    /// Return Y coordiante of leading edge

normalize af
    /// Return the normalized airfoil, which I
    /// define as a airfoil section with a chord of 1.0

fattenTe {
      naf        /// Normalized af [[x,y], ...] with af[0] == trailing edge
    , tt=1       /// Trailing edge Thickness
    , chord=10   /// Chord length
  }
    /// Fatten Trailing Edge. Not yet implemented just
    /// returns naf.
```

TODO: write a program which extracts documentation from lib-airfoil
and places it here. For now I'll just copy paste and delete the code.
