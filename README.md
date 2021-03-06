# EV3_GyroBlox
LEGO Mindstorms EV3 gyroscope-controlled driving blocks library

This library contains high-level building blocks in the standared EV3 Lego Mindstorms visual programming envirionment (LabView driven), for controlling two motors for driving a fixed distance and angle. The direction can be either controlled with feedback from the gyro-sensor, or open-loop. Also, a curve can be driven. The parameters can be adjusted to match the wheel diameter and distance, such that distance driven and turns made are correct.

The basic block with the parameters is Mijn_robot. ![mijn_robot](https://github.com/jan-gerard/EV3_GyroBlox/raw/gh-pages/images/mijn_robot.png)

The block Zet_op_koers rotates the robot to the desired heading.

The block Rij_koers drives a distance (optionally after setting the correct heading), and optionally uses gyro-feedback for keeping the right heading. If an obstacle is causing a deviation from the right course, the robot pulls back, and tries to recover.

The block Rij_bocht drives a circle section. You can enter distance and radius, distance and angle, or radius an angle. This block can optionally use the gyro-sensor. This block uses Rij_koers to follow the momentary heading of the curve.

The block Richt_tegen_muur aligns the robot with a wall. You can enter the known heading to align the gyro-based compass. ![richt_tegen_muur](https://github.com/jan-gerard/EV3_GyroBlox/raw/gh-pages/images/richt_tegen_muur.png)

The block Koers_is sets the current heading to a specific value. This block is used by Richt_tegen_muur.

Blocks to stop when a black line is observed, or when one of the other motors detects a change in output angle, are included as well. They stop the loop 'rijden' that is used by Rij_koers (and Rij_bocht). 

The block Langzaam_rijden can be used to set a slow acceleration value to gradually change start or stopping speed.

The file PolyGroup_Icons.zip can be unzipped into C:\Program Files (x86)\LEGO Software\LEGO MINDSTORMS ??? EV3\Resources\MyBlocks\images to get meaningfull distinctive icons for the blocks in this library.

The contents of the Unzipped folder is as good as possible in sync with the GyroBlox.ev3s file. In fact, GyroBlox.ev3s is a zip file with modified extension, containing xml-files that contain the actual EV3 model. They can be edited and put back into the GyroBlox.ev3s, or GyroBlox.ev3s can be edited with the LEGO Mindstorms software, and its contents unzipped to the unzipped folder. 
I would like to find a way to have GITHUB handle the zipping/unzipping automatically. You could download the 'unzipped' folder from GITHUB as zip file, and rename the extension to 3v3s.
