##  Probability Density Function using Non-Linear Model

This project demonstrates how to learn a probability density function after applying a roll-number-based non-linear transformation to NO2 air quality data.

---

##  Methodology

Data Loading → Column Selection → Non-Linear Transformation → Parameter Estimation → Display Results

---

##  Dataset

- File: data.csv  
- Feature Used: no2  

The dataset contains air quality measurements. Only the NO2 column is used for this experiment.

---

##  Data Transformation

Each NO2 value x is transformed into z using:

z = x + ar * sin(br * x)

where:

- ar = 0.05 * (r mod 7)  
- br = 0.3 * ((r mod 5) + 1)  
- r is the university roll number  

This step introduces roll-number-based non-linearity into the data.

---

##  Probability Density Function

After transformation, the following model is assumed:

p(z) = c * exp(-lambda * (z - mu)^2)

Where:

- lambda controls the spread  
- mu represents the mean  
- c is a scaling constant  

The parameters lambda, mu, and c are learned using Maximum Likelihood Estimation by minimizing the negative log-likelihood with numerical optimization.

---

##  Results
<img width="971" height="60" alt="image" src="https://github.com/user-attachments/assets/9ee25b05-0e8d-45ec-94c7-3940177cb21a" />


