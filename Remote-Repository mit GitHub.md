# 7 Remote-Repository mit GitHub

```
ssh-keyen
cd ~/.ssh
ls
cat id_rsa.pub
```

```
ssh -T git@github.com
```

```
https://github.com/T-vK/ESP32-BLE-Keyboard

git clone git@github.com:T-vK/ESP32-BLE-Keyboard.git
```

#### Create a Repo on GitHub with Files

```
git clone git@github.com:git4arduino/iamnotpublic.git
git pull
echo "add platformio files" >> todo.md

git add .
git commit -m "todo added"
git push
```

#### Push a local Repo to GitHub

Create a Repo without a readme and licence file

```
mkdir pushlocal
cd pushlocal
echo "A great project is in the making" >> README.md
git remote add origin git@github.com:git4arduino/pushlocal.git

git push --all
```
