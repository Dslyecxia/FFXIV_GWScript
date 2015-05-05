# Steps
* Log in to: http://guildwork.com/games/ffxiv#/gilgamesh/shouts
* Press *F12*
* Enter in console: 
```javascript
(function(){
var shouldNotify = function(msg) {
  var notifyOn = [
    'lfg',
    'hunt',
    'invite'
  ];
  var ignore = [
    'fate'
  ];
  var matches = function(str){ return msg.indexOf(str) !== -1};
  // Notify if at least 1 keyword is found, yet none of the blacklisted ones are present
  return notifyOn.some(matches) && !ignore.every(matches);
};
var throttle = function(fn, timeout) {
  var throttleTimer;
  return function(){
    if(!throttleTimer) {
      fn();
      throttleTimer = setTimeout(function(){
        throttleTimer = undefined;
      }, timeout);
    }
  }
};
var prepNotifications = function() {
  var notifier = document.createElement('audio');
  notifier.preload = true;
  notifier.src = "http://dslyecxia.com/Application/gw/apert.wav";
  document.querySelector('.shouts-inner').addEventListener('DOMSubtreeModified', throttle(function(data){
    var msg = document.querySelector('.shouts:last-child').innerText;
    if(shouldNotify(msg)) notifier.play();
  }, 2500));
}
prepNotifications();
})();
```
