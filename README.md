# layoutlm_CORD

# Introduction
This repo is a implementation of the Layoutlm Model, see [1], from the sourcecode (as I didn't manage to make it work with the
huggingface implementation : [HuggingFace Implementation](https://huggingface.co/transformers/model_doc/layoutlm.html) and benchmarked on the CORD Dataset,
see [2].

# Results
I compare the performance of the pre-train LayoutLM on IIT-CDIP dataset (version LARGE)  with the  Bert (version Large).

## Validation Set
Model | F1_Score | Precision | Recall
--- | --- | --- | --- |
LayoutLM Large| **0.9562** |  **0.9577** |  **0.9546** | 
Bert Large | **0.9474** |  **0.9466** |  **0.9481** | 

## Test Set
Model | F1_Score | Precision | Recall
--- | --- | --- | --- |
LayoutLM Large| **0.9843** |  **0.9845** |  **0.9841** | 
Bert Large | **0.9859** |  **0.9861** |  **0.9856** | 

In the validation set, Layoutlm outperformed Bert, but it is not the case in the test set. I need to do more
investigation. \
Nevertheless, it took Bert 11 minutes to finish the training (4 epochs) while Layoutlm needed only 3 minutes.
(same environment, setup ..)

# Important files
I am using the Layoutlm Large, files of the pre-trained model can be found on these links : \
[OneDrive](https://1drv.ms/u/s!ApPZx_TWwibInSy2nj7YabBsTWNa?e=p4LQo1) /
[GoogleDrive](https://drive.google.com/open?id=1tatUuWVuNUxsP02smZCbB5NspyGo7g2g) \
Other ressources can be found on the original repository : [Official Layoutlm](https://github.com/microsoft/unilm/tree/master/layoutlm)

##TODO
I will soon put a script for the training, otherwise you can always check my notebooks. \
I will also give more details about the dataset, the notebook's structure ...
 

##  References
[1] Yiheng Xu and Minghao Li and Lei Cui and Shaohan Huang and Furu Wei and Ming Zhou (2019) ,
    LayoutLM: Pre-training of Text and Layout for Document Image Understanding (https://arxiv.org/abs/1912.13318),
    https://github.com/microsoft/unilm/tree/master/layoutlm
    
[2] Park, Seunghyun and Shin, Seung and Lee, Bado and Lee, Junyeop and Surh, Jaeheung and Seo, Minjoon and Lee, Hwalsuk (2019)
    CORD: A Consolidated Receipt Dataset for Post-OCR Parsing (Document Intelligence Workshop at Neural Information Processing Systems)
    https://github.com/clovaai/cord