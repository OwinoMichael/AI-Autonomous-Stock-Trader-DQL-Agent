# AI-Autonomous-Stock-Trader-DQL-Agent

# Deep Q-Learning for Stock Trading

This repository contains an implementation of Deep Q-Learning (DQL) for automated stock trading. The model was trained and evaluated on seven major technology stocks and demonstrated significant outperformance compared to market benchmarks.

## Overview

This project applies reinforcement learning techniques to the domain of algorithmic trading. Using a Deep Q-Network (DQN), the system learns to make optimal trading decisions (buy, sell, hold) based on historical price data and technical indicators.

## Performance Highlights

- **Average Return**: 45.07% across seven technology stocks
- **Benchmark Comparison**: Outperformed S&P 500 benchmark (~10%) by approximately 35%
- **Best Performance**: 85.24% return on NFLX
- **Risk-Adjusted Performance**: Sharpe ratio of 1.0222 for AAPL with annualized volatility of 17.83%

## Stocks Analyzed

- Apple (AAPL)
- Microsoft (MSFT)
- Google (GOOGL)
- Amazon (AMZN)
- Facebook (FB)
- Netflix (NFLX)
- Adobe (ADBE)

## Features

- State representation using technical indicators
- Experience replay for stable learning
- Epsilon-greedy exploration strategy
- Customizable reward function based on portfolio value

## Requirements

```
python>=3.6
tensorflow>=2.0
pandas
numpy
matplotlib
yfinance
scikit-learn
gym
```

## Usage

1. Clone the repository:
```bash
git clone https://github.com/yourusername/dql-stock-trading.git
cd dql-stock-trading
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run training:
```bash
python train.py --stock AAPL --start_date 2016-01-01 --end_date 2017-02-07
```

4. Test the model:
```bash
python test.py --stock AAPL --start_date 2017-02-08 --end_date 2018-02-07
```

## Project Structure

```
├── data/                  # Data directory
├── models/                # Saved model weights
├── results/               # Performance results and visualizations
├── src/
│   ├── agent.py           # DQN agent implementation
│   ├── environment.py     # Trading environment
│   ├── models.py          # Neural network architectures
│   ├── data_utils.py      # Data processing utilities
│   ├── indicators.py      # Technical indicators
│   └── visualization.py   # Performance visualization tools
├── train.py               # Training script
├── test.py                # Testing script
├── requirements.txt       # Dependencies
└── README.md              # This file
```

## Results

The DQL model achieved significant positive returns across all tested stocks, with individual returns ranging from 18.10% (AAPL) to 85.24% (NFLX). While the model slightly underperformed compared to a stock-specific buy-and-hold strategy (-4.21% on average), it substantially outperformed the broader market index.

## Limitations and Future Work

Current limitations include:
- Strong bias toward holding positions
- Limited exploration during training
- Absence of transaction costs in the model

Future work will focus on:
- Incorporating LSTM networks to better capture temporal dependencies
- Including transaction costs for more realistic evaluation
- Improving the exploration-exploitation trade-off
- Implementing portfolio optimization across multiple stocks
- Enhancing the reward function design

## License

MIT

## Citation

If you use this code in your research, please cite:
```
@article{yourlastname2025dql,
  title={Deep Q-Learning for Automated Stock Trading},
  author={Your Name},
  year={2025}
}
```
