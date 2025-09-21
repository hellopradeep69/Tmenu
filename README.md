## Tmenu.sh
----------
###  What is tmenu.sh ?
----------
1. tmux menu with bunch of stuff and a buildin alike tmux-sessionizer (alike) by primeagen .
2. what can it do ?
- a lot of beautiful stuff .
- it create a tmux server with predefined template. 
- delete an unwanted tmux server that been living in your system for like months.
- tmux-sessionizer buildin alike twin that works just fine.
3. it uses fzf :-0.
4. thats it for now
----------
#### Installation
----------
- before installing stuff from internet its a good practice to read it before you run it .

```bash
git clone https://github.com/hellopradeep69/Tmenu.git ~/.local/bin/

```
- give permisson to the file .
```bash
chmod +x ~/.local/bin/tmenu.sh
```
----------
#### keybind (shortcuts)
- add in your .tmux.conf
```.tmux.conf
bind-key f run-shell "tmux neww -n 'Tmenu' ~/.local/bin/tmenu.sh"
```
- prefix + f opens the tmenu so you dont have to type it every time you want to open it
- prefix default it ctrl + b. [weird]
----------

