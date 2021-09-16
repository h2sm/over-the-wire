# over-the-wire

Level 0:
1) ssh bandit0@bandit.labs.overthewire.org -p 2220 
2) bandit0

Level 0 -> Level 1:
1) ls 
2) cat readme (password is boJ9jbbUNNfktd78OOpsqOltutMc3MY1)

Level 1 -> Level 2:
1) ssh bandit1@bandit.labs.overthewire.org -p 2220
2) cd ~
3) ls 
4) cat ./- (password is CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9)

Level 2 -> Level 3:
1) ssh bandit2@bandit.labs.overthewire.org -p 2220 
2) ls
3) cat spaces\ in\ this\ filename (password is UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK)

Level 3 -> Level 4:
1) ssh bandit3@bandit.labs.overthewire.org -p 2220
2) cd inhere/
3) ls
4) cat .hidden (password is pIwrPrtPN36QITSp3EQaw936yaFoFgAB)

Level 4 -> Level 5:
1) ssh bandit4@bandit.labs.overthewire.org -p 2220
2) cd inhere/
3) find . -type f -exec file {} + | grep ASCII (password is koReBOKuIDDepwhWk7jZC0RTdopnAYKh)

Level 5 -> Level 6:
1) ssh bandit5@bandit.labs.overthewire.org -p 2220
2) find . -size 1033c -type f -exec file {} + | grep ASCII (output is "./maybehere07/.file2: ASCII text, with very long lines")
3) cat ./maybehere07/.file2 (password is DXjZPULLxYr17uwoI01bNLQbtFemEgo7)

Level 6 - > Level 7:
1) ssh bandit6@bandit.labs.overthewire.org -p 2220
2) cd /
3) find . -size 33c -user bandit7 -group bandit6 (file is here : /var/lib/dpkg/info/bandit7.password)
4) cat /var/lib/dpkg/info/bandit7.password (password is HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs)


Level 7 -> Level 8:
1) ssh bandit7@bandit.labs.overthewire.org -p 2220
2) cat data.txt | grep millionth (password is cvX2JJa4CFALtqS87jk27qwqGhBM9plV)

Level 8 -> Level 9:
1) ssh bandit8@bandit.labs.overthewire.org -p 2220
2) cat data.txt | sort | uniq -u (password is UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR)

Level 9 -> Level 10:
1) ssh bandit9@bandit.labs.overthewire.org -p 2220
2) strings data.txt | grep -E "==" (password is truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk)

Level 10 -> Level 11:
1) ssh bandit10@bandit.labs.overthewire.org -p 2220 
2) base64 --decode data.txt (password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR)

Level 11 -> Level 12:
1) ssh bandit11@bandit.labs.overthewire.org -p 2220
2) 