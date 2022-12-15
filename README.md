# cmpe297 final project
## Building a recommender system using graph neural network
### Team members:  Weifeng Ma,  Aman Shah
</br>
</br>
In this project, we'll build a recommender system using different approaches(popular-based approach, collaborative filtering approach, and graph neural network approach). In this popular-based approach, we will filter out data and get the top and most popular items for users. This approach often use to create a top list for users to select items they might like. In collaborative filtering approach, the system will filter out items that a user might like on the basis of reactions by similar users. This approach is often done by using matrix factorization. Matrix factorization is the approach of decomposing a matrix into the product of two or more matrices. Lastly, we can also use a graph neural network to build a recommender system. By using a neural network, we can update/adjust the weights of a matrix from matrix factorization to get an optimal rating for each user. Graph neural networks have an advantage in recommender systems. We can easily represent user-item interaction by using a graph. In this project, we'd try all methods to build our recommender system.  </br>

![image](https://user-images.githubusercontent.com/32551600/206965130-c08d742d-3abb-4d4f-ab8c-1c4834a3116e.png)
The general idea of using graphs as a general network architecture for recommendation systems involves two key steps: graph encoding and bilinear decoding. Graph encoding is the process to convert data to embedding so that the system can use embeddings to calculate similarity among items. Bilinear decoding is used to predict a connection between nodes.; therefore, we perform link/edge prediction on a graph. A link/edge represents a connection between a user and item(s). If we can predict a link, we can perform recommendations to users. This is how a graph neural network works in recommender systems. </br>
The dataset
</br>
![image](https://user-images.githubusercontent.com/32551600/206971731-55c67468-817e-4c05-8aec-68bf36877f84.png)

The dataset we used is the Movielens dataset. The MovieLens datasets are widely used in machine learning. These datasets are a product of member activity in the MovieLens movie recommendation system. Datasets for building a recommender system often contain users' data and items' data. We can merge two datasets to get a user-item interaction dataset. The user-item interaction dataset contains information on users and their preferred items. We can use user-item interaction to create a connection between users and their preferred items. In a graph network, we can see these connections between users and items as a connection between nodes to nodes. 
</br>
![image](https://user-images.githubusercontent.com/32551600/206972619-e0ffe3a2-5c07-425f-b526-b3d15fa6c671.png) </br>
Since the user dataset and item dataset has their own features, each node in a graph would also have features. Each node's features are a message. Every time we forward or receive a message indicates a connection between users to items. Therefore, if we try to find a connection that exists for a user or not, we can perform link prediction. Based on link connections, we can perform recommendations. </br>
</br>
The main purpose of a GNN is to encode. In our project, we use LightGCN. LightGCN is a type of graph convolutional neural network. It is called "light" because it can do anything GCN does but with less time complexity. LightGCN learns user and item embeddings by linearly propagating them on the user-item interaction graph. In this project, we will use LightGCN to do embedding for our user-item interaction data. After applying data into LightGCN, we could get embedding for prediction. </br>

![image](https://user-images.githubusercontent.com/32551600/207019047-3a45112b-4c97-4419-b7b0-6bb92bd46770.png) </br>

$N_u$: the set of all neighbors of user $u$ (items liked by $u$)

$N_i$: the set of all neighbors of item $i$ (users who liked $i$)

$e_u^{(k)}$ : k-th layer user embedding

$e_i^{(k)}$ : k-th layer item embedding
LightGCN uses the above formula for user and item embeddings. It calculate layer combination of embeddings. The layer we selected is 3. In the demonstration, I would explain how it work in detail.
 </br>
 </br>
Full report: https://github.com/cmpe130weifeng/cmpe297_project/blob/main/Dev%26Full%20report.pdf </br>
</br>
Presentation Video link: https://youtu.be/6hYJ3Essu1U </br>
</br>
Colab Link: https://colab.research.google.com/drive/1xBnc36PJ_d82BS01plDYwPomoqQL0ojU#scrollTo=5b7f792e </br>
</br>
Powerpoint Link: https://github.com/cmpe130weifeng/cmpe297_project/blob/main/project%20ppt.pdf </br>
</br>
<br/>
### Team member contribution <br/>
**Weifeng Ma**: GNNs based RSs, documentation, and environment set up <br/>
**Aman Shah**: Popular based RSs, Collaborative filtering RSs <br/>
Works are evenly distributed. Contribution is even. <br/>
</br>
### Reference
Article reference: </br>
[1] Wu, Zonghan, et al, A comprehensive survey on graph neural networks (2020), IEEE transactions on neural networks and learning systems 32.1 (2020): 4–24. </br>
[2] He, Xiangnan, et al. "Lightgcn: Simplifying and powering graph convolution network for recommendation." Proceedings of the 43rd International ACM SIGIR conference on research and development in Information Retrieval. 2020. </br>
[3] LightGCN: https://arxiv.org/abs/2002.02126 </br>
</br>
Image reference: </br>
[1] https://towardsdatascience.com/graph-neural-network-gnn-architectures-for-recommendation-systems-7b9dd0de0856#:~:text=GNNs%20for%20recommendation,-Recommendation%20systems%20are&text=Recommendations%20are%20drawn%20from%20the,item%20past%20interactions. </br>
[2] https://link.springer.com/article/10.1007/s00521-020-05667-z </br>
