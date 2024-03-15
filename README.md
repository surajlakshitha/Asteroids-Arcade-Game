<p>Figure 1. gives the layout of the regions of space (a rectangular grid shape), the Spaceship is
represented by the blue triangle, its starting position is its home base (1, 1).</p>
<p>The aim is to move the Spaceship from its home base through space using the various movement
operations to get to the Starbase (6,4), avoiding the Asteroids.</p>
![Figure1](https://github.com/surajlakshitha/Asteroids-Arcade-Game/assets/78702149/cf156c64-d60e-45db-a28e-0ec69fcd9780)
<p>Notes</p>
• Space is made up of regions (squares of the grid) 12 wide by 7 high.<br>
• The regions of space are populated by 11 asteroids, each in one region of space, and
located as shown in Figure 1.<br>
• The Spaceship occupies only one square at a time which must be either an "empty space
square" or the Starbase in its square (6,4).<br>
For example, the Spaceship can be in region (5, 3), but not (8, 3) as it is occupied by an
asteroid.<br>
• The Spaceship is initially in its homebase, i.e. the bottom left square (1, 1).<br>
• The spaceship can make a normal move, i.e. from one region of space (grid square) to an
adjacent one, in one of four directions: Up, Down, Left and Right.<br>
• It uses up 5 units of power when it makes a normal move.<br>
• The spaceship can engage its warp-drive to “jump” to any region of space, except one
occupied by an asteroid. It must not travel outside known space, i.e. outside the grid.<br>
• It uses up 20 units of power when it engages its warp-drive, no matter how far it moves.<br>
• If the spaceship crashes into one of the asteroids it loses 10 units of power and bounces
back into the square it came from.<br>
• It cannot do a move for which it does not have the required amount of power.<br>
• The state of the game is one of the following:<br>
• the spaceship docks at the Starbase, in which case the game has been Won.<br>
• the spaceship is not docked at the Starbase & can not move because it has run out
of power, in which case the game is Lost.<br>
• otherwise the game is not over.<br>

<p>2 Develop a B Specification of the Regions of Space, Spaceship & Asteroids</p>
<p>Your B specification, i.e. collection of one or more B machines, should include the following elements.</p>
<p>2.1 Sets and Constants</p>
Any sets and constants that are required to define the data and state of the spaceship, space,
asteroids and their properties.<br>
(Hints: Represent space and the asteroids as relations. What is the relationship between space,
"empty space" & the asteroids locations?)<br>
<p>2.2 System State</p>
The state variables required to represent space, asteroids and the spaceship. Including the state
invariant and initialisation.
You can assume that the spaceship starts at its homebase, has no power yet, has not had any
collisions and it has only visited the regions of space its homebase is located in.
<p>2.3 New Game</p>
To start or re-start the game use the NewGame( power ) operation. This should reset the spaceship
to the initial state, except that it sets its power level to the value of the power parameter.
2.4 Spaceship Movements in Space
Note that all movement operations must report the outcome of an attempted movement. That is,
either it was successful, failed due to space boundary issues, failed due to an asteroid, or failed for
some other reason.
<p>2.4.1 Normal Spaceship Movements</p>
<p>The following operations are the basic movements that all move the spaceship one region (square) in
the appropriate direction in space and uses up 5 units of the spaceship's power:</p>
• MoveUp
• MoveDown
• MoveLeft
• MoveRight
<p>Note that If the
 move results in the spaceship hitting an asteroid the spaceship remains in its current
location, but its power is reduced by 10 units.</p>
<p>If any attempted movement cannot be performed because of the boundary of space or insufficient
power then an error is reported.</p>
<p>2.4.2 Warp-drive Spaceship Movement</p>
<p>The movement operation:</p>
<p>• WarpDrive( newposition )
where the player enters the newposition parameter, the region of space (i.e. grid co-ordinates) that
the spaceship should warp jump to. Engaging the warp-drive uses up 20 units of the spaceship's
power.</p>
<p>If the warp-drive cannot be used because the destination region input is either not within the known
regions of space or is occupied by an asteroid or if there is insufficient power to use the warp-drive
then an appropriate error message should be reported.</p>
<p>2.5 Spaceship's Mission Status</p>
<p>An enquiry operation MissionStatus that reports the current status of the spaceship:</p>
<p>• the game status (WON, LOST, or NOT_OVER),</p>
<p>• its current location,</p>
<p>• its current power reserves,</p>
<p>• how many asteroid collisions it has had.</p>
<p>2.6 Spaceship's Mission Route</p>
<p>An enquiry operation RegionsVisited that reports the regions of space that the spaceship has
travelled through.</p>
<p>2.8 General Requirements</p>
<p>The B specification should use the appropriate features to define the data and operations in your B
machine.</p>
<p>The specification must be syntactically and type correct, as checked by using the Atelier B tool.
The specification must be animated by ProB. That is it must initialise correctly and all operations can
be animated successfully and used to move the Spaceship around the regions of space, e.g. from the
homebase to the Starbase using a combination of all of the movement operations, including the warp
jump. </p>
