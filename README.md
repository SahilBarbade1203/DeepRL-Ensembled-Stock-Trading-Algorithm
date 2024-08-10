## DeepRL-Ensembled-Stock-Trading-Algorithm
FinSearch Research Competition

This repository contains the code and resources for implementing a Deep Reinforcement Learning (RL) based stock trading strategy using ensemble methods. The project involves training multiple RL agents—DQN, DDQN, and DDPG—on Nifty50 stock data from 2010 to 2019, and then ensembling their predictions to generate robust trading signals.

## Repository Structure

- **Nifty50_data/**: Contains the stock data for Nifty50 from 2010 to 2019.
- **RL_Models_Weights/**: Stores the trained weights for the DQN, DDQN, and DDPG models.
- **Results & Plots/**: Includes the results and plots generated during testing and evaluation.
- **DDPG_Agent.py**: Implementation of the Deep Deterministic Policy Gradient (DDPG) agent.
- **DDQN_Agent.py**: Implementation of the Double Deep Q-Network (DDQN) agent.
- **DQN_Agent.py**: Implementation of the Deep Q-Network (DQN) agent.
- **Ensemble_Pipeline.py**: Script to ensemble the outputs of the DQN, DDQN, and DDPG agents.
- **Final_Script.ipynb**: A Jupyter Notebook that brings everything together, from data preprocessing to final results.
- **requirements.txt**: List of Python dependencies required to run the project.
- **train.py**: Script to train the RL models.
- **test.py**: Script to test the trained RL models.
- **utils.py**: Utility functions used throughout the project.

## Project Overview

### Objective
The primary objective of this project is to develop an ensemble-based stock trading strategy using deep reinforcement learning. By combining the strengths of multiple RL agents, the ensemble model aims to improve the robustness and accuracy of trading signals.

### Methodology

1. **Data Preprocessing**:
    - Historical stock prices for Nifty50 from 2010 to 2019 are preprocessed and used as the input for the RL models.

2. **Model Training**:
    - Three RL agents (DQN, DDQN, and DDPG) are trained separately on the processed data.
    - Each model learns to predict actions (buy, sell, hold) based on the stock prices.

3. **Ensembling**:
    - The predictions from the three models are combined using a majority voting mechanism.
    - The final trading action is determined by the ensemble, which helps in reducing the risk of wrong predictions by individual models.

4. **Evaluation**:
    - The performance of the ensemble model is evaluated using key metrics such as cumulative returns, Sharpe ratio, and maximum drawdown.
    - Plots and results are generated to visualize the model's performance.

### Key Features
- **Multi-Agent RL**: Combines the strengths of DQN, DDQN, and DDPG for better decision-making.
- **Ensemble Learning**: Uses majority voting to enhance the robustness of trading signals.
- **Comprehensive Evaluation**: Provides detailed analysis through results and plots.

## Installation

To install the required dependencies, run:

```bash
pip install -r requirements.txt

```
## Usage

### Train the Models:
- Run `train.py` to train the DQN, DDQN, and DDPG models.
- The trained weights will be saved in the `RL_Models_Weights/` directory.

### Test the Models:
- Run `test.py` to evaluate the performance of the trained models.

### Ensemble and Evaluate:
- Use `Ensemble_Pipeline.py` to ensemble the predictions from the models and generate the final trading signals.
- Visualize the results using `Final_Script.ipynb`.

## Results

The ensemble model's performance is evaluated on the Nifty50 stock data, showing promising results in terms of cumulative returns, risk-adjusted returns, and overall trading strategy robustness.

### Example Plots
![Cumulative Returns](Results%20&%20Plots/DDPG_Results/DDPG_training_plots_1.png)
![Sharpe Ratio](Results%20&%20Plots/sharpe_ratio.png)

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For any questions or inquiries, please contact [Sahil Dhanraj Barbade](mailto:sahilbarbade1203@gmail.com).
