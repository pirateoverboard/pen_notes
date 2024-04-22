
`cd /opt`

`sudo git clone https://github.com/PlumHound/PlumHound.git

`cd PlumHound

`sudo pip3 install -r requirements.txt

note: make sure bloodhound and neoj4 are running first because it pulls data from it.

test if the domain works
`sudo python3 PlumHound.py --easy -p <neoj4_password>

then:
`sudo python3 PlumHound.py -x tasks/default.tasks -p <neoj4_password>`

`ls`

`firefox index.html`