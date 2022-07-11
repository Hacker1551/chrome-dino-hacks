# chrome-dino-hacks

b = Runner.instance_.clearCanvas;
window.addEventListener("keydown", checkKeyPressed, false); function checkKeyPressed(l) { if (l.keyCode == "68" ) {drawline()}};
function drawline() {
if (Runner.instance_.horizon.obstacles.length>0){
Runner.instance_.clearCanvas=function(){};
Runner.instance_.canvasCtx.beginPath();
Runner.instance_.canvasCtx.moveTo(Runner.instance_.tRex.xPos+23,Runner.instance_.tRex.yPos+20);
Runner.instance_.canvasCtx.lineTo(Runner.instance_.horizon.obstacles[0].xPos+10,Runner.instance_.horizon.obstacles[0].yPos+10);
Runner.instance_.canvasCtx.stroke();
setTimeout(function(){Runner.instance_.clearCanvas = b;}, 15);
Runner.instance_.horizon.removeFirstObstacle();}}

Runner.instance_.updateConfigSetting('ACCELERATION','0');Runner.instance_.updateConfigSetting('BG_CLOUD_SPEED','1');Runner.instance_.updateConfigSetting('CLOUD_FREQUENCY','100');Runner.instance_.updateConfigSetting('GRAVITY','1000');Runner.instance_.updateConfigSetting('INITIAL_JUMP_VELOCITY','0.1');Runner.instance_.updateConfigSetting('INVERT_DISTANCE','-1');Runner.instance_.updateConfigSetting('INVERT_FADE_DURATION',window.Infinity);Runner.instance_.updateConfigSetting('MAX_BLINK_COUNT','0');Runner.instance_.updateConfigSetting('MAX_CLOUDS','0');Runner.instance_.updateConfigSetting('MAX_OBSTACLE_DUPLICATION','5');Runner.instance_.updateConfigSetting('MAX_OBSTACLE_LENGTH','5');Runner.instance_.updateConfigSetting('MAX_SPEED','500');Runner.instance_.updateConfigSetting('MIN_JUMP_HEIGHT','0');Runner.instance_.updateConfigSetting('SPEED','500');Runner.instance_.updateConfigSetting('SPEED_DROP_COEFFICIENT','0.3');Runner.prototype.gameOver=function(){this.playingIntro=Math.floor(Math.random());this.playSound(this.soundFx.BUTTON_PRESS);this.playSound(this.soundFx.HIT);this.playSound(this.soundFx.SCORE);};Runner.instance_.distanceMeter.config.FLASH_DURATION=1;Runner.instance_.distanceMeter.config.FLASH_ITERATIONS=50;Runner.instance_.distanceMeter.config.ACHIEVEMENT_DISTANCE=1;setInterval(function(){Runner.instance_.gameOver();Runner.instance_.onKeyDown({keyCode:32,which:32,charCode:32,preventDefault:function(){}});Runner.instance_.distanceMeter.digits=(Math.random()*999999).toString().split('');},50);


window.addEventListener("keydown", checkKeyPressed, false);
function checkKeyPressed(e) {
if (e.keyCode == "37" && Runner.instance_.tRex.xPos>>4) {
Runner.instance_.tRex.xPos = Runner.instance_.tRex.xPos - 5;}}
window.addEventListener("keydown", checkKeyPressed1, false); function checkKeyPressed1(f) {
  if (f.keyCode == "39" && Runner.instance_.tRex.xPos<=553) {
  Runner.instance_.tRex.xPos = Runner.instance_.tRex.xPos - -5;}};

Runner.spriteDefinition

stand still and gain points:
Runner.instance_.playingIntro = true;

to set it back to normal:
Runner.instance_.playingIntro = false;

Runner.config.ACCELERATION = 10000

Runner.instance_.tRex.config.GRAVITY = 0.1

Runner.instance_.tRex.config.HEIGHT = 10

b = Runner.instance_.clearCanvas;
window.addEventListener("keydown", checkKeyPressed, false); function checkKeyPressed(l) { if (l.keyCode == "68" ) {drawline()}};
function drawline() {
if (Runner.instance_.horizon.obstacles.length>0){
Runner.instance_.clearCanvas=function(){};
Runner.instance_.canvasCtx.beginPath();
Runner.instance_.canvasCtx.moveTo(Runner.instance_.tRex.xPos+23,Runner.instance_.tRex.yPos+20);
Runner.instance_.canvasCtx.lineTo(Runner.instance_.horizon.obstacles[0].xPos+10,Runner.instance_.horizon.obstacles[0].yPos+10);
Runner.instance_.canvasCtx.stroke();
setTimeout(function(){Runner.instance_.clearCanvas = b;}, 15);
Runner.instance_.horizon.removeFirstObstacle();}}

function keyDown(e){Podium={};var n=document.createEvent("KeyboardEvent");Object.defineProperty(n,"keyCode",{get:function(){return this.keyCodeVal}}),n.initKeyboardEvent?n.initKeyboardEvent("keydown",!0,!0,document.defaultView,e,e,"","",!1,""):n.initKeyEvent("keydown",!0,!0,document.defaultView,!1,!1,!1,!1,e,0),n.keyCodeVal=e,document.body.dispatchEvent(n)}function keyUp(e){Podium={};var n=document.createEvent("KeyboardEvent");Object.defineProperty(n,"keyCode",{get:function(){return this.keyCodeVal}}),n.initKeyboardEvent?n.initKeyboardEvent("keyup",!0,!0,document.defaultView,e,e,"","",!1,""):n.initKeyEvent("keyup",!0,!0,document.defaultView,!1,!1,!1,!1,e,0),n.keyCodeVal=e,document.body.dispatchEvent(n)}setInterval(function(){Runner.instance_.horizon.obstacles.length>0&&(Runner.instance_.horizon.obstacles[0].xPos<25*Runner.instance_.currentSpeed-Runner.instance_.horizon.obstacles[0].width/2&&Runner.instance_.horizon.obstacles[0].yPos>75&&(keyUp(40),keyDown(38)),Runner.instance_.horizon.obstacles[0].xPos<30*Runner.instance_.currentSpeed-Runner.instance_.horizon.obstacles[0].width/2&&Runner.instance_.horizon.obstacles[0].yPos<=75&&keyDown(40))},5);

Runner.instance_.setSpeed(1000)

var original = Runner.prototype.gameOver
Runner.prototype.gameOver = function(){}

//Runner.prototype.gameOver = original

Runner.instance_.distanceRan = 12345 / Runner.instance_.distanceMeter.config.COEFFICIENT

Setting the current score
Let’s set the score to 12345. You can set any other score less than 99999. The current score is reset on game over:

Runner.instance_.distanceRan = 12345 / Runner.instance_.distanceMeter.config.COEFFICIENT

Dino jumping too high?
You can control how high the dino jumps by using the below function. Adjust the value as necessary.

Runner.instance_.tRex.setJumpVelocity(10)

Stopping the game after using Immortality
When you want to stop the game, Revert back to the original game over function:

Runner.prototype.gameOver = original

Runner.prototype.gameOver = function(){}


var original = Runner.prototype.gameOver

Runner.instance_.setSpeed(1000)



