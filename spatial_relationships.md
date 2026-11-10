# Spatial relationship analysis

```mermaid
flowchart TD
 A[Reviewed nuclear object masks] --> C[Import segmented objects into arivis relationship pipeline]
 B[Reviewed cell object masks] --> C
 D[Reviewed organoid object masks] --> C
 C --> E[Define containing compartment and objects of interest]
 E --> F[Select objects inside or intersecting compartment by at least one voxel]
 F --> G[Count nuclei associated with each cell]
 F --> H[Count cells associated with each organoid]
 F --> I[Other colocalized object counts where applicable]
 G --> J[Export object-level relationship measurements]
 H --> J
 I --> J
```

The one-voxel intersection criterion is a spatial association rule, not necessarily proof of complete biological containment. The precise treatment of objects intersecting multiple compartments is not specified in the supplied methods.
