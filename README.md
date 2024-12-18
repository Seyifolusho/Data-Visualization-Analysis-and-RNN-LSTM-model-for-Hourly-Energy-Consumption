# Hourly Energy Consumption Forecasting Using RNN LSTM 
 

## **Introduction**  
As someone passionate about leveraging data science for impactful solutions, I developed this project to analyze hourly energy consumption data. The goal was to uncover patterns, identify trends, and forecast future energy needs using a Recurrent Neural Network (RNN) with Long Short-Term Memory (LSTM). Energy consumption data plays a critical role in helping utilities and policymakers optimize grid operations, manage costs, and effectively integrate renewable energy sources.  

---

## **Problem Statement**  
Forecasting energy consumption is vital for efficient grid management and planning. Through this project, I aimed to address the following challenges:  
- Understanding historical energy consumption trends.  
- Identifying seasonal patterns and anomalies in energy usage.  
- Building a robust forecasting model capable of predicting future energy needs.  
- Applying clustering techniques to classify and understand different energy consumption behaviors.  

By tackling these challenges, I sought to provide actionable insights that could enhance grid efficiency and inform energy policies.  

---

## **Dataset**  
The analysis was based on the **AEP_hourly.csv** dataset, which contains hourly energy consumption data. Key features include:  
- **Datetime:** Timestamp for each observation.  
- **AEP_MW:** Energy consumption in megawatts (MW).  

This dataset served as the foundation for understanding patterns and building a predictive model.  

---

## **Data Preprocessing**  
Preparing the data for analysis and modeling was a critical step in this project. Key preprocessing tasks included:  

### **Datetime Handling**  
- Converted the "Datetime" column into a proper datetime object.  
- Extracted features such as year, month, day, and hour for granular analysis.  

### **Resampling**  
- Aggregated hourly data into daily averages to analyze broader trends.  

### **Data Splitting**  
- Split the dataset into training and testing sets for model validation.  
- Normalized the data using MinMaxScaler to ensure compatibility with the LSTM model.  

---

## **Exploratory Data Analysis (EDA)**  
EDA was performed to gain deeper insights into energy consumption patterns:  

### **Visualizing Trends**  
- Yearly energy consumption trends revealed distinct seasonal variations, with higher usage during specific months.  
- Distribution plots illustrated the central tendency and variability in energy usage.  

### **Energy vs. Time**  
- Line plots highlighted the relationship between energy usage and time, clearly showing peak and off-peak hours.  

### **Clustering Analysis**  
- Applied K-Means clustering to categorize energy consumption patterns.  
- Identified distinct clusters, offering valuable insights into consumer behaviors.  

---

## **Model Development**  

### **RNN LSTM Architecture**  

#### **Data Preparation**  
- Converted the time series data into a 3D format required for LSTM input.  
- Employed a sliding window approach with a lookback period of 60 time steps to capture temporal dependencies.  

#### **Model Design**  
Built an RNN with the following architecture:  
- LSTM layers with dropout regularization to prevent overfitting.  
- Dense output layer for regression to predict energy consumption.  
- Optimized using the Adam optimizer and Mean Squared Error (MSE) loss function.  

#### **Training**  
- Trained the model for 50 epochs with a batch size of 32.  

### **Prediction and Evaluation**  
- Evaluated the model’s performance on the test dataset.  
- Visualized predicted values against actual observations to assess accuracy.  

---

## **Insights and Findings**  

### **Energy Trends**  
- Clear seasonal trends emerged, with higher energy consumption during winter months due to heating demands.  
- Notable differences were observed between weekday and weekend usage patterns, reflecting shifts in activity levels.  

### **Model Performance**  
- The LSTM model successfully captured temporal patterns in the data, delivering reasonable accuracy in forecasting future energy consumption.  

### **Clustering Results**  
- Clustering analysis identified distinct groups of energy consumption behaviors, enabling targeted energy-saving initiatives.  

---

## **Recommendations**  

### **Policy Recommendations**  
- **Demand-Response Programs:** Implement programs during peak seasons to encourage shifting energy usage to off-peak hours.  
- **Energy Conservation Initiatives:** Tailor conservation campaigns based on high-consumption clusters.  

### **Model Improvement**  
- Combine LSTM with attention mechanisms for enhanced forecasting performance.  
- Incorporate additional features, such as weather data, to improve model accuracy and robustness.  

### **Operational Strategies**  
- Leverage clustering insights to develop customized energy-saving strategies for specific consumer groups.  

---

## **Conclusion**  
This project successfully analyzed hourly energy consumption data and developed a forecasting model using RNN LSTM. By uncovering trends, seasonal patterns, and distinct usage behaviors, the analysis offers valuable insights for energy providers. The recommendations and forecasting capabilities can support more efficient grid operations and long-term planning.  

In future work, I plan to enhance the model further by incorporating external datasets, such as weather and socioeconomic data, and exploring hybrid models to improve predictive accuracy.  

--- 
