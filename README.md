Data Generation using Modelling and Simulation for Machine Learning
Student Information
Roll Number: 102303950
Objective
The objective of this assignment is to generate a dataset using a simulation-based approach and then apply different machine learning models to analyze the generated data. Instead of using any real-world dataset, a simulation model is used to create synthetic data. This helps in understanding how modelling and simulation can be used when real data is not easily available or is expensive to collect.
Simulation Tool Used
In this assignment, the simulation tool used is SimPy, which is a Python-based discrete-event simulation library. SimPy is commonly used to model systems such as queues, servers, networks, and manufacturing processes. It allows us to simulate real-world processes using events and resources.
Simulation Model Description
A single-server queue system (M/M/1 queue) is modeled using SimPy. In this system, customers arrive randomly at the server, wait in a queue if the server is busy, receive service, and then leave the system. Both the arrival time and service time follow an exponential distribution. The main output of interest from this simulation is the average waiting time of customers in the queue.
Simulation Parameters and Bounds
The simulation uses two main parameters. The arrival rate represents how frequently customers arrive at the system and is varied between 1 and 10. The service rate represents how quickly the server can serve customers and is varied between 5 and 15. The simulation time is fixed at 100 units for each run. These bounds were chosen to represent realistic system behavior.
Data Generation Methodology
Random values for arrival rate and service rate are generated within the specified bounds. These values are passed to the simulation model, which runs for a fixed duration and records the average waiting time of customers. This process is repeated 1000 times, and each simulation run produces one data record. The final dataset consists of the roll number, arrival rate, service rate, and average waiting time. No external dataset is used, as the entire dataset is generated through simulation.
Machine Learning Approach
The generated dataset is used to train machine learning models. This is treated as a regression problem, where the input features are arrival rate and service rate, and the target variable is the average waiting time. The dataset is split into training and testing sets using an 80:20 ratio.
Machine Learning Models Used
Five different machine learning models are used for comparison. These include Linear Regression, Decision Tree Regressor, Random Forest Regressor, Support Vector Regressor, and K-Nearest Neighbors. Each model is trained on the same training data and evaluated on the same test data.
Evaluation Metrics
The models are evaluated using Mean Squared Error (MSE) and R² Score. Mean Squared Error measures the average squared difference between predicted and actual values, while R² Score measures how well the model explains the variance in the data. A lower MSE and a higher R² score indicate better model performance.
Result Table Explanation
The result comparison table displays the performance of all machine learning models using MSE and R² score. Linear Regression performs relatively poorly because the relationship between parameters and waiting time is non-linear. Tree-based models perform better, and among them, Random Forest achieves the best performance due to its ensemble learning capability.
Result Graph Explanation
A bar graph is plotted with machine learning models on the x-axis and R² scores on the y-axis. This graph visually compares the performance of all models. The graph clearly shows that Random Forest has the highest R² score, indicating superior predictive performance compared to other models.
Best Model Identified
Based on the evaluation results, the Random Forest Regressor is identified as the best-performing model. It achieves the highest R² score and the lowest prediction error among all the models considered in this assignment.
Conclusion
This assignment demonstrates how modelling and simulation can be effectively used to generate synthetic data for machine learning applications. The simulation-based dataset successfully captures system behavior, and machine learning models are able to learn meaningful patterns from it. The results show that ensemble models such as Random Forest perform best on simulation-generated data. This approach is especially useful in situations where real-world data is unavailable or difficult to obtain.
