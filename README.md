# Video-Captioning-using-Spatio-temporal-features-and-Gaussian-Attention

Video captioning is a challenging task in the domain of computer vision and natural language processing that aims to automatically generate descriptive textual representations for video content. The incorporation of spatio-temporal features allows the model to capture both spatial information related to individual frames and temporal dynamics across the video sequence. Coupled with the power of attention mechanisms, such as Gaussian Attention, the model can effectively focus on salient regions in the video, further enhancing the quality and relevance of generated captions.

In this project, we explore the application of Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU) networks to video captioning, leveraging spatio-temporal features and Gaussian Attention. We employ the widely used MSVD (Microsoft Research Video Description) dataset, containing a diverse range of videos with corresponding human-generated captions, to train and evaluate our model.

Our objective is to develop a robust and contextually-aware video captioning system that can automatically generate meaningful and accurate descriptions, effectively bridging the gap between visual content and natural language, with potential applications in video indexing, retrieval, and accessibility for visually impaired individuals. Through this project, we aim to contribute to the growing field of video understanding and multimodal AI research, while fostering advancements in human-computer interaction and multimedia analysis.

# For extracting the features
1) Download the original MSVD dataset from [here](https://www.cs.utexas.edu/users/ml/clamp/videoDescription/)
2) For the already extracted features use [this](https://drive.google.com/drive/folders/1qhRJg4d-5bRVM-F_fkoZBmHjSY1fjEBe?usp=sharing)

# Results
After training LSTM and GRU models using spatio-temporal features, the generated weights are utilized to generate captions for input videos.Once the models were trained, they were utilized to generate captions for new, unseen videos. The weights learned during training played a crucial role in determining the attention given to different regions and frames within the videos. By focusing on the most relevant visual cues, the models aimed to generate accurate and descriptive captions. The performance of these models is then evaluated using various metrics mentioned. Among these two approaches, the GAUSSIAN model with GRU (Gated Recurrent Unit) achieved the highest METEOR score of 0.304. Overall, the model utilizing spatio-temporal features with GRU outperformed the model employing LSTMs.

# Evaluation table

| Model         | Bleu_1  | Bleu_2  | Bleu_3  | Bleu_4  | METEOR  | ROUGE_L  | CIDEr  |
|---------------|---------|---------|---------|---------|---------|----------|--------|
| LSTM + GAUSS  | 0.641   | 0.438   | 0.330   | 0.241   | 0.206   | 0.568    | 0.302  |
| GRU + GAUSS   | 0.782   | 0.652   | 0.537   | 0.425   | 0.304   | 0.684    | 0.647  |



