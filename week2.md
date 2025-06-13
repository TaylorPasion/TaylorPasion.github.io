---
layout: default
title: "Week 2"
permalink: /week2/
---

<style>
  .section-highlight {
    background-color: #f0f8ff;
    border-left: 6px solid #42A5F5;
    padding: 12px 20px;
    margin: 20px 0;
    border-radius: 10px;
    font-size: 1.05em;
  }
  blockquote {
    background: #f9f9f9;
    border-left: 6px solid #008AFF;
    padding: 10px 15px;
    font-style: italic;
  }
</style>

## 📊 Week 2: Field Goals vs. Points Scored

In this week’s analysis, we explored the relationship between **Field Goals Attempted (FGA)** and **points scored** using data from the **top 5** and **bottom 5 scoring teams** in the 2022–23 NBA season.

---

### 🔝 Top 5 vs. Bottom 5 Scoring Teams

<div class="section-highlight">
<ul>
  <li>Top 5 scoring teams averaged <strong>90 FG attempts</strong> per game, compared to <strong>87 attempts</strong> for the bottom 5.</li>
  <li>Top 5 teams scored around <strong>118 PPG</strong>, while the bottom 5 averaged <strong>110 PPG</strong>.</li>
  <li>Top 5 teams scored <strong>140+ points in 15 games</strong>, compared to just <strong>3 games</strong> for the bottom 5.</li>
  <li>In those 140+ point games, top 5 teams took <strong>99 shots</strong> on average, while the bottom 5 took <strong>87</strong>.</li>
  <li>The bottom 5 scored <strong>under 100 points in 76 games</strong>, while the top 5 only did so in <strong>20 games</strong>.</li>
  <li>In sub-100 point games, teams attempted just <strong>84 shots</strong> on average.</li>
</ul>
</div>

<p align="center">
  <img src="/assets/img/top5_and_bottom5_scoring_teams.png" alt="Top 5 vs. Bottom 5 Scoring Teams" width="1200" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>

---

### 🔬 Sacramento vs. Miami: High vs. Low Scoring Teams

We zoomed in on the **highest scoring team (Sacramento)** and the **lowest (Miami)** to test how strong the FGA-to-points relationship was using linear regression.

<div class="section-highlight">
<ul>
  <li><strong>Sacramento’s R² = 0.18</strong> — a modest relationship between FGA and points scored.</li>
  <li><strong>Miami’s R² = 0.08</strong> — weaker correlation, suggesting other factors influenced scoring.</li>
</ul>
</div>

<p align="center">
  <img src="/assets/img/highest_lowest_scoring_teams.png" alt="Sacramento vs. Miami FG Analysis" width="1200" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>

---

### 🤔 Questions Raised

<blockquote>
Does a higher number of field goal attempts directly lead to more wins?  
Is scoring inefficiency a **team-level issue** or an **individual player issue**?  
What role do opponents play in limiting team performance?
</blockquote>

---

## 🏀 NBA Playoff Prediction Using Decision Trees

<p align="center">
  <img src="/assets/img/nba_playoffs_dt_new.png" alt="NBA Teams Decision Tree" width="1200" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>   

## 🏆 2022–23 NBA Playoff Status Summary

<style>
  .team-box {
    padding: 15px;
    border-radius: 10px;
    margin: 20px 0;
    font-size: 1.05em;
  }
  .made {
    background-color: #e6f9ec;
    border-left: 6px solid #4CAF50;
  }
  .missed {
    background-color: #fcebea;
    border-left: 6px solid #f44336;
  }
</style>

<div class="team-box made">
  <strong>✅ Teams That Made the Playoffs:</strong><br>
  <code>BKN</code>, <code>BOS</code>, <code>CHI</code>, <code>CLE</code>, <code>DEN</code>, <code>GSW</code>, <code>LAC</code>, <code>LAL</code>, <code>MIA</code>, <code>MIL</code>, <code>MIN</code>, <code>NYK</code>, <code>PHI</code>, <code>PHX</code>, <code>SAC</code>, <code>OKC</code>
</div>

<div class="team-box missed">
  <strong>❌ Teams That Did Not Make the Playoffs:</strong><br>
  <code>ATL</code>, <code>MEM</code>, <code>TOR</code>, <code>CHA</code>, <code>DAL</code>, <code>DET</code>, <code>HOU</code>, <code>IND</code>, <code>ORL</code>, <code>POR</code>, <code>SAS</code>, <code>UTA</code>, <code>WAS</code>, <code>NOP</code>
</div>


To explore what factors contributed to NBA teams making the playoffs, we built a **decision tree classifier** using various team statistics such as:

- Plus/Minus
- Points
- Field Goals Attempted (FGA)
- Assists
- Turnovers
- Blocks

---

## 🧠 Principal Component Analysis (PCA)

To better understand the variance across NBA team statistics, we used **Principal Component Analysis (PCA)**. Below are visualizations of the PCA results:

- The **bar plot** shows how much variance each principal component explains.
- The **scatter plot** shows how teams are distributed in PCA space, highlighting clusters and outliers.

<style>
  .pca-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    margin-top: 1em;
  }
  .pca-img {
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    max-width: 100%;
    height: auto;
    width: 48%;
  }
  @media (max-width: 768px) {
    .pca-img {
      width: 100%;
    }
  }
</style>

<div class="pca-container">
  <img src="/assets/img/pca_bar.png" alt="PCA Bar Plot" class="pca-img" />
  <img src="/assets/img/PCA.png" alt="PCA Scatter Plot" class="pca-img" />
</div>


<style>
  .highlight-box {
    background-color: #f0f8ff;
    border-left: 6px solid #42A5F5;
    padding: 16px 20px;
    margin: 20px 0;
    border-radius: 12px;
    font-size: 1.05em;
  }
  .highlight-box ul {
    margin-top: 10px;
    margin-bottom: 10px;
  }
</style>

## 📊 Key Findings

<style>
  .highlight-box {
    background-color: #f0f8ff;
    border-left: 6px solid #42A5F5;
    padding: 16px 20px;
    margin: 20px 0;
    border-radius: 12px;
    font-size: 1.05em;
  }
  .analysis-box {
    background-color: #fffbe7;
    border-left: 6px solid #f9a825;
    padding: 16px 20px;
    margin: 20px 0;
    border-radius: 12px;
    font-size: 1.03em;
  }
  .highlight-box ul {
    margin-top: 10px;
    margin-bottom: 10px;
  }
</style>

<div class="highlight-box">
  We found that three features were particularly predictive of whether a team would make the playoffs:

  <ul>
    <li>🏀 <strong>FGA (Field Goals Attempted)</strong></li>
    <li>🔄 <strong>Rebounds</strong></li>
    <li>🔥 <strong>Points</strong></li>
  </ul>

  These stats played a significant role in determining postseason eligibility and offered insight into both offensive efficiency and defensive strength.
</div>

<div class="analysis-box">
  It’s interesting how <strong>rebounds</strong> and <strong>FGA</strong> are both strong predictors — teams that take more shots naturally generate more rebounding opportunities. <br><br>
  We observed a similar relationship in our <strong>PCA</strong> results:


  
  
  - 📈 <strong>Points</strong> correlate closely with <strong>Assists</strong>
  - 🎯 <strong>Field Goal Percentage</strong> aligns with <strong>3PT FG Percentage</strong>

  Most playoff teams clustered strongly around <strong>PCA Component 1</strong>, suggesting that this component captures the offensive and scoring efficiency that defines postseason success.
</div>

## 🤖 Support Vector Classifier (SVC) Visualization

We applied a **Support Vector Classifier (SVC)** model to evaluate whether team performance metrics could be used to predict playoff qualification. The SVC model works by identifying an optimal boundary that separates teams based on statistical differences.

<p align="center">
  <img src="/assets/img/SVC.png" alt="Support Vector Classifier Plot" width="800" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>

<style>
  .svc-box {
    background-color: #f0f8ff;
    border-left: 6px solid #42A5F5;
    padding: 16px 20px;
    margin: 20px 0;
    border-radius: 12px;
    font-size: 1.03em;
  }
</style>

<div class="svc-box">
  The SVC model was trained using our **PCA-transformed data**, allowing it to find a classification boundary in a reduced feature space. This approach leveraged the variance captured in the PCA components to distinguish between playoff and non-playoff teams.<br><br>
  🔍 The visualization above illustrates how well the classifier separated the two groups — reinforcing trends we saw in both the decision tree and raw PCA results.
</div>
