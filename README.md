# Factd

Factd is a Multi-Modal Fact-Checking model. Abstract Fake news has always been hard to flag and take down before they make a negative impact.

We propose a new framework leveraging co-attention layers to jointly understand both the modalities and classify given claims into one of five categories -

### TABLE I. DESCRIPTION OF FACTIFY CATEGORIES
| Catgories               | Description 1           | Description 2   |
| -------------           |:-------------:| :-----:|
| Support Multimodal      | Text is supported                                                      |Image is supported |
| Support Text            | Text is supported                                                      |Image is neither supported nor refuted |
| Insufficient Multimodal | Text is neither supported nor refuted but may have something in common |Image is supported|
| Insufficient Text       | Text is neither supported nor refuted but may have something in common |Image is neither supported nor refuted |
| Refute                  | Claim text is fake or fabricated                                       |Claim image is fabricated or fake |


## Dataset

Trained on [Factify Dataset](https://aiisc.ai/defactify/factify.html) with 35k samples.
The dataset contains claims and their respective documents. Each claim has two modalities – text and image

## Method
It employs the Mid-Fusion approach in combination with the [Data-Efficient Image Transformer](https://arxiv.org/abs/2012.12877v2) and [DeBERTa](https://arxiv.org/abs/2006.03654) 
Both these models are optimized for common reasoning task

## Result

### TABLE II. METRICS OF MODEL ON VALIDATION SET
| Catgories               | Precision           | Recall    | F1 Score |
| -------------           |:-------------:| :-----:| :-----------|
| Support Multimodal      |0.56321839 | 0.65333333 | 0.60493827 |
| Support Text            |0.46902655 | 0.35333333 | 0.40304183 | 
| Insufficient Multimodal |0.44886364 | 0.52666667 | 0.48466258 |
| Insufficient Text       |0.49253731 | 0.44       | 0.46478873 |
| Refute                  |0.96078431 | 0.98       | 0.97029703 |

