# Data-to-Text-Generation-Of-Radiology-Reports
Radiology report writing in hospitals is a time-consuming task that also requires experience from the involved radiologists. This paper proposes a D2T NLG model to automatically generate selected sections in radiology reports given a structured input of medical annotations from the public MIMIC-CXR dataset.Our model combines three main inputs: (1) medical annotations extracted by Chexbert model into a structured table. (2) All the information in the report before the required generated section, contain only the tokens in which most information is stored for generating a correct coherent text. (3) Text features controlling the style of the generated report. This model uses T-5 encoder-decoder transformer which trained on 230,000 samples and aims to generate a coherent radiological report. We evaluate the generated reports using word-overlap metrics while also creating a new formula to measure the quality of the model's output. The model achieves Precision of 93.7\% on evaluating the differences between the actual sentences to the generated sentences in the "impression" section in the report which showed that 83.3\% of the generated reports on the test set were expertly written without any mistakes. Moreover, the model does not require a specific vocabulary and can be trained on different datasets without changing the architecture as long as the report contains the common sections.

## Brief summary of the process and experiments

summarization of the process we performed and the key changes we made:

<img src="https://github.com/orsho/Data-to-Text-Generation-Of-Radiology-Reports/blob/main/src/report%20flow.png" width="900" height="300">
