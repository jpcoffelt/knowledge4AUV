# min_uuv

## Details

Created by:
```
    Jeremy Coffelt
    ESR11 in the REMARO MSCA Project
    ROSEN Research and Technology
    Bremen, Germany
```

Published:
```
    github.com/jpcoffelt/knowlege4AUV
    2022-01-09
```

Filetype:
```
    Written in OWL2 using Protégé and saved in RDF/XML syntax
```

## Description

This is minimal ontology for the ROSEN pipeline inspection case study within the REMARO MSCA Project. It currently has no dependencies on the University of Bremen Institute of Artificial Intelligence ontology stack (e.g., DUL, URDF, KnowRob, SOMA, SRDL).

## Metrics
```
159 Axoms
102 Logical Axiom Count
50  Declaration Axioms Count
24  Class Count
7   Object Property Count
14  Data Property Count
8   Individual Count
1   Annotation Property Count
```

## Classes
```
owl:Thing
    | - Robot
    |     |- MobileRobot
    |               | - UnderwaterRobot
    |                       | - AUV
    |                       | - ROV
    |                       | - Glider
    | - RobotPart
    |       | - Tether
    |       | - Actuator
    |       |       | - Rudder
    |       |       | - Propeller
    |       | - Sensor
    |               | - PositionSensor
    |               | - EnvironmentSensor
    |               | - PerceptionSensor
    |                       | - AcousticSensor
    |                       | - OpticalSensor
    | - RobotCapability
            | - LocomotionCapability
            | - PlanningCapability
            | - PerceptionCapability
                    | - VisonPerceptionCapability
                    | - SonarPerceptionCapability                 
```

## Object Properties
```
owl:topObjectProperty
    | - requiresPart
    | - requiresCapability
    | - givesCapability
    | - hasCapability
    | - hasPart
    | - isAttachedTo
```

## Data Properties
```
owl:topDataProperty
    | - partProperty
    |       |- hasPose
    |       |- hasMesh
    |       |- hasMass
    |       |- hasMaterial
    |       |- hasColor
    | - robotProperty
            |- hasLatitude
            |- hasLongitude
            |- hasDepth
            |- hasOrientation
            |- lastPositionUpdate
            |- hasBatteryCapacity
```

## Individuals
```
owl:Thing
    | - Robot
    |     |- MobileRobot
    |               | - UnderwaterRobot
    |                       | - AUV
    |                             | - REMARO_AUV
    | - RobotPart
    |       | - Sensor
    |               | - PositionSensor
    |               |       | - InertialNavigationSystem
    |               | - EnvironmentSensor
    |               |       | - TurbiditySensor
    |               | - PerceptionSensor
    |                       | - AcousticSensor
    |                       |       | - SideScanSonar
    |                       | - OpticalSensor
    |                               | - HighDefColorCamera
    | - RobotCapability
            | - PerceptionCapability
                    | - VisonPerceptionCapability
                    |       | - ObjectDetectionWithCamera
                    | - SonarPerceptionCapability  
                            | - PipelineSegmentationWithSonar
```
