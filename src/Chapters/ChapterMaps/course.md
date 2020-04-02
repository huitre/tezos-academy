# Chapter 10 : Maps

Maps associates values of the same type with other values of the same type.

## Declaration

Maps are declared as

```
type balances is map (address, int)
```

## Instanciation

To create an non-empty map :

```
const user_balances : balances =
    map [
        ("tz1KqTpEZ7Yob7QbPE4Hy4Wo8fHG8LhKxZSx" : address) -> (5n);
        ("tz1gjaF81ZRRvdzjobyfVNsAeSC6PScjfQwN" : address) -> (0n)
    ]
```

ℹ️ If you want to declare an empty map, just leave the array empty [].

## Access

Use the postfix [] operator to read a value of the map :

```
const my_balance : option (int) =
  user_balances [("tz1gjaF81ZRRvdzjobyfVNsAeSC6PScjfQwN" : address)]
```

## Your mission

<!-- prettier-ignore -->
1- Create the mapping *name\_to\_ship* which associates ship names to their ship record.