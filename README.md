# BalanceBot

## Important Instructions

1. Please install all the libraries in the .zip file of the arduino IDE program.
2. Please modify the P,I and D values in the code as these values vary with the build.
3. Please modify the motor slack number in the code based on how well the two motors perform.

## Configuring P,I and D

1. Set I and D term to 0, and adjust P so that the robot starts to oscillate (move back and forth) about the balance position. P should be large enough for the robot to move but not too large otherwise the movement would not be smooth.
2. With P set, increase I so that the robot accelerates faster when off balance. With P and I properly tuned, the robot should be able to self-balance for at least a few seconds.
3. Finally, increase D so that the robot would move about its balanced position more gently, and there shouldn’t be any significant overshoot.
4. If first attempt doesn’t give the satisfying results, reset PID values and start over again with different value of P.
5. Repeat the steps until you find a certain PID value which gives the satisfactory results.
6. A fine tuning can be done to further increase the performance of PID system.
7. In fine tuning, PID values are restricted to neighboring values and effects are observed in practical situations.

### Important Points

1. There is no clear boundary for taking P, I or D values and is mostly taken based on experience.
2. Theoretically, I and D values depend on the state of the system. Ex. Mechanical Structure, Physical properties, Electrical properties (if any) etc.
3. But practically, it also depends on the external conditions. Ex. Atmospheric conditions etc.
4. PID values and method of choosing PID values depends largely on the characteristics of system. A method producing a good result for a system __*may not work at all for another system with different characteristics.*__

### What P, I & D values means practically?

For the BalanceBot:

* P-P determines the force with which the robot will correct itself. A lower P shows robot’s inability to balance itself and a higher P will shows the violent behavior.

* I-I determines the response time of robot for correcting itself. Higher the P, Faster it will response.

* D- D determines the sensitivity of robot to the error in its state. It is used to smoothen/depress the robot oscillations. A lower D is unable to remove oscillations and a higher D will cause violent vibrations.

Depending on your PID tuning, the bot will be able balance itself now.

