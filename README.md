
![](https://img.shields.io/badge/license-MIT-green.svg)
![](https://img.shields.io/badge/language-python-blue.svg)
![](https://img.shields.io/badge/framework-keras-orange.svg)



## Network Attack Detection System: Explaining Deep Learning-based Network Attack Detection Systems for Active Intrusion Responses

This repo includes the source code for the "Explaining Deep Learning-based Network Attack Detection Systems for Active Attack Responses" project. The code(notebooks,python scripts) is hardware independent and is optimized for execution on Github CodeSpaces.

Model can be embedded into network devices, for network attack detection and esclation to Security Operation Response Center


 
## Implementation Notes

Testing and running the code is straightforward, giving users the flexibility to utilize either Github Codespaces or a local machine for their testing purposes.

1. **Google Colab**:
   > 
   - Rename the folder
   > mv code - Network Intrusion Detection System   Network Intrusion Detection System
   - Upload the folder to **Colab Notebooks** folder under google drive
   - Run the Demo **explanation.ipynb** notebook
   - Although a GPU is not required, it can significantly accelerate the execution
     
2. **Local Machine**:
   
   > pip install -r requirements.txt
   
   > python explanation.py
   
 3. **Retrain the DL-NIDS**
    - Please carefully update the testcases accordingly in the **explantion.py** if the users want to retrain the models. 
    - **kitsune.ipynb** contains the reimplementation of kitnet. Please download the dataset and put them under the **Data** folder.
    - **kdd.ipynb** includes one *Autoencoder* and one **stateless** *RNN* based DL-NIDS
    - **kdd_histroy.ipynb** contains one **stateful** LSTM based DL-NIDS.

## Contribute

Contributions are always welcome! 

## Citation & Paper


The results of this project was published in the paper entitled "NIDS: Explaining Deep Learning-based Network Intrusion Detection Systems for Active Intrusion Responses" in the USENIX Security 2023. If you want to cite original paper or any extrapolation/modification to the original work, please use the following BibTeX entry.
git clone https://github.com/CactiLab/code-xNIDS.git

```
@inproceedings{wei2023xnids,
 title = {{xNIDS: Explaining Deep Learning-based Network Intrusion Detection Systems for Active Intrusion Responses}},
 author = {Wei, Feng and Li, Hongda and Zhao, Ziming and Hu, Hongxin},
 booktitle = {{USENIX Security}},
 year = {2023},
}

```