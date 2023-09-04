# 9 Kurze Praxisbeispiele aus dem Entwicklungsalltag

## 9\.1 createdata.sh

```
#!/bin/bash

RANDOM_NUMBER=$(( ( RANDOM % 100 ) + 1 ))
RANDOM_CPP="main$RANDOM_NUMBER.cpp"

# Datei mit inhalt füllen, da sie ansonsten nicht commited werden
echo "Hier steht bald ganz wichtiger Code von der Datei $RANDOM_CPP" > $RANDOM_CPP

git add .
git commit -m "$RANDOM_CPP hinzugefügt"
git log --oneline --graph
```

```
chmod +x createData.sh
./createData.sh
```

## 9\.2 

```
const char* ssid     = "lost";
const char* password = "4#8#15#16#23#42“;
```

```
#include "credentials.h"

nano .gitignore
.pio
.vscode/.browse.c_cpp.db*
.vscode/c_cpp_properties.json
.vscode/launch.json
.vscode/ipch
credentials.h
```

```
git add .
git commit -m „no credentials.h should be pushed“	
git push
```

```
git ls-files
```

## 9\.3 

```
git add -f credentials.h
git commit -m „added credentials.h template“
git push
```

## 9\.4

```
git add .
git rm -r .vscode
```

## 9\.5

```
git init
git add .
git commit -m „project init“

git ls-files
```

```
git switch -c LibraryTest

#include "DFRobot_DHT20.h"

git restore .
```

```
git clean -nfd

git clean -nxf
```

```
git clean -fd

git ls-files
```

## 9\.6

```
git commit -am "my fancy commit message"
```

## 9\.7

```
git status
```

## 9\.8

```
git diff HEAD~2 src/main.cpp
git diff 9a7f42bb116ed474659273936b3f56d0cf454e34 src/main.cpp
```

```
git restore -s HEAD~2 src/main.cpp
```

## 9\.9

```
git show HEAD~:src/main.cpp

git show HEAD~:src/main.cpp > oldmain.cpp

git show HEAD~ src/main.cpp 
```

## 9\.10

```
git log
git commit –amend
git log --oneline

git push --force
```

## 9\.11

```
git clone git@github.com:git4arduino/dht20_dht22.git
git log --oneline
```

```
git revert HEAD
git log
ls
```

## 9\.12

```
git clone git@github.com:git4arduino/dht20_dht22.git
git log –oneline

git switch -c feature
git log --online
```

```
git switch main
git switch -c mergetest
git log --online
```

```
git merge feature
git log --online
```

```
git switch main
git cherry-pick 4fa3130

git log
```

## 9\.13

```
git switch -c feature
git add .
git commit -m „changed seconds in loop blink without delay“
```

```
git switch main
git switch -c merge1
git merge feature
```

```
git log --merge
git diff
```

```
git add .
git commit -m "changed seconds from 2 to 5"
```

```
git merge feature
```

```
git add .
git commit -m "solved merge conflict in loop – keep 5 seconds"
git reset --merge 
```
