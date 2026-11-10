# 3D nuclear segmentation

```mermaid
flowchart TD
 A[Nuclear fluorescence / fluorescently tagged nuclei] --> B[Discrete Gaussian filter]
 B --> C[Two top-hat filters with selected radii]
 C --> D[Median and particle enhancement filters]
 D --> E[Segmentation using diameter, probability threshold and split sensitivity]
 E --> F[3D nuclear objects]
 F --> G[Visual QC and manual correction of missing nuclei]
 G --> H[Nuclear counts and morphology: volume, sphericity]
```

## Alternative deep-learning approach shown in the project figures

```mermaid
flowchart TD
 A[Nuclear fluorescence] --> B[Apeer custom deep-learning model]
 B --> C[Predicted nuclear masks]
 C --> D[Splitting step]
 D --> E[Size and sphericity filtering]
 E --> F[Visual review and correction]
 F --> G[3D nuclear objects and feature measurements]
```

The figures indicate that the custom Apeer model could be improved with additional reference images and annotations. No validated model performance metric was supplied.
