# Video Captioning

MEng Project

##Environment

Python 3.8.5  
Pytorch 1.7.1  
ffmepg (*the third-party library*)

## Usage

Download the demo of the dataset (1k videos), cd to the file `test_videos`:
```
wget --user htlog23 --password fb93dc3b1950d18 -i 1.txt
```

You also can download the full dataset (12TB with 1,330,000 videos):
```
wget --user htlog23 --password fb93dc3b1950d18 -i videolist.txt
```
Download the captions:  
https://www.rocq.inria.fr/cluster-willow/amiech/howto100m/howto100m_captions.zip

Put the zip file at the `./dataset/` and unzip with:
```
unzip -q howto100m_captions.zip $(cat 1.txt)
```
## Training
Run the `main_distributed.py`. 
```
python main_distributed.py
```



## Version Updates
__Feb 5th 2020:__  
1. Re-implement CBT because of no public code provided.  
2. Use the new loss fuction `MILNCELoss`
