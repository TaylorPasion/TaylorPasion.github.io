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
  <img src="/assets/img/top5_and_bottom5_scoring_teams.png" alt="Top 5 vs. Bottom 5 Scoring Teams" width="600" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
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
  <img src="/assets/img/highest_lowest_scoring_teams.png" alt="Sacramento vs. Miami FG Analysis" width="600" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);" />
</p>

---

### 🤔 Questions Raised

<blockquote>
Does a higher number of field goal attempts directly lead to more wins?  
Is scoring inefficiency a **team-level issue** or an **individual player issue**?  
What role do opponents play in limiting team performance?
</blockquote>

---
