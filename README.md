# Introduction to models

PaddlePaddle provides a rich set of computational units to enable users to adopt a modular approach to solving various learning problems. In this repo, we demonstrate how to use PaddlePaddle to solve common machine learning tasks, providing several different neural network model that anyone can easily learn and use.

## 1. Word Embedding

The word embedding expresses words with a real vector. Each dimension of the vector represents some of the latent grammatical or semantic features of the text and is one of the most successful concepts in the field of natural language processing. The generalized word vector can also be applied to discrete features. The study of word vector is usually an unsupervised learning. Therefore, it is possible to take full advantage of massive unmarked data to capture the relationship between features and to solve the problem of sparse features, missing tag data, and data noise. However, in the common word vector learning method, the last layer of the model often encounters a large-scale classification problem, which is the bottleneck of computing performance.

In the example of word vectors, we show how to use Hierarchical-Sigmoid and Noise Contrastive Estimation (NCE) to accelerate word-vector learning.

- 1.1 [Hsigmoid Accelerated Word Vector Training](https://github.com/PaddlePaddle/models/tree/develop/hsigmoid)
- 1.2 [Noise Contrast Estimation Accelerated Word Vector Training](https://github.com/PaddlePaddle/models/tree/develop/nce_cost)


## 2. Generate text using the recurrent neural network language model

The language model is important in the field of natural language processing. In addition to getting the word vector (a by-product of language model training), it can also help us to generate text. Given a number of words, the language model can help us predict the next most likely word. In the example of using the language model to generate text, we focus on the recurrent neural network language model. We can use the instructions in the document quickly adapt to their training corpus, complete automatic writing poetry, automatic writing prose and other interesting models.

- 2.1 [Generate text using the annotated neural network language model](https://github.com/PaddlePaddle/models/tree/develop/generate_sequence_by_rnn_lm)

## 3. Click-Through Rate prediction
The click-through rate model predicts the probability that a user will click on an ad. This is widely used for advertising technology. Logistic Regression has a good learning performance for large-scale sparse features in the early stages of the development of click-through rate prediction. In recent years, DNN model because of its strong learning ability to gradually take the banner rate of the task of the banner.

In the example of click-through rate estimates, we give the Google's Wide & Deep model. This model combines the advantages of DNN and the applicable logistic regression model for DNN and large-scale sparse features.

- 3.1 [Click-Through Rate Model](https://github.com/PaddlePaddle/models/tree/develop/ctr)

## 4. Text classification

Text classification is one of the most basic tasks in natural language processing. The deep learning method can eliminate the complex feature engineering, and use the original text as input to optimize the classification accuracy.

For text classification, we provide a non-sequential text classification model based on DNN and CNN. (For LSTM-based model, please refer to PaddleBook [Sentiment Analysis](https://github.com/PaddlePaddle/book/blob/develop/06.understand_sentiment/README.cn.md)).

- 4.1 [Sentiment analysis based on DNN / CNN](https://github.com/PaddlePaddle/models/tree/develop/text_classification)

## 5. Learning to rank

Learning to rank (LTR) is one of the core problems in information retrieval and search engine research. Training data is used by a learning algorithm to produce a ranking model which computes the relevance of documents for actual queries.
The depth neural network can be used to model the fractional function to form various LTR models based on depth learning.

The algorithms for learning to rank are usually categorized into three groups by their input representation and the loss function. These are pointwise, pairwise and listwise approaches. Here we demonstrate RankLoss loss function method (pairwise approach), and LambdaRank loss function method (listwise approach). (For Pointwise approaches, please refer to [Recommended System](https://github.com/PaddlePaddle/book/blob/develop/05.recommender_system/README.cn.md)).

- 5.1 [Learning to rank based on Pairwise and Listwise approches](https://github.com/PaddlePaddle/models/tree/develop/ltr)

## 6. Semantic model
The deep structured semantic model uses the DNN model to learn the vector representation of the low latitude in a continuous semantic space, finally models the semantic similarity between the two sentences.

In this example, we demonstrate how to use PaddlePaddle to implement a generic deep structured semantic model to model the semantic similarity between two strings. The model supports different network structures such as CNN (Convolutional Network), FC (Fully Connected Network), RNN (Recurrent Neural Network), and different loss functions such as classification, regression, and sequencing.

- 6.1 [Deep structured semantic model](https://github.com/PaddlePaddle/models/tree/develop/dssm)

## 7. Sequence tagging

Given the input sequence, the sequence tagging model is one of the most basic tasks in the natural language processing by assigning a category tag to each element in the sequence. Recurrent neural network models with Conditional Random Field (CRF) are commonly used for sequence tagging tasks.

In the example of the sequence tagging, we describe how to train an end-to-end sequence tagging model with the Named Entity Recognition (NER) task as an example.

- 7.1 [Name Entity Recognition](https://github.com/PaddlePaddle/models/tree/develop/sequence_tagging_for_ner)

## 8. Sequence to sequence learning

Sequence-to-sequence model has a wide range of applications. This includes machine translation, dialogue system, and parse tree generation.

As an example for sequence-to-sequence learning, we take the machine translation task. We demonstrate the sequence-to-sequence mapping model without attention mechanism, which is the basis for all sequence-to-sequence learning models. We will use scheduled sampling to improve the problem of error accumulation in the RNN model, and machine translation with external memory mechanism.

- 8.1 [Basic Sequence-to-sequence model](https://github.com/PaddlePaddle/models/tree/develop/nmt_without_attention)

## 9. Image classification

For the example of image classification, we show you how to train AlexNet, VGG, GoogLeNet and ResNet models in PaddlePaddle. It also provides a model conversion tool that converts Caffe trained model files into PaddlePaddle model files.

- 9.1 [convert Caffe model file to PaddlePaddle model file](https://github.com/PaddlePaddle/models/tree/develop/image_classification/caffe2paddle)
- 9.2 [AlexNet](https://github.com/PaddlePaddle/models/tree/develop/image_classification)
- 9.3 [VGG](https://github.com/PaddlePaddle/models/tree/develop/image_classification)
- 9.4 [Residual Network](https://github.com/PaddlePaddle/models/tree/develop/image_classification)


## Copyright and License

PaddlePaddle is provided under the [Apache-2.0 license](LICENSE).
