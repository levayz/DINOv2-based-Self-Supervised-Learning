# DINOv2-based-Self-Supervised-Learning

This work was accepted into ISBI 2024.
[Link to our paper](https://arxiv.org/abs/2403.03273).

## Abstract
Deep learning models have emerged as the cornerstone of
medical image segmentation, but their efficacy hinges on the
availability of extensive manually labeled datasets and their
adaptability to unforeseen categories remains a challenge.
Few-shot segmentation (FSS) offers a promising solution by
endowing models with the capacity to learn novel classes
from limited labeled examples. A leading method for FSS
is ALPNet, which compares features between the query im-
age and the few available support segmented images. A key
question about using ALPNet is how to design its features.
In this work 1 , we delve into the potential of using features
from DINOv2, which is a foundational self-supervised learn-
ing model in computer vision. Leveraging the strengths of
ALPNet and harnessing the feature extraction capabilities of
DINOv2, we present a novel approach to few-shot segmen-
tation that not only enhances performance but also paves the
way for more robust and adaptable medical image analysis.

## How To Run
### 1. Data preprocessing
Please refer to https://github.com/cheng-01037/Self-supervised-Fewshot-Medical-Image-Segmentation for data preprocessing.

### 2. Training and Validation
```
./main.sh [MODE] [MODALITY] [LABEL_SET]
```
MODE - validation or training \
MODALITY - ct or mri \
LABEL_SET - 0 (kidneys), 1 (liver spleen)

for example:
```
./main.sh training mri 1
```
Please refer to `main.sh` for further configurations.

## Acknowledgements
This work is largely based on [ALPNet](https://github.com/cheng-01037/Self-supervised-Fewshot-Medical-Image-Segmentation) and [DINOv2](https://github.com/facebookresearch/dinov2).

## Cite
If you found this repo useful, please consider giving us a citation and a star!

```bibtex
@misc{ayzenberg2024dinov2,
      title={DINOv2 based Self Supervised Learning For Few Shot Medical Image Segmentation}, 
      author={Lev Ayzenberg and Raja Giryes and Hayit Greenspan},
      year={2024},
      eprint={2403.03273},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
