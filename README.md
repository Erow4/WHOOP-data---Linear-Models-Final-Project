# Impact of Sleep and Training Intensity on Recovery and the Subsequent Day Strain 
*Stat139: Linear Models, Final Project*

## 📌 Overview  
This project investigates the relationship between **exercise intensity**, **sleep quality**, and **recovery patterns** using WHOOP data. By combining workout and sleep data, we explore whether physical activity during the day can predict the ratio of **deep (SWS) sleep** to total sleep, and whether exercise metrics can help classify days into *good* vs. *poor* sleep quality. Below is a summary of our findings. Please see the .pdf in this repository for our final submission.

## 🗂 Dataset  
Data was collected from WHOOP exports and cleaned into a unified time-series dataset with **33 variables**, including:  
- **Workout metrics**: Duration, energy burned, weighted average HR, HR zones, max HR.  
- **Sleep metrics**: Deep, light, REM, and awake duration; nap count & duration; sleep need & consistency.  
- **Physiological metrics**: Respiratory rate, recovery, resting HR.  

Final dataset structure: one row per day, capturing both workout activity and sleep outcomes.  

## ⚙️ Methods  
We applied both **inference** and **prediction** models:  
- **Inference (GLM & Regression)**: Tested predictors of deep sleep ratio.  
- **Stepwise Selection**: Improved adjusted R² up to **0.419**.  
- **Prediction Models**: Logistic regression, LASSO, k-NN, Random Forest, Gradient Boosted Trees, and SVM to classify sleep as good/bad.  

### Key Findings  
- Light sleep duration, awake duration, and sleep need were strong predictors of deep sleep ratio.  
- The best predictive models achieved **~65% accuracy**, with Gradient Boosted Trees and SVM performing best.  
- Naps and interaction effects (e.g., energy burned × heart rate) showed predictive value.  

## 📊 Results  
- **Baseline GLM**: Adjusted R² = 0.347  
- **Sophisticated Models**: Adjusted R² up to 0.419  
- **Prediction Accuracy**: 60–65% across methods  
- Strongest predictors: Sleep-related variables, with some exercise interactions  
