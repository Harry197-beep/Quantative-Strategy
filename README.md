# Quantative-Strategy
Sentiment-Volatility Inefficiency Strategy is a quantitative trading strategy built on the hypothesis that market inefficiencies emerge when significant news events generate elevated volatility while trading volume remains relatively low. In these situations, information may not be fully incorporated into prices because market participation is limited, leading to delayed price discovery and exaggerated emotional reactions. The strategy identifies assets experiencing strong sentiment-driven news shocks, unusually high volatility, and below-average volume, then analyzes subsequent price behavior for mean-reversion or momentum opportunities. By focusing on the disconnect between information impact and market participation, the strategy seeks to capture alpha from temporary pricing inefficiencies before the broader market fully reacts.

The core thesis is that volatility alone does not indicate efficient price discovery. When volatility spikes following new information but trading volume remains subdued, the market may lack sufficient participation to accurately process the information. This creates a potential inefficiency where prices overreact, underreact, or adjust slowly. The strategy quantifies sentiment intensity, volatility shocks, and volume anomalies to identify these conditions and systematically exploit the resulting mispricing.

based on the data in equity curve, report, and trade logs span over 2,5 years of data taking 1 trade per week shows a strong edge.


monte carlo system dictated a 
monte_carlo.py
==========================================================
  MONTE CARLO SIMULATION
  10,000 simulations | Starting equity: $10,000
==========================================================
Loaded 120 trades from results/trade_log.csv
Win rate  : 56.7%
Avg win   : $223.45
Avg loss  : $-116.38
Expectancy: $76.19 per trade

Running 10,000 Monte Carlo simulations...
Trades per simulation: 120
Starting equity: $10,000
  Progress: 10%
  Progress: 20%
  Progress: 30%
  Progress: 40%
  Progress: 50%
  Progress: 60%
  Progress: 70%
  Progress: 80%
  Progress: 90%
  Progress: 100%
Simulations complete ✅

══════════════════════════════════════════════════════════
  MONTE CARLO SIMULATION RESULTS
  10,000 simulations | 120 trades each
══════════════════════════════════════════════════════════

  ── RETURN DISTRIBUTION ──────────────────────────────
  Median outcome      : +91.4%
  Mean outcome        : +91.4%
  Best case  (95th)   : +91.4%
  Worst case (5th)    : +91.4%
  Probability profit  : 100.0%

  ── DRAWDOWN RISK ────────────────────────────────────
  Expected max DD     : -5.2%
  Median max DD       : -4.9%
  Worst 5% of cases   : -8.2%
  Worst 1% of cases   : -10.5%

  ── CIRCUIT BREAKER RISK ─────────────────────────────
  Circuit breaker     : 10% drawdown limit
  Probability of hit  : 1.4%
  Assessment          : ✅ LOW RISK — safe to trade

  ── VALUE AT RISK ────────────────────────────────────
  VaR 95% (worst 5%)  : $+9,142.72
  VaR 99% (worst 1%)  : $+9,142.72

══════════════════════════════════════════════════════════
  ✅ VERDICT: Strategy is robust — safe for live trading
══════════════════════════════════════════════════════════


this was very consistent during 3 test using monte carlo using 10.000 diffrent possibilities.
