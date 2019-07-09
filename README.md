# wedding-app
Call
```
./start-weddingapp
```
Then browse to http://localhost:8888 and connect using your your spotify credential.

Then, simply update the file public/playlist/playlist.json to link spotify tracks to the buddies who proposed these tracks ...
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

Hope it could help somebody some day... ;)
