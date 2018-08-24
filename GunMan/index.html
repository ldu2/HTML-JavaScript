<!DOCTYPE html>
<html>
    <meta charset="utf-8"> 
	<head>
		<title>Duluku</title>
		<link rel="stylesheet" href="main.css">
	</head>
	<body onload="startGame()">
		<header>
			<nav>
				<h1>Duluku</h1>
				<ul>
					<li><a href="index.html">Main</a></li>
					<li><a href="me.html">About</a></li>
					<li><a href="data.html">Data</a></li>
					<li></li>
				</ul>
			</nav>
		</header>
        <div class="row">
            <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
            <style>
            canvas {
                border:1px solid #d3d3d3;
                background-color: #f1f1f1;
            }
            </style>
            <script>
            
            var myGamePiece;
            var myObstacles = [];
            var myScore;
            var myImages=['never',"player_bot","player_left","player_top","player_right"]
            function startGame() {
            	window.addEventListener('keydown', accelerate);
            	window.addEventListener('keyup', decelerate);
                myGamePiece = new sprite(35, 23,10, 120);
                myScore = new component("30px", "Consolas", "black", 280, 40, "text");
                myGameArea.start();
            }
            
            var myGameArea = {
                canvas : document.createElement("canvas"),
                start : function() {
                    this.canvas.width = 860;
                    this.canvas.height = 483;
                    this.context = this.canvas.getContext("2d");
                    document.body.insertBefore(this.canvas, document.body.childNodes[0]);
                    this.frameNo = 0;
                    this.interval = setInterval(updateGameArea, 20);
                    },
                clear : function() {
                    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
                }
            }
            function sprite(width, height, x, y) {
                this.width = width;
                this.height = height;
                this.speedX = 0;
                this.speedY = 0;    
                this.x = x;
                this.y = y;
            	this.dir=4;
                this.update = function() {
            		var img=document.getElementById(myImages[this.dir]);
                    ctx = myGameArea.context;
                    ctx.drawImage(img,this.x, this.y);
            		
                }
                this.newPos = function() {
                    this.x += this.speedX;
                    this.y += this.speedY;
                    this.hitBottom();
            		for (i = 0; i < myObstacles.length; i += 1) {
            			this.crashWith(myObstacles[i]);
            		}
                }
                this.hitBottom = function() {
                    var rockbottom = myGameArea.canvas.height - this.height;
            		var rockRight = myGameArea.canvas.width - this.width;
                    if (this.y > rockbottom) {
                        this.y = rockbottom;
                    }
            		if(this.y<0){
            			this.y=0;
            		}
            		if(this.x<0){
            			this.x=0;
            		}
            		if(this.x>rockRight){
            			this.x=rockRight;
            		}
                }
            	
                this.crashWith = function(otherobj) {
            	//need to figure out where exactly is the place
            		var right=this.x+this.width;
            		var bottom=this.y+this.height;
                    var otherright = otherobj.x + otherobj.width;
                    var otherbottom = otherobj.y + otherobj.height;
            		if(this.y < otherbottom && bottom > otherbottom){
            			if (right > otherright && this.x < otherobj.x ){
            				this.y= otherbottom;
            			}
            		}
            		if(bottom > otherobj.y &&this.y<otherobj.y){
            			if( right > otherright && this.x < otherobj.x){
            				this.y = otherobj.y-this.height;
            			}
            		}
            		if(right> otherobj.x && this.x<otherobj.x){
            			if(this.y>otherobj.y && bottom < otherbottom){
            				this.x = otherobj.x-this.width;
            			}
            		}
            		if(this.x < otherright&&right>otherright){
            			if( this.y>otherobj.y && bottom < otherbottom){
            				this.x = otherright;
            			}
            		}
                }
            }
            function component(width, height, color, x, y, type) {
                this.type = type;
                this.score = 0;
                this.width = width;
                this.height = height;
                this.speedX = 0;
                this.speedY = 0;    
                this.x = x;
                this.y = y;
                this.update = function() {
                    ctx = myGameArea.context;
                    if (this.type == "text") {
                        ctx.font = this.width + " " + this.height;
                        ctx.fillStyle = color;
                        ctx.fillText(this.text, this.x, this.y);
                    } 	
            		else {
                        ctx.fillStyle = color;
                        ctx.fillRect(this.x, this.y, this.width, this.height);
                    }
                }
                this.newPos = function() {
                    this.x += this.speedX;
                    this.y += this.speedY;
                    this.hitBottom();
                }
                this.hitBottom = function() {
                    var rockbottom = myGameArea.canvas.height - this.height;
                    if (this.y > rockbottom) {
                        this.y = rockbottom;
                        this.gravitySpeed = 0;
                    }
                }
            }
            
            function updateGameArea() {
                var x, height, gap, minHeight, maxHeight, minGap, maxGap;
            
            	myGameArea.clear();
                myGameArea.frameNo += 1;
                if (myGameArea.frameNo == 1 || everyinterval(150)) {
                    x = myGameArea.canvas.width;
                    minHeight = 20;
                    maxHeight = 200;
                    height = Math.floor(Math.random()*(maxHeight-minHeight+1)+minHeight);
                    minGap = 50;
                    maxGap = 200;
                    gap = Math.floor(Math.random()*(maxGap-minGap+1)+minGap);
                    myObstacles.push(new component(10, height, "green", x, 80));
                }
                for (i = 0; i < myObstacles.length; i += 1) {
            		if(myGameArea.frameNo<300){
            		 myObstacles[i].x += -1;
            		 }
                    myObstacles[i].update();
                }
                myScore.text="SCORE: 100";
                myScore.update();
                myGamePiece.newPos();
                myGamePiece.update();
            }
            
            function everyinterval(n) {
                if ((myGameArea.frameNo / n) % 1 == 0) {return true;}
                return false;
            }
            
            function accelerate(event) {
            	var key=event.keyCode;
            	if(key==87){
            		myGamePiece.speedY = -5;
            		myGamePiece.dir=3;
            	}
            	if(key==83){
            		myGamePiece.speedY = 5;
            		myGamePiece.dir=1;
            	}
            	if(key==65){
            		myGamePiece.speedX = -5;
            		myGamePiece.dir=2;
            	}
            	if(key==68){
            		myGamePiece.speedX = 5;
            		myGamePiece.dir=4;
            	}
            }
            function decelerate(event) {
            	var key=event.keyCode;
            	if(key==87 || key==83){
            		myGamePiece.speedY = 0;
            	}
            	if(key==65 || key==68){
            		myGamePiece.speedX = 0;
            	}
            }
            </script>
            <br>
            <img src="HAND_GUN_MAN_WALK_RIGHT.bmp" id="player_right">
            <img src="HAND_GUN_MAN_WALK_LEFT.bmp" id="player_left">
            <img src="HAND_GUN_MAN_WALK_TOP.bmp" id="player_top">
            <img src="HAND_GUN_MAN_WALK_BOT.bmp" id="player_bot">
        </div>
		<footer class="foot">Copyright 2016 Duluku</footer>
	</body>
</html>
