# Image Captioning with Visual Attention

 ----------------------

* Details about different runs of the project can be found on [Weights & Biases](https://app.wandb.ai/veb-101/image-captioning-test/overview?workspace=user-veb-101)

* **Final Architecture used:**
  * *Encoder*: InceptionV3
  * *Attention*: Bahdanua's Soft attention
  * *Decoder*: LSTM unit
  * *Embeddings*: Glove Embedding (glove6b300d)

----
* **Some Outputs from the final run**
1) **Real Caption:** <start> a man on snow skis who is performing a jump <end>
**Prediction Caption:** a man flying through the sky <end>
<img src=".\demo%20outputs/1_output.png" alt='Attention Plot' height="500" width="500"/>
<img src=".\demo%20outputs/1png.png" alt='Image' height="300" width="400"/>

2) **Real Caption:** <start> a couple of elephants that are by the pond <end>
**Prediction Caption:** a group of elephants relax along water in a body of water <end>
<img src=".\demo%20outputs/2_output.png" alt='Attention Plot' height="500" width="800"/>
<img src=".\demo%20outputs/2.png" alt='Image' height="325" width="450"/>

----

* **ToDo**
  * [ ] Applying beam Search
  * [x] Applyling LearningRateScheduler
  * [ ] Making an interface
  * [x] Tuning different Hyperparameters

----

* **Comments**:
  * Code for *ExponentialDecay* added but not used in a run as evaluating the run takes a 3 hours on colab.
  * I have added a manual  early stopping and saving weights for each epoch (all.zip)
  * Try decreasing *vocab_size* and increasing number of images used.
  * I couldn't find any resources for dynamically caching images and loading them directly during run time to save storage space. Numpy's **memmap** seems a good starting point.

----

* **References**
  * [x] [CS231n Winter 2016 Recurrent Neural Networks, Image Captioning - YouTube](https://www.youtube.com/watch?v=cO0a0QYmFm8&feature=youtu.be)
  * [x] [paperswithcode - Image Captioning](https://paperswithcode.com/task/image-captioning)
  * [x] [[1502.03044] Show, Attend and Tell: Neural Image Caption Generation with Visual Attention](https://arxiv.org/abs/1502.03044)
  * [x] [Understanding LSTM Networks -- colah's blog](http://colah.github.io/posts/2015-08-Understanding-LSTMs/)
  * [x] [Attention in Neural Networks - YouTube](https://www.youtube.com/watch?v=W2rWgXJBZhU)
  * [x] [Attention? Attention!](https://lilianweng.github.io/lil-log/2018/06/24/attention-attention.html)
  * [x] [Multimodal Deep Learning - Towards Data Science](https://towardsdatascience.com/multimodal-deep-learning-ce7d1d994f4)
  * [x] [Multi-Modal Methods: Image Captioning (From Translation to Attention)](https://medium.com/mlreview/multi-modal-methods-image-captioning-from-translation-to-attention-895b6444256e)
  * [x] [A Comprehensive Study of Deep Learning for Image Captioning](https://www.groundai.com/project/a-comprehensive-study-of-deep-learning-for-image-captioning/1)
  * [x] [Neural Image Caption Generation with Visual Attention (algorithm) | AISC - YouTube](https://www.youtube.com/watch?v=ENVGHs3yw7k)
  * [x] [Image captioning with visual attention  |  TensorFlow Core](https://www.tensorflow.org/tutorials/text/image_captioning)
