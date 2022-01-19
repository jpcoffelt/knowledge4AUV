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
174 Axoms
122 Logical Axiom Count
45  Declaration Axioms Count
15  Class Count
5   Object Property Count
18  Data Property Count
10  Individual Count
1   Annotation Property Count

```

## Classes

```
owl:Thing
    | - ManmadeThing
    |       |- Pipeline
    |       |- Garbage     
    |       |- Vehicle
    |               | - SurfaceVehicle
    |               | - UnderwaterVehicle
    | - NaturalThing
            |- LivingThing
            |       | - Animal
            |       | - Vegetation
            |- NonLivingThing
                    | - SeaFloor
                    | - WaterColumn
                    | - WaterSurface

```

## Object Properties

```
owl:topObjectProperty
    | - isLocatedOn
    | - isLocatedWithin
    | - contains
    | - supports

```

## Data Properties

```
owl:topDataProperty
    | - locationProperty
    |       |- hasLatitude
    |       |- hasLongitude
    |       |- hasDepth
    |       |- lastPositionUpdate
    | - appearanceProperty
    |       |- hasShape
    |       |- hasSize
    |       |- hasColor
    | - qualityProperty
    |       |- isRecyclable
    |       |- isNotRecyclable
    |       |- isChoppy
    |       |- isStill
    |       |- isTurbid
    | - hasMaterial
    | - isSpecies

```

## Individuals

```
owl:Thing
    | - ManmadeThing
    |       |- Site0_Torpedo
    |       |- Vehicle
    |       |       | - SurfaceVehicle
    |       |       |       | - Site0_SupportVessel
    |       |       | - UnderwaterVehicle
    |       |               | - Site0_AUV
    |       |- Pipeline
    |       |       | - Site0_Pipeline 
    |       |- Garbage  
    |               | - Site0_PlasticBottle 
    |               | - Site0_DiscardedFishingNet 
    | - NaturalThing
            |- LivingThing
            |       | - Vegetation
            |               | - Site0_SeaWeed
            |- NonLivingThing
                    | - SeaFloor
                    |       | - Site0_SeaFloor
                    | - WaterColumn
                    |       | - Site0_WaterColumn    
                    | - WaterSurface
                            | - Site0_WaterSurface         
```                                     