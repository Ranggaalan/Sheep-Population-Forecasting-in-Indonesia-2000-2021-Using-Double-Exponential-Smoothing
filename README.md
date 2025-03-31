# Sheep-Population-Forecasting-in-Indonesia-2000-2021-Using-Double-Exponential-Smoothing
A data science project analyzing and forecasting Indonesia's sheep population (2000–2021) using Double Exponential Smoothing. With a low MAPE of 7.39%, it accurately captures population trends across 34 provinces.

# Sheep Population Forecasting in Indonesia (2000-2021)

## Project Overview
A comprehensive data science project analyzing and forecasting sheep population across Indonesian provinces using advanced time series forecasting techniques. Utilizing Double Exponential Smoothing algorithm to predict sheep population trends from 2000 to 2021, the project provides precise insights with a low MAPE of 7.39%, successfully capturing the nuanced population dynamics across 34 Indonesian provinces.

## Key Project Highlights
- **Data Period**: 2000-2021
- **Provinces Analyzed**: 34 Indonesian Provinces
- **Forecasting Algorithm**: Double Exponential Smoothing
- **Prediction Accuracy**: 
  - Mean Absolute Error (MAE): 945,631.83
  - Mean Absolute Percentage Error (MAPE): 7.39%

## Data Source
- **Official Source**: Badan Pusat Statistik (BPS) Indonesia
- **Link**: [BPS Sheep Population Statistics](https://www.bps.go.id/id/statistics-table/2/NDczIzI=/populasi-domba-menurut-provinsi.html)

## Methodology

### Exploratory Data Analysis (EDA)
- Comprehensive analysis of sheep population trends
- Province-level and national-level insights
- Visualization of population dynamics

### Forecasting Technique
- **Algorithm**: Double Exponential Smoothing
- Captures trend and level components
- Effective for data with linear trends

## Technical Implementation

```python
# Fungsi double exponential smoothing
def double_exponential_smoothing(data, alpha, beta):
    smoothed = [data[0]]
    trend = [data[1] - data[0]]
    
    for i in range(1, len(data)):
        smoothed.append(alpha * data[i] + (1 - alpha) * (smoothed[i-1] + trend[i-1]))
        trend.append(beta * (smoothed[i] - smoothed[i-1]) + (1 - beta) * trend[i-1])
    
    return smoothed
```

## Model Performance
- **Forecasting Accuracy**:
  - MAE indicates an average prediction error of ~945,632 sheep
  - MAPE suggests a 7.39% deviation from actual values
- **Interpretation**: Highly accurate forecasting with minimal error margins

## Insights
- Detailed analysis of sheep population dynamics in Indonesia
- Identification of provincial variations
- Trends and growth patterns across different regions

## Technologies Used
- Python
- Pandas
- NumPy
- Statsmodels
- Matplotlib/Seaborn

## EDA dan Result

![Image](https://github.com/user-attachments/assets/7d4b8281-048b-462d-adc4-a87f75cbb395)

![Image](https://github.com/user-attachments/assets/2ce80558-b59d-41d5-b536-f1d5e50420ee)

![Image](https://github.com/user-attachments/assets/4a505923-7f0c-406e-a605-13fc0c1c22a2)


## Future Work
- Incorporate additional economic factors
- Develop more advanced forecasting models
- Extended time series analysis with machine learning techniques

## Conclusion
The project provides a nuanced exploration of sheep population in Indonesia, offering data-driven insights through advanced time series forecasting and comprehensive exploratory analysis.

*"Transforming Agricultural Data into Predictive Insights"*

## Repository Contents
- Data preprocessing scripts
- Exploratory Data Analysis (EDA) notebooks
- Forecasting models
- Visualization scripts
- Detailed analysis reports
