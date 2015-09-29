## What is this?
Small modifications of [givf-player.js](https://github.com/globocom/gifv-player) so that [gifv](http://imgur.com/blog/2014/10/09/introducing-gifv/) videos aren't played by _onclick_ and _mouseenter_ events.

## Small modifications?
Removed the following event listeners:
```javascript
bindEvents: function () {
var player = this;
/*
$(document).on('click.gifv', this.selector, function (event) {
event.preventDefault();

var $player = $(this);
player.playPause($player);

return true;
});

if (this.options.autostart) {
$(document).on('mouseenter.gifv', this.selector, function (event) {
event.preventDefault();

var $player = $(this);
player.play($player);
});
}*/
```
##Demo
The demo simply showcases how two buttons can be used to play and pause the gifv.
```javascript
$("#play").click(function() {
    $('.gifv-player').find('video').show();
    $('.gifv-player').find('video')[0].play();
});
$("#pause").click(function() {
    $('.gifv-player').find('video')[0].pause();
});
```
For in depth details on how gifv-player works, consult the [project's repo](https://github.com/globocom/gifv-player) so that [gifv](http://imgur.com/blog/2014/10/09/introducing-gifv/) 

