# noswar
NHL Betting Odds Module (In Progress)
🏒 NHL Game Outcome Prediction Model
Overview

This project builds a data-driven model to simulate and predict NHL game outcomes using team offensive and defensive metrics. The goal is to estimate win probabilities, projected goal totals, and likely scorelines using statistical modeling and Monte Carlo simulation.

The model combines historical performance metrics with probabilistic simulations to better understand how teams match up in a given game.

This project is part of my sports analytics portfolio, focusing on applying data science and statistical modeling to hockey.

Project Goals

Build a predictive framework for NHL games

Estimate expected goals for each team

Simulate games using Monte Carlo simulation

Generate probabilities for:

Win/Loss outcomes

Over/Under totals

Most likely scorelines

Develop a repeatable workflow using public sports data

Model Methodology
1. Team Strength Modeling

Each team is assigned offensive and defensive strength ratings based on historical performance data.

Metrics include:

Goals scored

Goals allowed

Home vs away performance

League averages

Expected goals are estimated using a Poisson-based framework:

𝜆
𝑡
𝑒
𝑎
𝑚
=
Offensive Strength
×
Opponent Defensive Weakness
×
League Avg Goals
λ
team
	​

=Offensive Strength×Opponent Defensive Weakness×League Avg Goals

Where:

λ_home = expected home goals

λ_away = expected away goals

2. Monte Carlo Simulation

Using the expected goal values, the game is simulated thousands of times.

Example:

λ_home = 2.77
λ_away = 2.61

Each simulation generates a random score based on the Poisson distribution.

The results estimate:

Win probabilities

Total goal distributions

Scoreline likelihoods

Example output:

P(Home Win): 0.528
P(Over 5.5): 0.455
P(Under 5.5): 0.545
Example Simulation Output

Avalanche @ Red Wings

λ_home = 2.772
λ_away = 2.615

P(home win) = 0.528

Over/Under Probabilities
Over 5.5 = 45.5%
Under 5.5 = 54.5%

Over 6.5 = 29.8%
Under 6.5 = 70.2%

Most likely scorelines:

Home Goals	Away Goals	Probability
2	2	5.9%
3	2	5.5%
2	3	5.2%
3	3	4.9%
2	1	4.7%
Tech Stack

Languages and tools used in this project:

Python

Pandas – data manipulation

NumPy – statistical simulation

SQL – structured sports data storage

NHL Public API – data sourcing

Tableau – data visualization

Data Sources

Primary data is collected from:

NHL Public API

Historical game results

Team statistics datasets

These sources allow automated retrieval of:

Game schedules

Team statistics

Player statistics

Game results

Current Features

Expected goals model

Monte Carlo game simulation

Win probability calculation

Over/Under projections

Scoreline probability distributions

Future Improvements

Planned upgrades include:

Player-level impact modeling

Goalie-adjusted expected goals

Shot-based metrics (xG models)

Lineup adjustments

Betting market comparison

Model backtesting

Example Workflow

Pull team statistics from NHL API

Calculate offensive and defensive strengths

Estimate expected goals for each team

Run 10,000+ simulations

Output probabilities and score distributions

Why This Project

Sports organizations increasingly rely on data-driven decision making for:

Player evaluation

Game strategy

opponent scouting

predictive modeling

This project demonstrates how statistical modeling and simulation techniques can be applied to real-world sports analytics problems.

Author

Ethan Rawson

Florida State University
Sports Analytics | Data Analytics | Hockey Analytics

LinkedIn:
www.linkedin.com/in/ethan-rawson
