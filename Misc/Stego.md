## Brute Force
In some instances, you may find you have a stego image, but have no way of identifying the password. It may be a case of brute forcing them with the below tools.

### Stegseek
For a fast brute force solution you can run stegseek
[https://github.com/RickdeJager/stegseek](https://github.com/RickdeJager/stegseek)

**Usage:**
```
stegseek <FILE> <WORDLIST>
```

### Stegcracker
If you have a stego image but need to brute force the password you can use Stegcracker. (Stegcracker will call steghide to decrypt the file) 

[https://github.com/Paradoxis/StegCracker](https://github.com/Paradoxis/StegCracker)

**Usage:**
```
stegcracker <FILE> <WORDLIST>
```

