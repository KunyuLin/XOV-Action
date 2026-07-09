# XOV-Action: Towards Generalizable Open-Vocabulary Action Recognition

## 🌈 Overview

![alt text](xovabench_setting.png)
<!-- https://github.com/KunyuLin/XOVABench/blob/main/xovabench_setting.png?raw=true -->

- This repository is for the paper titled "[*XOV-Action: Towards Generalizable Open-Vocabulary Action Recognition*](https://arxiv.org/abs/2403.01560)". 
In this work, we delve into an intriguing question: **Can CLIP-based video learners effectively generalize to video domains that they have not encountered during training?** 

<p align="center">
  <img src="xovabench_results.png" alt="XOVABench results" width="500">
</p>
<!-- https://github.com/KunyuLin/XOVABench/blob/main/xovabench_results.png?raw=true -->

- We establish **XOVABench**, a **CROSS**-domain **O**pen-**V**ocabulary **A**ction recognition Benchmark, and our evaluation reveals that existing CLIP-based video learners exhibit limited performance when recognizing actions in unseen test domains.
- To address the generalizable open-vocabulary action recognition task, our work contributes a novel XOV-Action model that focuses on two critical challenges: novel action concepts and scenario discrepancy across video domains.

## 📚 XOVABench Benchmark
### New Features 🔥
- XOVABench is the first benchmark, composed of two training datasets and four test datasets, for evaluating models in the *generalizable open-vocabulary action recognition* task.
- We identify closed-set and open-set categories for each test domain, thus providing a comprehensive way to evaluate models across various situations. *This is different from prevailing existing open-vocabulary action recognition works that treat all the categories in another datasets as open-set.*

### Benchmark Components
#### Training Datasets 
- **Kinetics400**: One of the most widely-used action recognition datasets, consisting of 400 action categories.
- **Kinetics150**: A subset of Kinetics400, composed of 150 action categories selected from the full Kinetics400.
#### Test Datasets
- **UCF101**: One of the most widely-used action recognition datasets, consisting of 101 action categories.
- **HMDB51**: A widely-used action recognition datasets consisting of 51 action categories.
- **ARID**: A dataset consisting of 11 categories of action videos, which are recorded under dark environments.
- **NEC-Drone**: A dataset consisting of 16 categories of action videos, which are recorded by drones in the same basketball court. 

### Evaluation Metrics
- The **closed-set accuracy** measures the recognition performance of closed-set categories, which primarily evaluates the model abilities of tackling domain gaps when fitting training videos.
- The **open-set accuracy** measures the performance of open-set categories, which evaluates the generalization abilities across both video domains and action categories.
- The **overall accuracy** measures the recognition performance over all categories, which provides a holistic view of model effectiveness across various situations.

Please refer to our paper for more details. 

## 🚀 Methodology
- We propose **XOV-Action**, a model for generalizable open-vocabulary action recognition.
- XOV-Action captures rich action-related concepts from videos by **Diversified Elaboration Representation Learning**.
- XOV-Action learns scene-agnostic video representations by **Scene-Aware Video-text Alignment**.
- The code for our proposed method is coming soon.

## 📌 Acknowledgement 
- Our benchmark is established based on [Kinetics400](https://arxiv.org/abs/1705.06950), [UCF101](https://www.crcv.ucf.edu/data/UCF101.php), [HMDB51](https://serre-lab.clps.brown.edu/resource/hmdb-a-large-human-motion-database/), [ARID](https://xuyu0010.github.io/arid.html) and [NEC-Drone](https://www.nec-labs.com/research/media-analytics/projects/unsupervised-semi-supervised-domain-adaptation-for-action-recognition-from-drones/). Thanks for the authors' diligent efforts and significant contributions. 

- Our method is implemented based on the codebases [ViFi-CLIP](https://github.com/muzairkhattak/ViFi-CLIP) and [Open-VCLIP](https://github.com/wengzejia1/Open-VCLIP). Thanks for the authors' high-quality codebases. 

- If you find our paper/code/benchmark useful, please consider citing our paper:
```
@article{lin2026xovaction,
  author       = {Kun{-}Yu Lin and Henghui Ding and Jia{-}Run Du and Jiaming Zhou and Yi{-}Xing Peng and Yu{-}Ming Tang and Zhilin Zhao and Chen Change Loy and Wei{-}Shi Zheng},
  title        = {XOV-Action: Towards Generalizable Open-Vocabulary Action Recognition},
  journal      = {{IEEE} Transactions on Pattern Analysis and Machine Intelligence},
  year         = {2026},
}
```
