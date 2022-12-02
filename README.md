# Factd

Factd is a Multi-Modal Fact-Checking model. Abstract Fake news has always been hard to flag and take down before they make a negative impact.

We propose a new framework leveraging co-attention layers to jointly understand both the modalities and classify given claims into one of five categories -

# Dataset 

Trained on [Factify Dataset](https://aiisc.ai/defactify/factify.html) with 35k samples.
The dataset contains claims and their respective documents. Each claim has two modalities – text and image

# Method
It employs the Mid-Fusion approach in combination with the [Data-Efficient Image Transformer](https://arxiv.org/abs/2012.12877v2) and [DeBERTa](https://arxiv.org/abs/2006.03654)


![My Remote Image](https://www.dropbox.com/s/.../my-remote-image.jpg?dl=0)

Both these models are optimized for common reasoning task
