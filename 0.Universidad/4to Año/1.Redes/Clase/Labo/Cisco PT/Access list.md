```
access-list [0;200] permit [protocol] [ip add origin] [joker] [ip add destination]
```

[joker] -> for a particular host = 0.0.0.0   ;   for a net = opposite to the mask
[0;99] -> Simple -> No ip add destination (only origin)

Has to be configurated on both routers (with opposite ip origin/destination)