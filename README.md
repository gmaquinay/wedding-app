# wedding-app

Make sure you have nodejs and npm installed. Then, call:
```
npm i
./start-weddingapp
```
And browse to http://localhost:8888 and connect using your your spotify credential.

To make magic happen, simply update the file public/playlist/playlist.json to link spotify tracks to the buddies who proposed these tracks ...
This is a stupid UI made for a wedding where we asked all guests to propose 10 tracks they really like.

playlist.json looks like:
```
{
  "people" : {
    "1" : {"nickname":"La Mariééée!",    "image":"elo.jpg"},
    "2" : {"nickname":"Guigui",          "image":"guigui.png"},
    "21": {"nickname":"Sijj Fano",       "image":"fano.jpg"}
    "24": {"nickname":"Jean Claude Dus", "image":"jcdus.jpg"}
  },
  "tracks" : {
    "spotify:track:46PIncJ42Zirjj01wSru2y"          : {"proposedBy":["1"]"},
    "spotify:track:2SbsvihBJmgNKZ4qkXFWrp"          : {"proposedBy":["2","1"]},
    ...
    "spotify:local:Sadistic+Intent:Ancient+Black+Earth:Ancient+Black+Earth:310" : {"proposedBy":["21"],"artwork":"sadistic_intent.jpg"},
    ...
    "spotify:track:4znl02ZqeJ6gKd0DfvBXf7" : {"proposedBy":["24"]}
  }
}

```

Last but not the least, if you want to make it default app on a rapsberry pi,
install the following packages,
```
sudo apt install ttf-mscorefonts-installer unclutter x11-xserver-utils
```
and add the following lines to the file .config/lxsession/LXDE-pi/autostart
```
@/home/pi/wedding-app/start-wedding-browser
@xset s off
@xset s noblank
@xset -dpms
```


Hope it could help somebody some day... ;)
