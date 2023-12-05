# 2048-AI

In this project, three students and I train a Deep Q-learning model to learn the game of 2048. A convolutional neural network is used to approximate the optimal policies at every state. Our agent also utilizes the epsilon-greedy approach to balance exploration and exploitation throughout the training.

After training for 10,000 games, our model learns the game effectively. When compared to a baseline agent that chooses a random action every time, our model performs 4 times better after the training. The plot of the average scores versus the number of games trained follows a linear path. Linear regression gives us a line of best fit, and under the assumption that the linear pattern holds, the model would be 35 times better than the baseline agent after 100K iterations and 69 times better after 200K iterations.

We also tested 3 variations of the game 2048, training the model on each modified game to compare its performance and analyze its adaptation abilities. The first variation was a 5x5 board, as opposed to the original 4x4. Through only 1,000 iterations, our model performed 3.5 times better than a baseline model, compared to the model from the original game scoring 1.2 times better after 1,000 iterations. The improved learning is most likely due to the increase in dimensions for the CNN and longer gameplay (harder to fill up all spots and lose). The next variation is a game with no randomness (i.e, after every swipe, a 2-tile spawns in a similar logic every time). After 10,000 iterations, the model performs 6 times better than a random movement player. The last variation is a game with a block, which cannot be combined with any other tile. After 10,000 iterations, hte model only scores 2.4 times better than a baseline agent. This is because the CNN does not understand how to assess our implementation of a block.

More details about our model and results can be found on the pdf report.

This repository has 4 files, each representing a game variation. Majority of the modeling code is the same across all files.
