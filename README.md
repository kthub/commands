## Commands

### Git
Alias for simplistic-push
```
alias gpush="git add --all; git commit -m ‘commit'; git push origin master"
```

### SSH
Generate keys
```
ssh-keygen -t rsa -b 4096 -C "keiichi.tsuda@gmail.com" -f id_rsa_kt
```
If you unable to ssh, try followings.
```
ssh root@cicd01 -o PreferredAuthentications=password
# .ssh/config を変えてもOK
```
