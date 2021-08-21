# Enumeration

We find a suid binary called try-harder

analysing this in ghidra we can see that it is xoring the data.

Because we know the value of two of these, we can reverse it 

`local_14 = local_1c ^ 0x1116 ^ local_18;`

local_18= 23987

1573743953 ^ 4374 ^ 23987 