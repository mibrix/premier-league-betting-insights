# Premier League Betting Insights

This project explores the profitability of a betting strategy that fades (bets against) specific Premier League teams throughout a season. The analysis demonstrates that such a strategy, especially when targeting teams likely to be relegated, can yield consistent profits. It also introduces a simple rookie-team-based betting approach and provides visualizations of returns based on final league rankings.

## Objective

The goal of this project is to investigate whether there are inefficiencies in bookmaker odds — specifically, whether consistently betting against certain Premier League teams can result in profitable outcomes over time.

To evaluate this, I used historical data from [football-data.co.uk](https://www.football-data.co.uk/englandm.php), covering Premier League seasons from 2010/11 to 2023/24.

## Profitability by Final League Rank

The analysis uses odds from Bet365 (patterns are similar across most bookmakers). The following graph shows the probability of ending a season in profit by betting on the **loss** of the same team in every match:

![Probability of Profit](exploratory_analysis/graphs/probability_of_profit_B365.png)

**Interpretation:**  
- Betting against the team that finishes **last (20th)** results in profit 100% of the time.  
- Teams finishing **18th or 19th** yield a profit around 80% of the time.

## Average Profit by Final League Rank

The graph below shows the **average return** from betting against teams based on their final league position:

![Average Profit](exploratory_analysis/graphs/average_profit_B365.png)

**Key insights:**  
- Betting against relegated teams (positions 18th–20th) results in average returns of **400% to 800%** per season.  
- Over 14 seasons, the **average return** when betting against a relegated team is **511.71%**.

**Example:**  
If someone bet €100 on each match against a team that eventually got relegated, they would expect to earn approximately **€511.71** in profit by the end of the season.

## Theoretical Implications

This consistent profitability suggests that bookmakers **underestimate the probability of relegation-prone teams losing**. In a properly efficient market, such a strategy would not produce long-term profits. According to the Central Limit Theorem, the presence of sustained gains indicates a systematic inefficiency in the odds.

## Rookie Team Strategy

To explore a simple predictive approach, I implemented a naive strategy:  
> **Each season, bet against the newly promoted (rookie) teams.**

While more volatile, the following graph shows the performance of this approach:

![Rookie Strategy](exploratory_analysis/graphs/rookie_teams_strategy_B365.png)

- Despite the variance, this strategy has an **expected return of 49.57%** using Bet365 odds.
- However, the high volatility highlights the need for a more sophisticated selection method to reduce risk and improve consistency.

## Real-World Test: Luton Town (2023/24)

During the 2023/24 season, I tested the strategy with a local bookmaker by betting **€1 against Luton Town** in every match.

- **Outcome:** Ended the season with **€2.62**, a **162% profit**.  
- **Result:** Luton Town finished **18th** and were relegated.

## Summary

- Betting against relegation-bound teams in the Premier League can be highly profitable.
- Bookmakers appear to systematically misprice odds for weaker teams.
- Even a basic strategy (like targeting rookie teams) can be profitable, though more intelligent models are needed to reduce volatility.

## Data Source

- [football-data.co.uk](https://www.football-data.co.uk/englandm.php)  
- Seasons: 2010/11 – 2023/24

---

Suggestions and ideas for refining the selection strategy are welcome.
