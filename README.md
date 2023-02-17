# Solutions for OverTheWire bandit ctf:
to log into a certain problem
```console
┌──(intedai㉿kali)-[~]
└─$ ssh bandit[problem number]@bandit.labs.overthewire.org -p 2220
```

after every problem type `exit -d` to logout 
## Bandit Level 0 → Level 1

password is bandit0

```console
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```

## Bandit Level 1 → Level 2

password is NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

```console
bandit1@bandit:~$ cat <-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

## Bandit Level 2 → Level 3

password is rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

```console
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```

## Bandit Level 3 → Level 4

password is aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

```console
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```

## Bandit Level 4 → Level 5

password is 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

```console
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```

-file07 is the only file with ASCII text therefore it's the readable file

```console
bandit4@bandit:~/inhere$ cat <-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

## Bandit Level 5 → Level 6

password is lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

```console
bandit5@bandit:~$ find . -readable -size 1033c ! -executable
./inhere/maybehere07/.file2
bandit5@bandit:~$ cat ./inhere/maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

## Bandit Level 6 → Level 7

password is P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

```console
bandit6@bandit:~$ bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c -perm /u+r,g+r,o+r 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```

## Bandit Level 7 → Level 8

password is z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

```console
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```

## Bandit Level 8 → Level 9

password is TESKZC0XvTetK0S9xNwm25STk5iWrBvP

```console
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```

## Bandit Level 9 → Level 10

password is EN632PlfYiZbn3PhVK3XOGSlNInNE00t

```console
bandit9@bandit:~$ strings data.txt | grep ==
```

I used 2 = instead of 1 because the question says several '=' so we can eliminate lines with 1 '='

```console
c========== the
h;========== password
========== isT
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

## Bandit Level 10 → Level 11

password is G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

```console
bandit10@bandit:~$ base64 -d data.txt
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```

## Bandit Level 11 → Level 12

password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

```console
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```

## Bandit Level 12 → Level 13

password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

```console

```
