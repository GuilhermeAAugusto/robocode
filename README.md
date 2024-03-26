package Roboshark;
import robocode.*;
//import java.awt.Color;

// API help : https://robocode.sourceforge.io/docs/robocode/robocode/Robot.html

/**
 * Baby_shark - a robot by (your name here)
 */
public class Babyshark extends AdvancedRobot
{
	/**
	 * run: Baby_shark's default behavior
	 */
	public void run() {
		// Initialization of the robot should be put here

		// After trying out your robot, try uncommenting the import at the top,
		// and the next line:

		// setColors(Color.red,Color.blue,Color.green); // body,gun,radar

		// Robot main loop
		while(true) {
			// Replace the next 4 lines with any behavior you would like
			setAhead(10);
			setTurnLeft(1);
			//setBack(100);
			setTurnRight(1);
			setTurnGunRight(100);
			setTurnGunLeft(100);
			//setTurnGunRight(180);
			execute();

		}
	}

	/**
	 * onScannedRobot: What to do when you see another robot
	 */
	public void onScannedRobot(ScannedRobotEvent e) {
		// Replace the next line with any behavior you would like
			//setTurnGunRight(360);
			setFire(50);
			setTurnLeft(10);
			setBack(100);
			//setTurnLeft(1);
			//fire(100);
			execute();
	
	}

	/**
	 * onHitByBullet: What to do when you're hit by a bullet
	 */
	public void onHitByBullet(HitByBulletEvent e) {
		// Replace the next line with any behavior you would like
			setTurnRight(80);
				setBack(100);
			setFire(+10);
			execute();
	}
	
	/**
	 * onHitWall: What to do when you hit a wall
	 */
	public void onHitWall(HitWallEvent e) {
		// Replace the next line with any behavior you would like
		setTurnRight(100);
		setBack(50);
			//setAhead(100);
		
		execute();
	}	
}
