# minPipeline_noDependencies

# Details

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
225 Axoms
166 Logical Axiom Count
44  Declaration Axioms Count
11  Class Count
7   Object Property Count
16  Data Property Count
13  Individual Count
1   Annotation Property Count
```

## Classes
```
owl:Thing
    | - Pipeline
    | - PipeSegment
    |       |- StraightSegment
    |       |- SegmentWithValve
    |       |- SegmentWithAnode
    |       |- RightBend
    | - Nearby Object
    |       |- SafeObject
    |       |- DangerousObject
    | - Terrain
```

## Object Properties
```
owl:topObjectProperty
    | - hasPart
    | - isPartOf
    | - isBefore
    | - isAfter
    | - isNear
    | - touches
```

## Data Properties
```
owl:topDataProperty
    | - pipeProperty
    |       |- hasLength
    |       |- hasOuterDiameter
    |       |- hasWallThickness
    |       |- hasMaterial
    |       |- hasCorrosionProtection
    | - locationProperty
    |       |- hasLatitude
    |       |- hasLongitude
    |       |- hasDepth
    |       |- hasOrientation
    | - appearanceProperty
            |- hasShape
            |- hasSize
            |- hasColor
```

## Individuals
```
owl:Thing
    | - Pipeline
    |       |- Site0_PipelineA
    |       |- Site0_PipelineB
    | - PipeSegment
    |       |- Site0_PipelineA_Segment0
    |       |- Site0_PipelineA_Segment1
    |       |- Site0_PipelineA_Segment2
    |       |- Site0_PipelineB_Segment0
    |       |- Site0_PipelineB_Segment1
    |       |- Site0_PipelineB_Segment2
    |       |- Site0_Pipeline3_Segment2
    | - Nearby Object
    |       |- SafeObject
    |       |       | - Site0_Boulder0  
    |       |- DangerousObject
    |               | - Site0_Boulder1  
    |               | - Site0_Torpedo   
    | - Terrain
            |- Site0_Terrain
```