# EANN-KDD18

EANN: Event Adversarial Neural Networks for Multi-Modal Fake News Detection

Fixed some code to get it in working condition.

## Setup

- Create a virtual environment
  `python -m venv .venv`

- Install requirements
  `pip install -r requirements.txt`

  You may need to check PyTorch installation instructions for working with GPU.

- The `src/data` folder has partial data. The README below has the link to the full dataset.

- The `src/EANN.py` file does the training. There are some arguments which control some behaviour.

- I have added the terminal output for a full training run on the full dataset at `src/EANN-Full-Training.txt`

- I have provided a couple of notebooks.
  - `src/PlotMetrics.ipynb` for plotting accuracy and loss.
  - `src/EANN-Testing.ipynb` provides some code for testing and visualizing the results.


This ends the part added by me.
Read below for the original README.

---


[EANN: Event Adversarial Neural Networks for Multi-Modal Fake News Detection](https://dl.acm.org/citation.cfm?id=3219819.3219903)  
 [Yaqing Wang](http://www.acsu.buffalo.edu/~yaqingwa/),
 [Fenglong Ma](http://personal.psu.edu/ffm5105/), 
 [Zhiwei Jin](https://scholar.google.com/citations?user=iv22mK4AAAAJ&hl=zh-CN), 
 [Ye Yuan](https://scholar.google.com/citations?user=97ZPgN4AAAAJ&hl=en&authuser=1), 
 [Guangxu Xun](https://scholar.google.com/citations?user=HhyfdQYAAAAJ&hl=en),
 [Kishlay Jha](http://people.virginia.edu/~kj6ww/),
  [Lu Su](https://cse.buffalo.edu/~lusu/),
 [Jing Gao](https://cse.buffalo.edu/~jing/)
 
 SUNY Buffalo. KDD, 2018.
 
 ## Dataset
 **We recently release a dataset (in Chinese) on fake news from Wechat. The dataset includes news titile, report content, news url and image url. Find more details via 
https://github.com/yaqingwang/WeFEND-AAAI20**
 
 

 
 The data folder contains a subset of weibo dataset for a quick start.  If you are interested in full weibo dataset, you can download it via https://drive.google.com/file/d/14VQ7EWPiFeGzxp3XC2DeEHi-BEisDINn/view?usp=sharing. (Approximately 1.3GB)
 

 
 ## Main Idea
One of the unique challenges for fake news detection on social media is how to identify fake news on  **newly emerged events**. The EANN is desgined to  __extract shared features among all events__ to effectively improve the performance of fake news detection on never-seen events.


## Experiment
Comparision between reduced model (w/o adversarial) and EANN(w adversarial)

<img src="https://github.com/yaqingwang/EANN-KDD18/blob/master/Fig/Accuracy.png" width="300">  <img src="https://github.com/yaqingwang/EANN-KDD18/blob/master/Fig/F1.png" width="300">

The feature representations learned by the proposed model EANN (right) are more discriminable than fake news detection (w/o adv).

<img src="https://github.com/yaqingwang/EANN-KDD18/blob/master/Fig/baseline_tsne.png" width="256">  <img src="https://github.com/yaqingwang/EANN-KDD18/blob/master/Fig/model_tsne.png" width="256">
 
 

 ## Citation
If this code or dataset is useful for your research, please cite our [paper](https://dl.acm.org/citation.cfm?id=3219819.3219903):

```
@inproceedings{wang2018eann,
  title={EANN: Event Adversarial Neural Networks for Multi-Modal Fake News Detection},
  author={Wang, Yaqing and Ma, Fenglong and Jin, Zhiwei and Yuan, Ye and Xun, Guangxu and Jha, Kishlay and Su, Lu and Gao, Jing},
  booktitle={Proceedings of the 24th ACM SIGKDD International Conference on Knowledge Discovery \& Data Mining},
  pages={849--857},
  year={2018},
  organization={ACM}
}
```
