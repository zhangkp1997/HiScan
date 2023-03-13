# HiScan
Hierarchical Imitation Learning for Goal-directed Scanpath Prediction on Long-term Tasks


## Scripts
- Train a model with
    ```
    python train.py <hparams> <dataset_root> [--cuda=<id>]
    ```
- Model evaluation
     ```
    python test.py
    ```
    
## Data Preparation
The typical `<dataset_root>` should be structured as follows
```
<dataset_root>
    -- bbox_annos.npy                                # bounding box annotation for each image (available at COCO)
    -- coco_search18_fixations_TP_train.json         # train split of human scanpaths (ground-truth)
    -- coco_search18_fixations_TP_validation.json    # validation split of human scanpaths (ground-truth)
    -- ./DCBs
        -- ./HR                                      # high-resolution belief maps of each input image (pre-computed)
        -- ./LR                                      # low-resolution belief maps of each input image (pre-computed)
