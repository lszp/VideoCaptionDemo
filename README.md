# Video Captioning Demo

<img src="videos\msrvtt\video7089_temp.gif" style="zoom:150%;" /> 

<center><audio id="audio" controls="" preload="none"> <source id="mp3" src="audio/video7089.mp3"> </audio></center>

| GT Caption:  a black man and a white man on american idol talk to the judges. |
| ------------------------------------------------------------ |
| <b>Generated Caption (Ours)</b>:  a man and a woman are talking on a talk show. |
| <b>Generated Caption (Baseline[1])</b>:  a man is talking about a man. |

<img src="videos\msrvtt\video8834_temp.gif" style="zoom:150%;" /> 

<center><audio id="audio" controls="" preload="none"> <source id="mp3" src="audio/video8834.mp3"> </audio></center>

| GT Caption: a man wearing a red apron eats food out of a bowl in the kitchen. |
| :----------------------------------------------------------- |
| <b>Generated Caption (Ours)</b>: a man in a white shirt is cooking a food in a kitchen. |
| <b>Generated Caption (Baseline[1])</b>: a man in a kitchen is cooking food in a kitchen. |



<img src="videos\msrvtt\video9818_temp.gif" style="zoom:150%;" /> 

<center><audio id="audio" controls="" preload="none"> <source id="mp3" src="audio/video9818.mp3"> </audio></center>

| <b>GT Caption</b>: a woman is applying eye makeup with a black brush. |
| :----------------------------------------------------------- |
| <b>Generated Caption (Ours)</b>: a woman is applying makeup to her eyebrows with a brush. |
| <b>Generated Caption (Baseline[1])</b>: a woman is applying makeup on her face. |



<img src="videos\msrvtt\video9149_temp.gif" style="zoom:150%;" /> 

<center><audio id="audio" controls="" preload="none"> <source id="mp3" src="audio/video9149.mp3"> </audio></center>

| <b>GT Caption</b>: a boy and a girl are singing for a competition. |
| :----------------------------------------------------------- |
| <b>Generated Caption (Ours)</b>: a group of people are singing on stage. |
| <b>Generated Caption (Baseline[1])</b>: a boy is singing on stage. |

# Method

- <b>Baseline[1]</b>

  The method guides the video caption generation with Part-of-Speech (POS) information, based on a gated fusion of multiple representations of input videos .

- <b>Ours</b>

  This method captures video temporal information by using graph convolution network , and puts forward the multi-granularity part-of-speech attention mechanism to compute multi-granularity part-of-speech information; further, this is  the first time to introduce meta learning method training video caption model, making the model to maximize reward while guaranteeing the quality of generated statements.

# Dataset

|      Dataset      | Video Number | train | validation | test |
| :---------------: | :----------: | :---: | :--------: | :--: |
|      MSR-VTT      |    10000     | 6513  |    497     | 2990 |
|       MSVD        |     1970     | 1200  |    100     | 670  |
| Charades Captions |     9223     | 6963  |    500     | 1760 |

# Experimental Results

- <b>MSR-VTT</b>

|       Method       | BLUE4 | METEOR | ROUGE-L | CIDEr |
| :----------------: | :---: | :----: | :-----: | :---: |
| <b>Baseline[1]</b> | 41.3  |  28.7  |  62.1   | 53.4  |
|    <b>Ours</b>     | 45.1  |  28.9  |  63.8   | 54.9  |



# Related Paper

1. B. Wang, L. Ma, W. Zhang and et al. Controllable Video Captioning with POS Sequence Guidance Based on Gated Fusion Network[C]. In Proceedings of the IEEE International Conference on Computer Vision, 2019:2641-2650.