# Steps
* Log in to: http://guildwork.com/games/ffxiv#/gilgamesh/shouts
* Press *F12*
* Enter in console: 
```
var jq = document.createElement('script'); jq.src = "https://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js"; document.getElementsByTagName('head')[0].appendChild(jq);
```
* Wait 2 seconds
* Enter in console: 
```
$('head').append('<audio id="wav" src="http://dslyecxia.com/Application/gw/apert.wav" preload="auto"></audio>'); $('.shouts-inner').bind("DOMSubtreeModified",function(data){String.prototype.contains = function(it) {return this.indexOf(it) != -1; }; s = $('.shout:last-child')[0]; s = $(s).text(); s = s.toLowerCase(); if(s.contains("lfg")){document.getElementById("wav").play(); return true; } if(s.contains("invite")){document.getElementById("wav").play(); return true; } if(s.contains("hunt")){document.getElementById("wav").play(); return true; } });
```
