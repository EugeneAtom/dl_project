# dl_project
Венгерское внимание


Google drive with the dataset, embeddings and adjacency matrices https://drive.google.com/drive/folders/1csZ98jszqoT_-Qsme9b-26E1pxxqtvy2?usp=sharing

The directory `preprocessing` contains necessary notebooks for preprocessing the data (graphs, images).

Names of the notebooks roughly correspond to their purpose (`train`, `baselines`, `model`).

There are additional notebooks from the Superglue paper, which was modified in order to satisfy our settings. We included only modified notebooks, in order to run Superglue one should clone https://github.com/magicleap/SuperGluePretrainedNetwork and replace modified notebooks.
Run this command for superglue: `./match_pairs.py --input_dir 'assets/birds' --input_pairs='assets/test_idx_pairs.txt' --superglue indoor --nms_radius 3 --resize_float --match_threshold 0.001 --keypoints 'assets/rescaled_480_landmarks' --viz`

The resulting matches are illustrated here:

**Ground truth match**
![Ground truth match](./images/gt.png)

As one can see Superglue match not all keypoints.
Lines from top left corner correspond to matches of parts of birds which are not present on the picture.

**Superglue**
![Superglue](./images/superglu.png)

Our results are much better
**With attention**
![](./images/with_attention.png)

**Without attention**
![Without attention](./images/without_attention.png)
