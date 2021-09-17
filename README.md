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
2) cat data.txt | tr '[a-z]' '[n-za-m]' | tr '[A-Z]' '[N-ZA-M]' (password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu)

Level 12 -> Level 13:
1) ssh bandit12@bandit.labs.overthewire.org -p 2220
2) mkdir /tmp/pass
3) cp data.txt /tmp/pass
4) file data1 (data1: gzip compressed data, was "data2.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix)
5) mv data1 data1.gz
6) ls (data1.gz  data.txt)
7) gunzip data1.gz 
8) ls (data1  data.txt)
9) file data1 (data1: bzip2 compressed data, block size = 900k)
10) bzip2 -d data1 (bzip2: Can't guess original name for data1 -- using data1.out)
11) ls (data1.out  data.txt)
12) file data1.out (data1.out: gzip compressed data, was "data4.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix)
13) mv data1.out data1.gz
14) ls (data1.gz  data.txt)
15) gunzip data1.gz
16) ls (data1  data.txt)
17) file data1 (data1: POSIX tar archive (GNU))
18) tar xvf data1
19) ls (data1  data5.bin  data.txt)
20) file data5.bin (data5.bin: POSIX tar archive (GNU))
21) tar xvf data5.bin (data6.bin)
22) file data6.bin (data6.bin: bzip2 compressed data, block size = 900k)
23) bzip2 -d data6.bin (bzip2: Can't guess original name for data6.bin -- using data6.bin.out)
24) ls (data1  data5.bin  data6.bin.out  data.txt)
25) file data6.bin.out (data6.bin.out: POSIX tar archive (GNU))
26) tar xvf data6.bin.out
27) ls (data1  data5.bin  data6.bin.out  data8.bin  data.txt)
28) file data8.bin (data8.bin: gzip compressed data, was "data9.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix)
29) mv data8.bin data8.gz
30) gunzip data8.gz
31) ls (data1  data5.bin  data6.bin.out  data8  data.txt)
32) file data8 (data8: ASCII text)
33) cat data8 (The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL)

Level 13 -> Level 14:
1) ssh bandit13@bandit.labs.overthewire.org -p 2220
2) ssh bandit14@localhost -i sshkey.private
3) cd /etc/bandit_pass
4) cat bandit14 (4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e)

Level 14 -> Level 15:
1) nc localhost 30000
2) 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e (Correct! BfMYroe26WYalil77FoDi9qh59eK5xNr)

Level 15 -> Level 16:
1) ssh bandit15@bandit.labs.overthewire.org -p 2220
2) openssl s_client -connect localhost:30001 -ign_eof 
3) BfMYroe26WYalil77FoDi9qh59eK5xNr (Correct! cluFn7wTiGryunymYOu4RcffSxQluehd)

Level 16 -> Level 17:
1) ssh bandit16@bandit.labs.overthewire.org -p 2220
2) mkdir /tmp/myfiles
3) cmd /tmp/myfiles
4) nmap -31000-32000 localhost | awk '/open/{print $1+0}' > ports.txt (31046 31518 31691 31790 31960)
5) for i in $(cat ports.txt); do print $i | echo "cluFn7wTiGryunymYOu4RcffSxQluehd" | timeout 1 openssl s_client -connect localhost:$i -quiet; done
6) cat /etc/bandit_pass/bandit16 | openssl s_client -connect localhost:31790 -quiet > ssh22.private
7) Удаляем "Correct!" из ssh22.private
8) chmod 400 ssh22.private
9) ssh -i ssh22.private bandit17@localhost

Level 17 -> Level 18:
1) 