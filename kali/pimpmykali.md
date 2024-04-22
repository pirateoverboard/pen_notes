
`cd opt`
`sudo git clone https://github.com/Dewalt-arch/pimpmykali.git `

`sudo ln -s primpmykali/<app> <app>`

pull-request for flame shot

$getrealuser ?

`/home/kali/.config/xfce4/xfconf/xfce-perchannel-xml`

`sed -rnE 's|^(\s+<property\s+name="Print"\s+type="string")\s+value="/usr/share/kali-themes/xfce4-screenshooter"/>|\1 value="/usr/bin/flameshot gui"/>|ip' xfce4-keyboard-shortcuts.xml`

`mkdir -p "$logname/.config/autostart"
`cat > ~/.config/autostart/flameshot.desktop << EOF
[Desktop Entry]
Type=Application
Exec=/usr/bin/flameshot
Hidden=false
NoDisplay=false
Name=flameshot
Comment=Run flameshot during login
Terminal=false
StartupNotify=false
EOF`

`auto_start_dir`

`[ -d $auto_start_dir ] || mkdir -p $auto_start_dir`
```
[ ! -f $auto_start_dir/fameshot.desktop ]; then
	cat > $auto_start_dir/flameshot.desktop << EOF
	```