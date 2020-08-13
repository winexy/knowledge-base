# Monoid - Моноид

`Monoid` это `Semigroup` с одним отличием. Он так же требует наличие `identity` элемента для типа 

Например для `Integer` identity будет 0

```
x <> 0 == x
0 <> x == x
```

--- 

## Законы 

**Associativity**
- x <> (y <> z) = (x <> y) <> z `(Semigroup)`

**Right identity**
- x <> mempty = x

**Left identity**
- mempty <> x = x


--- 

```hs
GHCi> [1,2,3] ++ []
[1,2,3]

GHCi> [1,2,3] <> []
[1,2,3]

GHCi> [1,2,3] `mappend` mempty 
[1,2,3]
```

В **Haskell** `Monoid` требует реализовать две функции

- `mempty`
- `mappend` 

Реализовав их `mconcat` уже автоматически работает для вас и позволяет комбинировать массив типов