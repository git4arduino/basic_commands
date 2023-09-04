# 6 Branches im lokalen Repository

```
mkdir DHT20_DHT22	
cd DHT20_DHT22
git init
```

```
git add .
git commit -m "Projekt init – temp + hum values on serial monitor"
```

```
git add .
git commit -m "visualize dht22 values on oled"
```

```
git switch -c develop

git switch main

git switch develop
```

```
git switch -c ichwillnichtgelöschtwerden
git switch main
git branch

git branch -d ichwillnichtgelöschtwerden

git branch
```

```
git add .
git commit -m "added DHT20 Sensor"
git switch main
```

```
git switch develop
git stash
git switch develop
git stash pop
```

```
git switch -c newfeature
git add . 
git commit -m "added writeTextAndGrafic Function"
```

```
git switch main
git merge develop
git add .
git commit -m "deleted dht22 content"
git log --oneline
```
