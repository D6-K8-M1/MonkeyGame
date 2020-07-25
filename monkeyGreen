
var monkey=createSprite(40,370,10,10);
 monkey.setAnimation("monkey");
 monkey.scale = 0.1;
var ground=createSprite(800,380,1600,10);
ground.velocityX=-4;

var bananaGroup=createGroup();
var obstacleGroup=createGroup();

// var stone=createSprite(50,370,10,10);
// var banana=createSprite(148,288,10,10);



var count=0;
console.log("AAAAAAAAA");

function draw(){
  background("#BEE2B3");
  console.log("111");
  
  ground.shapeColor="#000000";
  
  text("Score: "+count,300,80);
  
  if(keyDown("space")){
    monkey.velocityY=-10;
  }
  console.log("22");
   monkey.velocityY=monkey.velocityY+0.8;
   
   if(ground.x<0) {
     ground.x = 800;
   }
   
   monkey.collide(ground);
   spawnBananas();
   spawnRocks();
   
   if(bananaGroup.isTouching(monkey)) {
     count = count + 1;
     bananaGroup.destroyEach();
   }
   
   if(obstacleGroup.isTouching(monkey)){
     count=0;
     //monkey.destroy();
     rock.velocityX=0;
     banana.velocityX=0;
     ground.velocityX=0;
   }
  drawSprites();
 
 
}

function spawnBananas() {
  if(World.frameCount % 80 === 0) {
    var banana = createSprite(400,250,10,10);
    banana.setAnimation("Banana");
    banana.scale = 0.1;
    banana.velocityX = -4;
    banana.lifetime = 100;
    bananaGroup.add(banana);
  }
}

function spawnRocks() {
  if(World.frameCount % 60 === 0) {
    var rock = createSprite(400,362,10,10);
    rock.setAnimation("Stone");
    rock.scale = 0.1;
    rock.velocityX = -10;
    rock.lifetime = 100;
    obstacleGroup.add(rock);
  }
}
