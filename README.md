# Simplifying Robot Grasping in Manufacturing with a Teaching Approach based on a Novel User Grasp Metric

This is the supporting material for the paper "Simplifying Robot Grasping in Manufacturing with a Teaching Approach based on a Novel User Grasp Metric". Within this repo the code used for fusing the user input together with Dex-Net is provided. Moreover,supplementary materials (i.e., figures, example of test objects) are provided. If you find this work useful please consider citing it.

## News 

[2023/09/29] Submission of final paper to 2023 International Conference on Industry 4.0 and Smart Manufacturing (ISM) and finalization of the repo.

[2023/08/10] Acceptance to the 2023 International Conference on Industry 4.0 and Smart Manufacturing (ISM).

[2023/06/28] Submission of paper to the 2023 International Conference on Industry 4.0 and Smart Manufacturing (ISM) and polishing of the repo.

[2022/09/12] Introduction of code and supplementary materials.

## Installation

### [DISCLAIMER] Prerequisites for Dex-Net
This repo is a fork of the Berkeley AUTOLAB's dex-net GQ-CNN. Therefore, here we focus only on the modifications for fusing the user input.For Dex-Net documentation and code see [[1]](https://berkeleyautomation.github.io/dex-net/), [[2]](https://berkeleyautomation.github.io/gqcnn/), and [[3]](https://github.com/BerkeleyAutomation/gqcnn). Dex-Net general information can be find in:

    @article{mahler2019learning,
        title={Learning ambidextrous robot grasping policies},
        author={Mahler, Jeffrey and Matl, Matthew and Satish, Vishal and Danielczuk, Michael and DeRose, Bill and McKinley, Stephen and Goldberg, Ken},
        journal={Science Robotics},
        volume={4},
        number={26},
        pages={eaau4984},
        year={2019},
        publisher={AAAS}
    }

### Prerequisites

The package has only been tested with Python 3.7 on Ubuntu 16.04. We recommend using a Python environment management system, in particular Virtualenv. 

    virtualenv -p /usr/bin/python3.7 ~/virtualenv/dex-net-user-input
    source ~/virtualenv/dex-net-user-input/bin/activate

### 1. Clone the repository

Clone or download the project from Github.

    git clone https://github.com/matteopantano/Dex-Net-userInput

### 2. Run pip installation

Change directories into the gqcnn repository and run the pip installation.

    pip install .

This will install gqcnn in your current virtual environment.

## Inference

With the virtualenv activated, run from the gqcnn directory execute:

    ./run_DexNet_with_user_input_example.sh

You can adjust the parameters defined in the shell script to point to your own data.

Note that ``segmask``, ``config_filename`` and ``user_input_fusion_method`` are optional parameters.

If ``user_input_fusion`` method is provided, also ``camera_pose_path``,  ``user_input_3d_dir`` must be provided

## Useful material

The objects used for the evaluation are stored under in [`data/objects`](data/objects) and are divided upon object for [`virtual evaluation`](data/objects/virtualEvaluation) and [`physical evaluation`](data/objects/physicalEvaluation). For sake of clarity some figures are reported here:

### Virtual evaluation

<img src="https://github.com/matteopantano/Dex-Net-userInput/blob/main/data/objects/virtualEvaluation/imageVirtAll.png?raw=true" alt="drawing" width="800"/>

### Physical evaluation

<img src="https://github.com/matteopantano/Dex-Net-userInput/blob/main/data/objects/physicalEvaluation/imagePhyAll.png?raw=true" alt="drawing" width="800"/>

## Contributors

* **Vladislav Klass** - [vladi315](https://github.com/vladi315)
* **Matteo Pantano** - [matteopantano](https://github.com/matteopantano)

## Reference

    @software{pantano2022weaklysupervised,
        title={A Weakly-supervised Labeling Approach for Robotic Grasp Teaching and its Effects on Grasp Quality and Operator's Human Factors},
        author = {Matteo Pantano and Vladislav Klass},
        title = {Fusing of the user input in Dex-Net},
        url = {https://github.com/matteopantano/Dex-Net-userInput},
        version = {1.0},
        date = {2022-09-12},
    }

    @inproceedings{pantano2023,  
      author = {Matteo Pantano, Vladislav Klass, Qiaoyue Yang, Akhil Sathuluri, Daniel Regulin, Lucas Janisch, Markus Zimmermann, Dongheui Lee},  
      title = {Simplifying Robot Grasping in Manufacturing with a Teaching Approach based on a Novel User Grasp Metric},  
      booktitle = {2023 International Conference on Industry 4.0 and Smart Manufacturing (ISM)},  
      year = {2023},  
      address = {Lisbon, Portugal},  
    }  
