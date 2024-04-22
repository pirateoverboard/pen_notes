
change display settings in gui

edit /etc/lightdm/lightdm.conf

look for line 
\[Seat:*\]
`display-setup-script=xrandr -s 1920x1080`

`sudo sed -i  's/^\[Seat:\*\]/\[Seat:\*\]\ndisplay-setup-script=xrandr -s 1920x1080/' /etc/lightdm/lightdm.conf
`
`sudo xrandr | head -n1 | grep -Po '(?<=\scurrent\s)[0-9]{3,4}\sx\s[0-9]{3,4}' | tr -d " "`

`get_current_screen_size=$(xrandr | head -n1 | grep -Po '(?<=\scurrent\s)[0-9]{3,4}\sx\s[0-9]{3,4}' | tr -d " ")