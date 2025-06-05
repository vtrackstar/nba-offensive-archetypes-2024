# nba-offensive-archetypes-2024

## 🏀 NBA Player Archetypes via KMeans Clustering

This project uses unsupervised machine learning to discover **NBA player archetypes** from per-36-minute statistics. By segmenting **starters** and **bench players**, I uncover player roles based on real in-game performance rather than traditional positions or subjective narratives.

## 🔧 Tools & Technologies
- Python
  - `pandas`, `numpy` for data manipulation
  - `nba_api` for live NBA player stats
  - `scikit-learn` for clustering (KMeans, StandardScaler)
  - `matplotlib`, `seaborn` for visualizations
- Jupyter Notebook

## 📈 Key Features Used
- Points per 36 (PTS_per36)
- Assists per 36 (AST_per36)
- Rebounds per 36 (REB_per36)
- 3-Pointers Made per 36 (FG3M_per36)
- Turnovers, Usage Rate Proxy, Efficiency Score (custom metrics)

## 📊 Methodology
1. Pulled 2024-25 season stats using the official **NBA API**.
2. Filtered players into **starters** and **bench players** based on minutes played.
3. Engineered per-36 metrics and custom efficiency formulas.
4. Applied the Elbow Method to choose optimal clusters:
   - `k=4` for starters
   - `k=3` for bench
5. Clustered each group separately and interpreted results using player examples and stat profiles.

## 🧠 Final Player Archetypes

### ⭐ Starters:
| Cluster | Archetype                  | Description                                 |
|---------|----------------------------|---------------------------------------------|
| 0       | Non-Scoring Playmakers     | High assists, lower scoring floor generals   |
| 1       | Elite Scoring Playmakers   | MVP-caliber scorers who can also facilitate |
| 2       | Elite Scoring Rebounders   | Bigs who dominate the paint on both ends     |
| 3       | 3P Range Scorers           | High 3PM players who stretch the floor       |

### 🪑 Bench:
| Cluster | Archetype                | Description                                  |
|---------|--------------------------|----------------------------------------------|
| 0       | Scoring Rebounders       | Energy bigs with strong interior presence    |
| 1       | All-Around Bench Players | Balanced stat lines across scoring/rebounding|
| 2       | Bench Bigs with Range    | Stretch 4/5s who can shoot the 3 ball        |

## 📌 Takeaways
- These clusters offer a data-driven lens to evaluate roles and performance tiers.
- Can help analysts, coaches, and fans understand how players contribute regardless of position.
- Future improvements could include defensive metrics, on/off impact, and shot location data.
