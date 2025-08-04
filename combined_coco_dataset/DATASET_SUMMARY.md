# Combined COCO Dataset Summary

## Overview
This document provides a summary of the combined COCO dataset created by merging three individual datasets:
1. `bottle-cap.v3i.coco` - Bottle cap defect detection dataset
2. `Gesture segmentation.v2i.coco` - Hand gesture segmentation dataset  
3. `hand.v2i.coco` - Hand detection dataset

## Dataset Statistics

### Total Dataset Size
- **Total Images**: 3,270
- **Total Annotations**: 3,367
- **Total Categories**: 14

### Split Distribution
| Split | Images | Annotations | Categories |
|-------|---------|-------------|------------|
| Train | 2,954 | 3,042 | 14 |
| Test | 146 | 155 | 0* |
| Valid | 170 | 170 | 0* |

*Note: Categories are primarily defined in the train split, with test/valid splits referencing the same category IDs.

### Categories
The combined dataset contains 14 different categories:

#### Bottle Cap Categories (IDs 1-6)
1. **bottle-cap-defects** (ID: 1)
2. **Broken Cap** (ID: 2) 
3. **Broken Ring** (ID: 3)
4. **Good Cap** (ID: 4)
5. **Loose Cap** (ID: 5)
6. **No Cap** (ID: 6)

#### Gesture Categories (IDs 7-12)
7. **0** (ID: 7) - Gesture class 0
8. **1** (ID: 8) - Gesture class 1
9. **2** (ID: 9) - Gesture class 2
10. **3** (ID: 10) - Gesture class 3
11. **4** (ID: 11) - Gesture class 4
12. **5** (ID: 12) - Gesture class 5

#### Hand Categories (IDs 13-14)
13. **hand** (ID: 13) - General hand detection
14. **Hand raise** (ID: 14) - Raised hand gesture

## File Naming Convention
Images from different source datasets are prefixed to avoid naming conflicts:
- `bottle-cap_v3i_coco_*` - Images from bottle cap dataset
- `Gesture_segmentation_v2i_coco_*` - Images from gesture segmentation dataset
- `hand_v2i_coco_*` - Images from hand detection dataset

## Directory Structure
```
combined_coco_dataset/
├── train/
│   ├── _annotations.coco.json
│   └── [2,954 image files]
├── test/
│   ├── _annotations.coco.json
│   └── [146 image files]
└── valid/
    ├── _annotations.coco.json
    └── [170 image files]
```

## Annotation Format
The dataset follows the standard COCO annotation format with:
- **Images**: Contains image metadata (id, filename, width, height)
- **Annotations**: Contains bounding box/segmentation annotations
- **Categories**: Contains category definitions with unique IDs
- **Info**: Contains dataset metadata

## Usage
This combined dataset can be used for:
1. **Multi-class object detection** - Training models to detect bottle caps, hands, and gestures
2. **Transfer learning** - Pre-training on one domain and fine-tuning on another
3. **Multi-task learning** - Training models to handle multiple object types simultaneously
4. **Data augmentation** - Increasing dataset diversity for better generalization

## Data Quality Notes
- All images have been successfully copied and verified
- Annotation IDs have been updated to prevent conflicts between datasets
- Category IDs have been remapped to create a unified category system
- Image filenames include dataset prefixes to maintain traceability

## Created
- **Date**: August 4, 2024
- **Total Processing Time**: Approximately 30 seconds
- **Script Used**: `combine_datasets.py`
- **Output Location**: `/Users/tuhinabanerjee/Desktop/CNN/combined_coco_dataset`
