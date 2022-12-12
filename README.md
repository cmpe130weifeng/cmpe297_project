# cmpe297 final project
## Building a recommender system using graph neural network
### Team members:  Weifeng Ma,  Aman Shah
</br>
</br>
In this project, we'll build a recommender system using different approaches(popular-based approach, collaborative filtering approach, and graph neural network approach). In this popular-based approach, we will filter out data and get the top and most popular items for users. This approach often use to create a top list for users to select items they might like. In collaborative filtering approach, the system will filter out items that a user might like on the basis of reactions by similar users. This approach is often done by using matrix factorization. Matrix factorization is the approach of decomposing a matrix into the product of two or more matrices. Lastly, we can also use a graph neural network to build a recommender system. By using a neural network, we can update/adjust the weights of a matrix from matrix factorization to get an optimal rating for each user. Graph neural networks have an advantage in recommender systems. We can easily represent user-item interaction by using a graph. In this project, we'd try all methods to build our recommender system.  </br>
![alt text](https://github.com/cmpe130weifeng/cmpe297_project/blob/main/Images/GNN1.png?raw=true)
</br>
The general idea of using graphs as a general network architecture for recommendation systems involves two key steps: graph encoding and bilinear decoding. Graph encoding is the process to convert data to embedding so that the system can use embeddings to calculate similarity among items. Bilinear decoding is used to predict a connection between nodes.; therefore, we perform link/edge prediction on a graph. A link/edge represents a connection between a user and item(s). If we can predict a link, we can perform recommendations to users. This is how a graph neural network works in recommender systems. </br>
</br>
</br>
Colab Link: https://colab.research.google.com/drive/1xBnc36PJ_d82BS01plDYwPomoqQL0ojU#scrollTo=5b7f792e </br>
</br>
Article reference: </br>
[1] Wu, Zonghan, et al, A comprehensive survey on graph neural networks (2020), IEEE transactions on neural networks and learning systems 32.1 (2020): 4–24. </br>
</br>
Image reference: </br>
[1] https://towardsdatascience.com/graph-neural-network-gnn-architectures-for-recommendation-systems-7b9dd0de0856#:~:text=GNNs%20for%20recommendation,-Recommendation%20systems%20are&text=Recommendations%20are%20drawn%20from%20the,item%20past%20interactions.
[2] https://link.springer.com/article/10.1007/s00521-020-05667-z 
