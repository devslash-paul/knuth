1: 10 --> 
The text showed how to interchange the values of m and n, using the replacement notation, by setting t <- m, m <- n, n <- t. Show how the values
of four variables (a,b,c,d) can be rearranged to (b,c,d,a) by a sequence of replacements. In other words, the new value of a is to be the original
value of b, etc. Try use the minimum number of replacements.

t <- a
a <- b
b <- c
c <- d
d <- a

2: -----------

3: [20] -->  
Change algorithm E (for sake of efficiency) so that all trivial replacement operands such as "m <- n" are avoided. White
this new algorithm in the style of Algorithm E, and call it Algorithm F.

Algorithm E
-----------

1. [Find remainder] Divide m by n and let r be the remainder (0 <= r < n)
2. [Is it zero] If r = 0, the algorithm terminates; n is the answer
3. [Reduce] Set m <- n, n <- r, and go back to E1.

Algorithm F

1. [Find remainder] Divide m by n, let m be the remainder
2. [Is it zero] If m = 0, the algorithm terminates; n is the answer
3. [Find the remainder] Divide n by m, let n be the remainder
4. [Is it zero] if n = 0. the algorithm terminates; m is the answer. Else, go to 1
