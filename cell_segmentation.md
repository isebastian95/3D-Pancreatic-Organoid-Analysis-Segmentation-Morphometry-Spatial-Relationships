# Membrane-based cell segmentation

```mermaid
flowchart TD
 A[Cell membrane fluorescence] --> B[Discrete Gaussian denoising]
 B --> C[Two top-hat filters with selected radii]
 C --> D[Membrane-based segmentation]
 D --> E[Adjust minimum intensity threshold, split sensitivity and maximum area]
 E --> F[3D segmented cell objects]
 F --> G[Visual QC and correction when needed]
 G --> H[Cell counts, volume and sphericity]
```

A pretrained Cellpose cell model was proposed in the initial planning slide, but the supplied methodology does not establish that it was used in the final cell segmentation workflow.
