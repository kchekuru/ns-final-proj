
![](https://img.shields.io/badge/license-MIT-green.svg)
![](https://img.shields.io/badge/language-python-blue.svg)
![](https://img.shields.io/badge/framework-keras-orange.svg)



## Active Network Attack Detection System: Explaining Deep Learning-based Active Network Attack Detection Systems

This repo includes the source code for the "Explaining Deep Learning-based Active Network Attack Detection Systems" project. The code(notebooks,python scripts) is hardware independent and is optimized for execution on Github CodeSpaces.

Model can be embedded into network devices, for network attack detection and esclation to Security Operation Response Center


 
## Implementation Notes

Testing and running the code is straightforward, giving developers the flexibility to utilize either Github Codespaces or a local machine for their testing purposes.


1. **Github Codespaces**:
   - Run the Demo **explanation.ipynb** notebook
   - Although a GPU is not required, it can significantly accelerate the execution
     
2. **Local Machine**:
   
   > pip install -r requirements.txt
   > python explanation.py
   
 3. **Retrain the Deep Learning - Active Network Attack Detection System**
    - Please carefully update the testcases accordingly in the **explantion.py** if the users want to retrain the models. 
    - **kitsune.ipynb** contains the reimplementation of kitnet. Please download the dataset and put them under the **Data** folder.
    - **kdd.ipynb** includes one *Autoencoder* and one **stateless** *RNN* based DL-NADS
    - **kdd_histroy.ipynb** contains one **stateful** LSTM based DL-NADS.
 
## Citation & Paper


The results of this project was published in the paper entitled "Network Attack Detection System: Explaining Deep Learning-based Network Attack Detection Systems" in the USENIX Security 2023. Please cite original paper for original work and any modification including this to support GitHub Codespaces, refactored to move away from google drive
git clone https://github.com/CactiLab/code-xNIDS.git

```
@inproceedings{wei2023xnids,
 title = {{xNIDS: Explaining Deep Learning-based Network Intrusion Detection Systems for Active Intrusion Responses}},
 author = {Wei, Feng and Li, Hongda and Zhao, Ziming and Hu, Hongxin},
 booktitle = {{USENIX Security}},
 year = {2023},
}

```