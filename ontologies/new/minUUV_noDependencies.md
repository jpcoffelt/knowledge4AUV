# minUUV_noDependencies

# Details

Created by:
    Jeremy Coffelt
    ESR11 in the REMARO MSCA Project
    ROSEN Research and Technology
    Bremen, Germany

Published:
    github.com/jpcoffelt/knowlege4AUV
    2022-01-09

Filetype:
    Written in OWL2 using Protégé and saved in RDF/XML syntax

## Description

This is minimal ontology for the ROSEN pipeline inspection case study within the REMARO MSCA Project. It currently has no dependencies on the University of Bremen Institute of Artificial Intelligence ontology stack (e.g., DUL, URDF, KnowRob, SOMA, SRDL).

## Metrics

??? Axoms
??? Logical Axiom Count
??? Declaration Axioms Count
??? Class Count
??? Object Property Count
??? Data Property Count
??? Individual Count
??? Annotation Property Count

## Classes

owl:Thing
    |
    | - Robot
    |     |
    |     |- MobileRobot
    |               |
    |               | - UnderwaterRobot
    |                       |
    |                       | - AUV
    |                       | - ROV
    |                       | - Glider
    | - RobotPart
    |       |
    |       | - Tether
    |       |
    |       | - Actuator
    |               |
    |               | - PositionSensor
    |               | - EnvironmentSensor
    |               | - PerceptionSensor
    |                       |
    |                       | - AcousticSensor
    |                       | - OpticalSensor
    |
    | - RobotCapability
            |
            | - NavigationCapability
            | - PlanningCapability
            | - PerceptionCapability
                    |
                    | - VisonPerceptionCapability
                    | - SonarPerceptionCapability                 

## Object Properties

owl:topObjectProperty
    |
    | - requiresPart
    | - requiresCapability
    | - givesCapability
    | - hasCapability
    | - hasPart
    | - isAttachedTo

## Data Properties

owl:topDataProperty
    |
    | - pipeProperty
    |       |
    |       |- hasLength
    |       |- hasOuterDiameter
    |       |- hasWallThickness
    |       |- hasMaterial
    |       |- hasCorrosionProtection
    |
    | - locationProperty
    |       |
    |       |- hasLatitude
    |       |- hasLongitude
    |       |- hasDepth
    |       |- hasOrientation
    |
    | - appearanceProperty
            |
            |- hasShape
            |- hasSize
            |- hasColor

## Individuals

owl:Thing
    |
    | - Pipeline
    |       |
    |       |- Site0_PipelineA
    |       |- Site0_PipelineB
    |
    | - PipeSegment
    |       |
    |       |- Site0_PipelineA_Segment0
    |       |- Site0_PipelineA_Segment1
    |       |- Site0_PipelineA_Segment2
    |       |- Site0_PipelineB_Segment0
    |       |- Site0_PipelineB_Segment1
    |       |- Site0_PipelineB_Segment2
    |       |- Site0_Pipeline3_Segment2
    |
    | - Nearby Object
    |       |
    |       |- SafeObject
    |       |       |   
    |       |       | - Site0_Boulder0  
    |       |
    |       |- DangerousObject
    |               |   
    |               | - Site0_Boulder1  
    |               | - Site0_Torpedo   
    |
    | - Terrain
            |
            |- Site0_Terrain