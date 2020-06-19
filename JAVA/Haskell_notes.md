# Definitions

## Curried Functions
Functions that take their arguments one at a time are called **curried functions**.Curried functions are more **flexible** than functions on tuples, because useful functions can often be made by partially applying a curried function. 

## Polymorpgic Functions
A function is called **polymorphic** ("of many forms") if its type contains one or more type variables. <br>
```length :: [a] -> Int ```

## Overloaded Functions 
A polymorphic function is called **overloaded** if its type contains one or more class constraints. <br/>
```
Num - Numeric types
Eq - Equality types
Ord - Ordered types 
eg.
(+) :: Num a => a -> a -> a
(==) :: Eq a => a -> a -> Bool
(<) :: Ord a => a -> a -> Bool 
```
## Conditional Expressions 
```
signum :: Int → Int
signum n = if n < 0 then -1 else
 if n == 0 then 0 else 1 
 ```
 
## Guarded Equations 
```
signum n | n < 0 = -1
 | n == 0 = 0
 | otherwise = 1 
 ```
## Pattern Matching
```
(&&) :: Bool -> Bool -> Bool
True && True = True
_    && _    = False 
```
## Lists Comprehensions 
### Dependant Generators 
```
[x^2 | x <- [1..5]] 

[(x,y) | x <- [1,2,3], y <- [4,5]]
[(1,4),(1,5),(2,4),(2,5),(3,4),(3,5)]
```
### Guards
```
factors :: Int → [Int]
factors n =
 [x | x ← [1..n], n `mod` x == 0] 
 ```

 