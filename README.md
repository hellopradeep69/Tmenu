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
#### Requirement
- fzf
- tmux [no s#it herlock]
- curl
----------
#### Installation
----------
- before installing stuff from internet its a good practice to read it before you run it .

```bash
curl -o ~/.local/bin/tmenu.sh https://raw.githubusercontent.com/hellopradeep69/Tmenu/main/tmenu.sh

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
#### How to add your own template

```bash
nvim ~/.local/bin/tmenu.sh

```

1. search for template like /template
- example template

```bash
    temp)
        tmux new-session -d -s "$session_name" -n "nvim" # create a window name nvim 
        tmux new-window -t "$session_name" -n "xtra" # create second window name xtra
        tmux split-window -h -t "$session_name:2" -c "#{pane_current_path}" # create split window
        tmux resize-pane -t "$session_name:2.0" -Z # resize pane ig
        tmux new-window -t "$session_name" -n "btop" # third window namely btop
        tmux select-window -t "$session_name:1" # focus session 1 
        tmux new-window -t "$session_name" -n "config" -c ~/.config/ # -c open tmux server in .config dir 
        ;;
```

2. template menu
- search for /template menu 

```bash
printf "temp\nproject\ndev\nweb\ndefault" | fzf \
```

- add your temp in above format
----------


