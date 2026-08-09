# Super AI SuperTrack 2026 game rules
### CONTENT

**Section 1. Game Introduction**....................................................................................3
**Section 2. Robot Requirements**................................................................................4

**2.1. Construction Materials**.........................................................................................4
**2.2. Requirements for Designing Robots**.............................................................4
**Section 3. Competition Field**.....................................................................................6

**3.1 Field Map**....................................................................................................................6
**3.2 Field Specifications**................................................................................................6
**Section 4. Robot Mission Description**..................................................................7

**4.1. Robot Missions**.......................................................................................................7
Task 1: Start Cruise.........................................................................................................8
Task 2: Flight Path Survey............................................................................................8
Task 3: Interstellar Vortex.............................................................................................9
Task 4: Beacon Delivery................................................................................................9
Task 5: Gravity Launch..................................................................................................11
Task 6: Starship Docking..............................................................................................12
Task 7: Energy Refill.......................................................................................................13
Task 8: Safe Return........................................................................................................13
Task 9: Star Map Decoding (Additional Task)......................................................13

**4.2 Task Randomization**.............................................................................................15
**4.3 Time Limit**.................................................................................................................15
**4.4 Off-Track Rule**..........................................................................................................15
**Section 5. Competition Format**................................................................................16

**5.1 Competition Order**..................................................................................................16
**5.2 Programming & Debugging**...............................................................................16
**5.3 Pre-Match Preparation**..........................................................................................17
**5.4 Start Procedure**.........................................................................................................17
**5.5 Time Bonus**.................................................................................................................17
**5.6 Reset**...............................................................................................................................18
**5.7 End of Match**...............................................................................................................19
**5.8 Final Score**....................................................................................................................19
**5.9 Ranking**..........................................................................................................................19
**5.10 Violations**.....................................................................................................................20
Appendix 1............................................................................................................................21
**Score Sheet** – **Star Cruise**................................................................................................21

# Section 1. Game Introduction

Stars shimmer along both sides of the **Milky Way–Andromeda Interstellar Route**, a vital corridor for humanity’s deep-space exploration. To ensure the continuous and safe operation of this route, robots are deployed to conduct routine cruise missions—identifying obstacles, deploying signal beacons, and activating navigation facilities.

This competition simulates such a cruise scenario. Participants are required to build and program their own robots on-site, complete debugging, and execute designated tasks.

With **Star Cruise** as its theme, contestants will guide their robots through a simulated interstellar passage to accomplish key missions. The event aims to promote knowledge of deep-space navigation and aerospace safety while developing participants’ logical thinking, responsiveness, hands-on coordination, and team spirit.

The competition is divided into the **Elementary, Junior, and Senior Groups**. Each team consists of **one contestant and one coach**, and all contestants must be enrolled students as of **July 2026**.

# Section 2. Robot Requirements

## 2.1. Construction Materials

Contestants must design and build their own robots to complete the assigned tasks; however, on-site assembly is not required. Robots are limited to electronic components with plastic housings and plastic interlocking building parts. 3D-printed components are not permitted, and robots must not damage the competition field or any task models at any time.

Among the materials brought by contestants, **only motors, battery boxes, sensors,** **remote controllers, and cameras** may include components joined by screws or solder. All other parts must not be assembled using screws, soldering, glue, double-sided tape, or any other auxiliary materials.

By registering for the competition, participants acknowledge that the Organizing Committee reserves the final right to interpret this rulebook.

## 2.2. Requirements for Designing Robots

|Item|Requirements|
|---|---|
|Quantity|Each team can use only one robot.|
|Dimensions|The robot must fit within 25 cm × 25 cm × 25 cm (Length × Width × Height) while inside the Start Zone. After leaving the Start Zone, mechanical structures may extend, but the robot must never exceed 35 cm × 35 cm × 35 cm (Length × Width × Height) at any time.|
|Controller|Each robot may use only one controller. All input/output ports (including motor control ports) must use RJ11 connectors. The controller must include a built-in color LCD|

||touchscreen of at lea(A8C inches.|
|---|---|
|Sensors|The types and quantities of sensors used on the robot are not restricted.|
|Motors|The total number of motors (including servos) shall not exceed 6, and a single motor can only drive a single grounded wheel. The motors shall not be modified or over-pressurized. (For fairness, the motors used to drive the grounded wheels are limited to 3582, 3581, 3579, 3570, 9522, and 9523 models.)|
|Drive Wheels|The diameter of the robot's wheels (including tires) used for landing shall not exceed 70mm, and the width shall not exceed 25mm.|
|Structure|The robot must be built using plastic building parts with a 10 mm design standard. You may not use 3D-printed components, screws, bolts, rivets, glue, adhesive tape, or any other auxiliary fastening materials. Rubber bands may be used only as auxiliary elastic components.|
|Battery|The robot’s input-rated voltage must not exceed 8.4 V. Each robot must be equipped with an independent power supply and not be connected to any external power source.|
|Inspection|Before the first competition round, robots may be fully assembled while entering the venue, but must pass a comprehensive inspection to ensure full compliance with all regulations. Contestants must correct any non-compliant parts before being allowed to participate in the match.|

# Section 3. Competition Field

## 3.1 Field Map

The final layout of the robot competition field shall be subject to the version announced on-site.

**Figure:** Example of the competition field with all task elements arranged.

## 3.2 Field Specifications

1. The maximum size of the robot competition field is **3000 mm (L) × 2000 mm**
**(W)**.
2. An irregular flight route is distributed across the field. It consists mainly of a 25 mm (±1 mm) wide tracking line, which provides directional guidance for the robot. The exact shape and layout of the flight route shall follow the field presented on-site.

3. Two **planet zones**, labeled **A** and **B**, are placed in the field for installing beacon placement models. Each planet zone is a circular area with a diameter between **300 mm and 400 mm**. At the center of each planet zone is the **beacon placement point**, enclosed by a **regular octagonal fence** approximately **70 mm high** and **170 mm in diameter**.
4. The field includes a **Start Zone** and an **End Zone**, each measuring **250 mm × 250** **mm**, clearly marked “Start” and “End.” At the beginning of the match, the robot departs from the Start Zone, follows the flight route, and ultimately reaches the End Zone on the opposite side.
# Section 4. Robot Mission Description

Irregular tracking lines are distributed across the field. Within the **180-second time** **limit**, the robot must operate **fully autonomously**, departing from the Start Zone in the designated direction, moving forward **without leaving the flight route**, reaching each task area as quickly as possible to complete the assigned missions, and finally arriving at the End Zone. Task models follow the diagrams provided in the task description. However, the actual models used in competition may differ slightly—for example, variations in the color of beams/pins or minor differences in size or height. Contestants must be able to adjust their solutions based on the actual field conditions.

## 4.1. Robot Missions

l **Basic Tasks:** Start Cruise, Flight Path Survey, Interstellar Vortex, Beacon Delivery, Gravity Launch, Safe Return. l **Random Tasks:** Starship Docking, Energy Refill. l **Additional Task:** Star Map Decoding.

The Basic Task areas are arranged in designated zones according to the detailed task specifications.

- **Elementary Group:** No Random Tasks.
- **Junior Group:** Required to complete **one** Random Task (drawn on-site).
- **Senior Group:** Required to complete **all** Random Tasks.
Additional Tasks may be set at the competition field. If used, they will be announced **before the debugging period** and placed in the corresponding area according to the task requirements.

### Task 1: Start Cruise

**a)** The robot leaves the Start Zone.
**b)** When the robot’s vertical projection completely exits the Start Zone during the initial phase (recorded once per match), the team earns 60 points.
### Task 2: Flight Path Survey

**a)** Along the flight route, several marker lines are placed perpendicular to the route, dividing it into multiple route segments. Each segment is labeled with letters such as A, B, C, and so on.
**b)** Throughout the mission, the robot must move **forward along the direction of the** **flight route**.
- Except for short departures required **solely to complete a task**, or when reversing (the robot must return to the point where it left the route and continue forward afterward),
- Both **drive wheels** must remain **on both sides** of the flight path or **directly on** **top** of the flight path at all times.
**c)** Each time any **drive wheel** touches a marker line of the flight route, the team earns **6 points**, up to a maximum of **60 points**.

|a) b) c) wheels|the model’s final position. supported by a the platform. grounded side team scores|Task 3: Interstellar Vortex and 60 points|50 mm.|One Interstellar Vortex model is placed at a The Interstellar Vortex model consists of a field surface, while the other end is suspended. The robot must climb onto the platform from the|The task is considered completed when the robot maintaining contact with the platform surface|the programming and debugging period begins, the referee will draw lots to determine and push down to make the suspended end touch the field surface, and then drive off exits from the previously suspended side,|bracket on both sides. One end of the platform touches the|random location ground-contact side|on the field. Before platform (400 mm × 300 mm × 30 mm), move forward, enters the platform from the with both drive throughout the process. The|
|---|---|---|---|---|---|---|---|---|---|
|a) For the For the|Placement Points.|Task 4: Beacon Delivery Elementary Group||Figure: Junior Group and Senior Group|Two planet zones are set in the field for placing Beacon Placement Points. place a Beacon Placement Point before programming and debugging.|status of the Interstellar Vortex model, the referee will draw, both|one||of the two planet zones to planet zones will be used as Beacon|

**b)** Before programming and debugging begin, the referee will randomly select a Delivery Point located 300 mm to 600 mm from the center of a planet zone along the flight path. Once confirmed, a Delivery Point Marker (diameter: 50 mm) will be pasted at that position. The **Elementary Group** will have **one Delivery Point**. The **Junior Group** and **Senior Group** will have **two Delivery Points.** A beacon model will be placed at the Delivery Point located closer to the planet zone. The beacon model is a plastic regular dodecahedron with a diameter no greater than 50 mm.
**c)** The robot must carry one beacon model from the Start Zone to a Delivery Point and deliver it into the Beacon Placement Point. The **Junior Group** and **Senior Group** must then proceed to the next Delivery Point to obtain another beacon model and deliver it to the second Beacon Placement Point.
**d)** If the vertical projection of the beacon model **touches the planet zone**, the task is considered completed and earns **20 points each** (the **Elementary** Group must complete 1 beacon; **Junior Group** and **Senior Group** must complete 2). If the beacon model is **fully placed within** the Beacon Placement Point, **an** **additional 40 points** will be awarded for each beacon.
**e)** Throughout the delivery process, the robot must keep the vertical projection of its main body fully covering the Delivery Point Marker; otherwise, the delivery is invalid. Main body refers to the robot’s core frame when stationary in the Start Zone, excluding any arms or extensions deployed after leaving the Start Zone.
**Figure:** Delivery Point with Marker Applied, and Beacon Placed on the Delivery

Point

**Figure:** Two Completed States of the Beacon Delivery Task

### Task 5: Gravity Launch

**a)** The task model consists of **a starship, a launcher, and a control hub**. The control hub must always face the adjacent track line.
**b)** The Gravity Launch model is fixed in Task Zone A1.
**c)** The robot must carry the **key** (a robot Info-Tag Module), depart, and use it to touch the control hub, triggering the hub to activate the launcher and send the starship model into the air.
**d)** When the **“Super AI”** indicator on the control hub lights up, the robot earns **60** **points**.

#### Figure: Task Zone A1

**Figure:** Initial and Completed States of the Gravity Launch Model

### Task 6: Starship Docking

**a)** The task model consists of a starship, a cabin module, and a control lever. The cabin module initially stands perpendicular to the starship, and the two components do not touch.
**b)** The robot must lift the control lever to rotate the cabin module until it becomes parallel to the starship, completing the docking process.
**c)** When the tail of the starship remains in contact with the front end of the cabin module, the task is considered completed and earns 60 points.

**Figure:** Initial, Intermediate, and Completed States of the Starship Docking Model

### Task 7: Energy Refill

**a)** The task model consists of a starship, an energy block, and a refill box.
**b)** The robot shall lift the refill box upward, allowing the energy blocks inside to enter the starship.
**c)** When the energy block is completely inside the starship, the task is completed, and 60 points are scored.
**Figure:** Initial and Completed States of the Energy Refill Model

### Task 8: Safe Return

**a)** The robot shall enter the End Zone along the forward-moving direction indicated by the alphabetical order of the marker lines, without leaving the Flight Path.
**b)** When the vertical projection of any drive wheel is fully within the End Zone, the task is completed, and 60 points are scored.
### Task 9: Star Map Decoding (Additional Task)

**a)** The Star Map Decoding model is fixed in Task Zone A2 adjacent to the End Zone. Robots may start this task only after completing the “Safe Return” task. This task is

not timed, and its completion does not affect the Time Bonus. The additional task cannot be reset.

**b)** The task model consists of a **Star Map Display** (featuring four types of star maps, with actual designs subject to the on-site presentation), **four physical constellations** (each corresponding to one star map shown on the display), and an **operation panel.**
**c)** The robot must push the **operation panel** to rotate the Star Map Display for at least one full turn. Once the display stops, the robot must use its vision module to identify the star map pattern facing the robot, then **knock down** the physical constellation that exactly matches the displayed star map (changing from vertical to inclined). Knocking down extra or incorrect constellations will not earn points.
**d)** If the operation panel makes contact with the base plate, the team scores **10 points**. If the robot successfully identifies the star map and knocks down the corresponding constellation, an additional **50 points** will be awarded.

|||Figure: Initial, Intermediate, and Completed States of the Star Map Decoding Model||
|---|---|---|---|
||4.2 Task Randomization|||
|Except for|Gravity Launch||, which is fixed in Task Zone A1, and the additional task|
|Star Map Decoding||, which is fixed in Task Zone A2, the locations of the task models||
|for Interstellar Vortex|,|Beacon Delivery, Starship Docking|, and Energy Refill are|
|not fixed||. Before programming and debugging begin, the referee will determine the||
|position and orientation|requirements of the corresponding tasks. identical for all rounds within the same division|of each task model by drawing lots, according to the Once the position and orientation are confirmed, the task model layout will.|remain|
|4.3 Time Limit||||
|Each round has a|180-second 4.4 Off-Track Rule During movement, the robot may from the track line, it must be The robot may momentarily leave the track line tasks other than Beacon Delivery|time limit. its drive wheels must remain on both sides of the track line or directly on top of it, passing over every track line encountered along the path). If the robot manually reset.. Still, it must return to the|not leave the flight path’s guiding track line (i.e., fully deviates only when required to complete point of departure|
|from the track line and||resume movement from that position|.|

# Section 5. Competition Format

## 5.1 Competition Order

The competition adopts a points-based system. Participating teams will draw lots on-site to determine their groupings and competition order. Teams will enter the field one by one according to the order determined by the draw.

The Organizing Committee ensures that all teams in the same division receive equal competition opportunities, usually at least two rounds. When the current team begins its match, the next team will be notified to prepare in the waiting area. Any team that fails to arrive within the designated time will be deemed to have forfeited its qualification for that match.

## 5.2 Programming & Debugging

Before the first round begins, all teams will have at least 60 minutes for robot debugging. The exact debugging time for each round will be determined and announced by the referee team based on on-site conditions.

Participants must queue in an orderly manner for programming and debugging in accordance with venue rules. Teams that fail to follow on-site rules may be disqualified. After debugging is complete, all teams must place their robots in the designated storage area under the referee’s custody. Participants may not touch their robots again without permission; otherwise, the team will be disqualified.

If the referee signals the start of a match and a team is still unprepared, the team will lose its opportunity for that round, but its qualification for subsequent rounds will not be affected.

## 5.3 Pre-Match Preparation

When preparing to enter the field, team members shall retrieve their robot and enter the competition area under the guidance of the referee or staff. Teams that fail to arrive within the designated time will be considered to have forfeited.

Contestants must stand near the Start Zone. After entering, contestants shall place their robot inside the Start Zone; no part of the robot, including its vertical projection on the ground, may extend beyond the Start Zone boundary.

## 5.4 Start Procedure

After confirming that the team is ready, the referee will announce the countdown: “3, 2, 1, Start.” Once the countdown begins, team members may bring their hand slowly toward the robot. As soon as the contestant heard the word “Start,” the team member could press a physical button on the controller to activate the robot. Starting the robot before the “Start” command will be regarded as a **false start** and may result in a warning or penalty. Once activated, team members must not touch the robot (except when performing a reset).

After activation, the robot must not intentionally detach components or leave mechanical parts on the field. Any parts that fall off accidentally will be removed by the referee. Deliberately detaching components for strategic purposes is a violation. If, after activation, the robot leaves the field boundary completely due to excessive speed or programming errors, or if it throws carried objects out of the field, the robot and the objects are not allowed to return for the remainder of the match.

## 5.5 Time Bonus

Teams that complete all required basic tasks and random tasks within the allotted time

will receive a **Time Bonus**. The completion of the additional task does not affect the Time Bonus. At the end of the run, contestants must immediately signal the referee to stop the timer. The remaining time is converted into points based on the intervals below (the integer part of the remaining time is used: e.g., 2.7 seconds → 2 seconds; 10.3 seconds → 10 seconds):

1. **Remaining time < 3 seconds:** 0 points
2. **3 seconds ≤ remaining time < 10 seconds:** +5 points
3. **10 seconds ≤ remaining time < 20 seconds:** +10 points
4. **20 seconds ≤ remaining time < 30 seconds:** +20 points
5. **Remaining time ≥ 30 seconds:** +30 points
## 5.6 Reset

To encourage teams to improve the stability of their programs and optimize their strategies, a **Smoothness Score** is introduced. Each run automatically starts with **50 Smoothness Points**. For every reset that occurs during the run, **5 points will be deducted**, up to a maximum deduction of 50 points. After each reset, all previously earned points for the ongoing run become invalid; task props must be restored to their initial positions, and the robot must return to the Start Zone before restarting. The timer **does not stop** during resets. Additional tasks do not allow resets.

A robot must be reset to the Start Zone under any of the following circumstances:

1. The contestant requests a reset.
2. The robot exits the competition field.
3. The contestant touches any task model or the robot without permission.
4. The robot fails to move in the direction of the flight path or deviates from the

#### track line during a task.

## 5.7 End of Match

The match will end upon the referee’s whistle under any of the following circumstances, and the time will be recorded accordingly:

1. The robot can no longer continue the remaining tasks.
2. The team completes the “Safe Return” task.
3. The team signals the referee to voluntarily end the match.
4. The time limit for the run is reached.
## 5.8 Final Score

After each match, the team’s **single-run score** will be calculated. The **Task Score** is awarded based on the task completion criteria detailed in the Robot Mission Description. After all rounds are completed, the team’s **highest single-run score** will be used as the final competition result. The Time Bonus is calculated based on the seconds of remaining time at the end of the run, following the tiered scoring rules described in Section 4.5. **Single-run Score = Task Score + Smoothness Score + Time Bonus**

## 5.9 Ranking

After all matches in a division are completed, teams are ranked according to their highest single-run score. If a tie occurs, it will be broken using the following criteria in order:

1. The team with the higher combined score from both rounds ranks higher.
2. The team with the shorter total time across both rounds ranks higher.
3. The team with fewer resets ranks higher.

4. The team using fewer motors and sensors in total ranks higher.
## 5.10 Violations

1. Each team is allowed **one mistaken start** per round. A second mistaken start will result in **zero points for that round** during the group stage and **direct** **elimination** in the final round.
2. After the match begins, if a participant **touches any field elements or the robot** **without the referee’s permission**, the first offense will result in a **warning**, and a second offense will result in **zero points for that round**.
3. If a coach or parent **verbally instructs the participant in a way that affects the** **match**, or **physically assists** in building, debugging, touching, or repairing the robot, the round will be awarded **zero points** once verified.
4. After the robot is started, it must not **intentionally detach parts or drop** **components** for strategic purposes. This is a violation. The referee will issue a warning for the first offense, and a repeated offense will result in **zero points for** **that round**. Any detached or fallen components will be immediately removed by the referee.
5. If a participant **fails to follow the referee’s instructions**, the referee may, depending on the severity, issue a **warning**, assign **zero points for that round** during the preliminary stage, **eliminate the team** in the final round, or even **disqualify the team from the event**.

#### Appendix 1

### Score Sheet – Star Cruise

#### Team Name: vvvvvvvvvvvvvvv( Group: vvvvvvvvvvvvvvvvv

|Task|Scoring Criteria|Round 1|Round 2||
|---|---|---|---|---|
|Basic Task|Start Cruise|Robot leaves the Start Zone, 60 pts.|||
||Flight Path Survey|Each time any drive wheel touches a marker line, 6 pts per line.|||
||Interstellar Vortex Beacon Delivery (A single beacon can score up to 60 points.）|Robot boards and passes through the Interstellar Vortex model, 60 pts. The task is complete when the beacon leaves its initial position; 10 pts per beacon. Beacon touches the planet area, 10 pts per beacon. Beacon fully enters the placement point, 40 pts per beacon.|||
||Gravity Launch|Control Center lights up the operation indicator, 60 pts.|||
||Safe Return|Any drive wheel of the robot fully enters the End Zone, 60 pts.|||
|Random Task|Starship Docking|The rear end of the starship remains in contact with the front of the docking cabin, 60 pts.|||
||Energy Refill|Energy block fully enters the starship, 60pts.|||
|Additional Task Total Task Score ( Basic Tasks + Random Tasks + Additional Task) Fluency Score Task Time (≤ 180 seconds, recorded to 0.1 s accuracy.) Time Score ( Awarded based on remaining time according to “(5.5) Time Score.”) Single-Round Total Score (Single-Round Total = Total Task Score + Fluency Score + Time Score) Final Score (Highest Single-Round Score)|Star Map Decoding Initial 50 pts. –5 pts for each reset (maximum deduction: 50 pts).|The operation panel touches the base plate, 10pts. Only the correct constellation is knocked down, 50pts.|||

**Referee**: ________________ **Team Member**: _______________________ <u>Passing Ma</u>**rker Lines on** <u>the Flight</u> **Path**

|Round|1|2|3|4|5|6|7|8|9|10|
|---|---|---|---|---|---|---|---|---|---|---|
|1|||||||||||
|2|||||||||||
