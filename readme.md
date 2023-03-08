# How I setup my Arch Linux on my laptop with an external display

## How I set correct resolution and linked my laptop to external display

### Step 1

Install arandr via pacman
Sudo pacman -S arandr

### Step 2
Open arandr, then put your primary laptop display over your external moniter
Now press save on the furthermost right button below the menubar options
Name your '.sh' file and click save. 
Copy the xrandr command inside the '.sh' file you saved
Paste it into your ~/.xinitrc and replace it with other prexisting xrandr commands

## A solution to external moniter turning off after laptop lid is closed

### Step 1

nvim into /etc/systemd/logind.conf
add this line to the file "HandleLidSwitch=ignore"
Then reload to apply the changes "systemctl restart systemd-logind"

Tip: If frozen, Make sure to hold powerbutton until you see the screen change

(AUDIO)
## How to solve PulseAudio Problems with HDMI

This was fairly easy to do
Install "pavucontrol" via pacman
Do "sudo pacman -S pavucontrol"
then you're good to go.


