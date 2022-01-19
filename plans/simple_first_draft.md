# MISSION: Pipeline Inspection with Single AUV (Moderate Complexity)

## Initialization:
- AUV model
- sensor configuration
- battery capacity and state
- initial AUV pose
- final AUV pose
- waypoints for searches
- search pattern (lawnmower, spiral, ...)
- perception algorithms
- other a priori knowledge
- mission plan

## Execution:
### in parallel do:
- #### monitor (internal) moisture:
  - *loop:*
    - read moisture sensor
    - *if moisture threshhold exceeded:*
	    - notify surface operators that pipeline search/inspection is being terminated
	    - terminate pipeline search/inspection
	    - surface AUV
	    - notify surface operators of current pose
	    - terminate mission
- #### monitor battery:
  - *loop:*
    - read battery sensor
    - *if battery low:*
      - notify surface operators that pipeline search/inspection is being terminated
      - terminate pipeline search/inspection
      - travel to final pose
      - notify surface operators of final pose
      - terminate mission

- #### avoid obstacles:
  - *loop:*
    - read forward-looking and/or mechanically scanned sonar
    - run obstacle detection algorithms
    - *if obstacle detected:*
      - pause pipeline search/inspection
      - run local path planning algorithm
      - maneuver to avoid obstacle
      - resume pipeline search/inspection

- #### update position:
  - *loop:*
    - read positioning sensors (IMU/INS/DVL/GPS)
    - run position calculation algorithms

- #### pipeline search:
  - *loop:*
    - *if pipeline detected:*
      - pause pipeline search
    - *else:*
      - *if all waypoints visited:*
        - notify surface operators that pipeline search/inspection is being terminated
        - travel to final pose
        - notify surface operators of final pose
        - terminate mission
      - *else:*
        - determine next waypoint
        - run global path planning algorithm
        - navigate to next way point
        - *while search pattern not completed:*
          - determine next pose in pattern
          - run local path planning algorithm
          - *while navigating to next pose:*
            - *if have sidescan sonar:*
              - read sidescan sonar
              - run 2D pipeline detection algorithm
            - *if have multibeam sonar:*
              - read multibeam sonar
              - run 3D pipeline detection algorithm
            - *if pipeline detected:*
              - pause pipeline search
              - start pipeline inspection

- #### pipeline inspection:
  - *loop:*
    - *if pipeline not detected:*
      - pause pipeline inspection
      - start pipeline search
    - *else:*
      - determine next pose of pipeline
      - run local path planning algorithm 
      - determine next pose of AUV
      - start navigating to next pose
      - *if have camera(s) and water is not turbid:*
        - read camera(s)
        - run 2D pipeline detection algorithm
      - *else:*
        - *if have sidescan sonar:*
          - read sidescan sonar
          - run 2D pipeline detection algorithm
        - *if have multibeam sonar:*
          - read multibeam sonar
          - run 3D pipeline detection algorithm
      - *if anomaly detected:*
        - run anomaly classification algorithms
