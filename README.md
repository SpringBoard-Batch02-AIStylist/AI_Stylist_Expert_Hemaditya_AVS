# AI_Stylist_Expert_Hemaditya_AVS

# Introduction

This repository showcases two primary recommendation methods implemented for a retail scenario: Collaborative Filtering and Content-Based Filtering. These methods aim to suggest relevant products to users based on their past behavior and preferences. By the help of  user data and transaction history, we can enhance the shopping experience by providing personalized fashion recommendations.

# Method 1: Collaborative Filtering - Matrix Factorization

Collaborative Filtering relies on user similarity to make predictions. The core idea is that if two users, say A and B, share similar tastes, then items purchased by A are likely to be of interest to B as well, and vice versa. We utilized the training splits for user data and combined them with transaction data within the specified timeframe.

# Matrix Factorization
We create a matrix, A, representing users and the articles they have purchased. This matrix is sparse, as each user typically buys only a small subset of all available articles. To address this, we apply Singular Value Decomposition (SVD) and retain the top 10 singular values to reconstruct matrix A. The resulting matrix provides probabilities indicating how likely user X is to be interested in purchasing an article based on the buying patterns of similar users.

# Method 2: Content-Based Filtering - (K-Means)

Content-based filtering methods use metadata of articles previously purchased by users to recommend similar items. The principle here is that if user A bought article X, they are more likely to be interested in other articles similar to X. For instance, if a user bought a striped shirt, the algorithm will suggest other striped shirts. We merged product data with transaction data within the specified timeframe for this approach.

# Clustering Product Images using K-Means
In our approach, we utilized K-means clustering to group product images into various categories, such as shirts, pants, shoes, etc. By working with image data, this method also considers patterns or designs on products, such as floral or striped designs, clustering them together.


# VGG-16 Architecture

VGG-16 is a convolutional neural network model developed by the Visual Geometry Group (VGG) at the University of Oxford. This model was introduced in the paper "Very Deep Convolutional Networks for Large-Scale Image Recognition" by Simonyan and Zisserman. The VGG-16 model is known for its simplicity and depth, consisting of 16 weight layers.

# Key Characteristics of VGG-16

Architecture: The model consists of 13 convolutional layers and 3 fully connected layers. It uses small 3x3 filters in all convolutional layers, which are stacked one after another.
Depth: VGG-16 is considered a deep network with its 16 layers, allowing it to learn complex features from images.
Activation Function: It uses the Rectified Linear Unit (ReLU) activation function to introduce non-linearity.
Pooling: Max-pooling layers are used to reduce the spatial dimensions of the feature maps.
Pre-trained Model: VGG-16 is often used as a pre-trained model on the ImageNet dataset, which consists of millions of images across a thousand categories. This pre-training helps in feature extraction for various computer vision tasks.
Application in Product Image Clustering
In our approach, we modified the VGG-16 architecture to extract features from product images. The extracted features are then used for clustering similar products together using K-means. This method helps in grouping products not just based on textual metadata but also on visual similarities such as patterns, designs, and colors.

By using the power of VGG-16, we can achieve more accurate and visually coherent clusters of products, enhancing the overall recommendation system.

