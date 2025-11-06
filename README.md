# Temp-Logistics

Temp-Logistics benchmarks Random Forest, LSTM and GRU models to forecast future temperature trends using historical Detroit weather data (2014–2023). The goal is to understand how classical ML vs deep learning models perform in a real time-series forecasting scenario and how temperature prediction can support logistics, planning and supply chain decisions.

## Models Compared
- Random Forest (baseline classical ML)
- LSTM (deep learning)
- GRU (deep learning)


## Dataset

This project uses historical daily weather data for Detroit (USA) between 2014–2023.

**Source (Raw):**  
NOAA National Weather Service Climate Data Archive:  https://www.ncei.noaa.gov/

## Repository Structure
```
Temp-Logistics/
│
├── Dataprocessing.ipynb
├── Rf&LSTM_model.ipynb
├── GRU_model.ipynb
├── requirements.txt
└── README.md
```
## Results Summary

| Model | Performance Summary |
|--------|---------------------|
| Random Forest | Performed well on short horizon prediction but struggled capturing longer sequential seasonal pattern. |
| LSTM | More stable forecasting compared to RF. Performed better when future horizon increased but took longer training time. |
| GRU | Provided the most balanced performance, lower MSE overall, and trained faster than LSTM. GRU was the best performing approach among all three models in this benchmark. |

**Conclusion:**  
GRU was the most efficient + accurate model for this dataset and forecasting horizon. LSTM was second best and Random Forest was the weakest performer in long horizon forecasting.

