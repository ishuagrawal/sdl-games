# SDL Games Site

Check out my collection of video games I developed using C++ and the SDL library. The games were ported to the web using Emscripten.

Link: https://ishuagrawal.github.io/sdl-games/  

## Games:

### **Mario Kart**:
This game implements the original SNES Rainbow Road track from the original *Super Mario Kart*.
- The player can drive the kart with ```W```, ```A```, and ```D```, with a spring camera working appropriately.
- The kart’s height is correctly interpolated based on the height map.
- The enemy drives around the track at a reasonable speed without driving in circles, getting stuck, or driving noticeably outside the bounds of the track.
- Checkpoints, lap tracking, and place tracking work correctly. Game start timer works as specified, and game displays whether you win or lose at the end.

### **Star Fox Tunnel**:
This game implements a 3D “endless flying” gameplay using art assets inspired by Star Fox.
- The ship moves using WASD, and the follow camera follows appropriately.
- Obstacles 1 to 20 load and are randomly selected after the first in-order iteration.
- Ships can fire bullets on the leading edge of the spacebar, bullets hitting a block destroys the bullet, and bullets hitting an exploding block triggers the explosion and chain explosions. Bullets also despawn after 1 second if they hit nothing.
- The player starts with 3 shield levels, the player colliding with an obstacle reduces their shield level by 1, hitting 0 shield pauses the player, and the HUD properly shows the current shield level.
- You can do a barrel roll as described by pressing Q, it will regenerate 1 shield level (up to the max of 3), and Peppy will periodically remind you to do a barrel roll.
- The game speeds up over time.

### **Zelda**:
This game implements a small portion of 1991’s *A Link to the Past* for the Super Nintendo (SNES).
- The tiles for the map are loaded appropriately.
- Link can walk with the arrow keys. Multiple arrow key presses has Link in one of the pressed directions. The correct walking animation plays based on the direction, and the correct standing animation plays when not moving. The camera centers on and follows Link around as he walks.
- The soldier travels in a path, computed based on the A* search algorithm.
- Link cannot walk through enemies and can deal damage to them. Soldiers die in two hits (while being stunned after one hit) and the bushes in one.

### **Parkour's Edge**:
This game is a first-person parkour game, inspired by 2008's *Mirror's Edge*.
- The player correctly moves with ```WASD```. Mouse left/right movement rotates the player on the yaw axis, and up/down movement of the mouse pitches the camera (with the maximum up/down pitch clamped).
- The player can jump (on the leading edge of the spacebar), fall (at the apex of their jump), and collide with blocks.
- The player can wall climb (when running roughly towards a wall).
- The player can wall run (when running roughly perpendicular to the wall), with the camera rolling appropriately.
- The player can collect coins.
- Laser trip mines emit lasers from their bases, and stop drawing when they hit a block or the player.
- Mirrors reflect lasers off blocks appropriately.
- Security cameras work appropriately as their cone color correctly changes between white/yellow/red. The cameras also rotate appropriately, and their sound volume changes based on distance to the player.
- The player can collect checkpoints and respawns at the position of their last checkpoint when falling off the world, being hitting by a laser, or getting caught by a security camera. The checkpoint arrow points towards the next active checkpoint.
- The player advances to the next level when touching the final checkpoint of a level.
- The player's HUD is updated accordingly to maintain a timer and count the number of collected checkpoints and coins.
- The security camera blip's position on the radar mirrors the position of the security camera relative to the player and rotates based on the player rotating direction. The blips themselves also update their rotation based on the rotation of the security cameras in the world.

### **Pac-Man**
This game mostly recreates Pacman with an implementation of the Ghost AI.
- At the start of the game, all four ghosts move towards their respective corners and will circle around the node.
- When Pacman eats a power pellet, ghosts reverse their direction of travel for 7 seconds.
- If the ghost is killed, it will path back to the pen and become alive again.
- The animations update properly, based on the state and the direction the ghost is facing.

### **Mario**
This game recreates the first level of *Super Mario Bros.* (World 1-1), albeit with not all the different gameplay features/mechanics of the actual game.
- Mario can run and jump through the level and collides with the blocks and pipes.
- Camera advances as Mario runs through the level. The camera should not go backwards, and Mario should not be able to run off camera.
- Goombas should fall when not standing on anything, and when they hit a wall or another Goomba, they switch directions.
- Mario can stomp on Goombas, and Mario dies if he runs into a Goomba and isn’t stomping it.
- The animations for Mario (idle, run, jump, dead) and the Goomba (walk, dead) play as appropriate.
- The main music plays and loops. The sound effects for jump, stomp, and bump play as expected. When Mario dies (either killed by a Goomba or falls in a pit), the main music stops, and the death music plays. When Mario reaches the end of the level, the main music stops, and the victory music plays.

### **Frogger**
This game is based on the classic arcade game *Frogger*.
- The frog hops on the leading edge of the various arrow keys and can’t hop off screen.
- The Frog-Vehicle intersection works as expected, and when the frog dies it shows a DeadFrog and moves the frog back to the start position,
- Vehicles slow down if the frog is within an angle in front of the vehicle.
- Frog can ride logs and dies if it jumps into the water.
- Frog is paused when it reaches the goal.

### **Asteroids**
This game is based on Atari's version of *Asteroids* with updated graphics.
- Ship appears and moves on screen using the arrow keys.
- Asteroids initialize with random positions and rotations, move on screen, and wrap around when they go off screen.
- Pressing spacebar fires lasers, but you can’t shoot more than one a second, and lasers will disappear after one second if they hit nothing.
- Lasers can collide with asteroids and in the event of a collision both are destroyed.

### **Pong**
This game is a single-player version of Pong.
- The up and down keys move the paddle and you can’t move the paddle off screen.
- The ball bounces off the wall and paddle as expected.


