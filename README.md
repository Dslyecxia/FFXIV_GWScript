# Steps
* Log in to: http://guildwork.com/games/ffxiv#/gilgamesh/shouts
* Press *F12*
* Enter in console: 
```
(function(){
var jq = document.createElement('script'); jq.src = "https://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js"; 
var prepNotifications = function() {
  $('head').append('<audio id="wav" src="http://dslyecxia.com/Application/gw/apert.wav" preload="auto"></audio>'); $('.shouts-inner').bind("DOMSubtreeModified",function(data){String.prototype.contains = function(it) {return this.indexOf(it) != -1; }; s = $('.shout:last-child')[0]; s = $(s).text(); s = s.toLowerCase(); if(s.contains("lfg")){document.getElementById("wav").play(); return true; } if(s.contains("invite")){document.getElementById("wav").play(); return true; } if(s.contains("hunt")){document.getElementById("wav").play(); return true; } });
}
document.getElementsByTagName('body')[0].appendChild(jq);
var jqint = setInterval(function(){
  try{
    prepNotifications();
    clearInterval(jqint);
  } catch(e) { /* Not Yet Loaded */ }
}, 1000);
})();
```
