# Short-term-Forecasting-of-Load-and-Solar-Energy-in-a-Micro-grid.
Short term forecasting of renewable energy using Stacked LSTM model and Load using SARIMA model and calculating the net value of energy required from grid.
- In micro grid forcasting for load consumption and renewable energy production like solar energy and wind energy is important for calculation of net energy required from grid or surplus energy injected into the grid.
- Net FLow of energy and Information is show in below diagram.
![net_load_flow](smart_grid_diagram.png)

### LSTM(Long Short term memory)
 LSTM is used for forecasting of renewable energy( solar power in our case). 
 - A powerful type of neural network designed to handle sequence dependence is called a recurrent neural network. The Long Short-Term Memory network or LSTM network is a type of recurrent neural network used in deep learning because very large architectures can be successfully trained.
 - LSTM is a special kind of RNN, capable of learning long-term dependencies
 - Finding correlation - correlation heat map is show as below:
 ![Heat Map](correlation.jpeg)
 - Feature selection
 we tried various feature selection methods like - kselect method, grid search etc
 we used selectting parameters with particular correlation value with solar power generation and not including the feature with same correlation value. we have selected feature - POAI (point of array irradiance), GHI(Global horizontal irradiance), Tmpc(temperature in celcus). RH2M(Relative humidity 2m), solar generation.
 
### Net Energy Flow calculation
- Prediction for renewable energy production using stacked LSTM is calculated and Load consumption is calculated using Sarima model.
- Net energy surplus in case of more renewable production or Net energy deficit in case of more load is calculated by substracting two values.
- Energy flow Diagram is show below:
![Net energ flow Diagram](net_load_flow.jpg)

## Error
- percentage error for load prediction is around 4-5 % and percentage error for renewable energy production prediction is around 6-8%.
 
 
 

 
