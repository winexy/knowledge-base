# Semigroup - Полугруппа

`Seimgroup` - нужен для того чтобы комбинировать значения одного типа

```hs
instance Semigroup Integer where
  (<>) x y = x + y`
```

> Сигнатура 

```hs
(<>) :: Semigroup a => a -> a -> a
```

---

## Законы 
**Associativity**
- x <> (y <> z) = (x <> y) <> z