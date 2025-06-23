---
layout: default
title: "Week 3"
permalink: /week3/
---

# Day 1
---

## 🧠 Transformer Model Text Analysis

We implemented a transformer-based large language model (LLM) to analyze text and conversational data.  
This project provided hands-on experience with the architecture and inner workings of transformer models,  
while deepening our understanding of how LLMs process, interpret, and generate natural language.

**The goal:**  
To explore how transformer models operate and to gain practical experience in building, training, and applying an LLM to real-world text inputs.

---

### 🔗 Attention Mechanism

The image below shows an attention map, which visualizes how correlated each word is to the others in a sentence.  
This is a core mechanism in transformer models—it allows the model to weigh the importance of each word relative to every other word.

<p align="center">
  <img src="https://github.com/user-attachments/assets/676a431e-04d7-46cd-abc2-f9a86a624e86" alt="Attention Map" width="600">
</p>

---

### 💬 Conversation Summarization

Below is an example of how the model was trained using real conversations.  
It shows how the transformer learns to summarize long text inputs into concise outputs.

<p align="center">
  <img src="https://github.com/user-attachments/assets/b7726e92-bbf8-4500-b049-e0c1c8fbbf41" alt="Conversation Summarization Training" width="900">
</p>

# Day 2
---

## 📊 Pokémon Stat Embedding Visualization

<iframe src="/assets/img/pokemon_plot.html" width="100%" height="600" frameborder="0" style="border: 1px solid #ddd; border-radius: 8px;"></iframe>

### 🧬 About the Plot

We created embeddings for Pokémon based on core stats such as **HP**, **Attack**, **Defense**, and **Speed**. This data was pulled using a public Pokémon API and visualized using a dimensionality reduction technique called **t-SNE**.

Unlike other projection methods that may impose artificial structure, **t-SNE** preserves the local relationships in the data, giving us a more authentic view of how Pokémon compare based on their attributes.

Each point in the plot represents a single Pokémon, and you can hover over each point to view its **types**, **abilities**, and **evolution line**.

# Day 3
---

## 🌐 Pokémon Network Visualizations

---

### 🧬 Evolution Network

<iframe src="/assets/img/pokemon_evo_network_2.html" width="100%" height="600" frameborder="0" style="border: 1px solid #ddd; border-radius: 8px;"></iframe>

- Each **node** represents a Pokémon, and each **edge** represents an evolutionary relationship.
- Nodes are **colored by type** (e.g., Fire, Water, Psychic).
- While visually interesting, this network is relatively **dense and cluttered**, making it difficult to clearly trace evolutionary paths or uncover meaningful structure.

---

### 🏞️ Habitat Network (Community Detection)

<iframe src="/assets/img/pokemon_network.html" width="100%" height="600" frameborder="0" style="border: 1px solid #ddd; border-radius: 8px;"></iframe>

- In this network, each **node** is a Pokémon, and **edges connect Pokémon that share the same habitat** (e.g., Grassland, Urban, Water’s Edge, Cave, Mountain).
- This layout produces much **clearer clusters**, allowing us to identify tight communities of Pokémon that live in similar environments.
- We applied **Louvain community detection**, which groups Pokémon into clusters based on their shared habitats. This highlights how **habitat strongly influences natural groupings** in the Pokémon world.

## 📉 Pokémon t-SNE Plot (Colored by Habitat Communities)

<iframe src="/assets/img/pokemon_tsne_louvain.html" width="100%" height="600" frameborder="0" style="border: 1px solid #ddd; border-radius: 8px;"></iframe>

This t-SNE visualization displays Pokémon as nodes positioned based on their stat-based similarity, with **colors representing their habitats**. Each point is a Pokémon, and nearby points tend to have similar stats like HP, Attack, Defense, and Speed.

### 🌍 Observations

- **Legendary Pokémon** from the `rare` habitat cluster closely and tend to have **higher base stats**, suggesting that stronger Pokémon are often found in less common environments.
- Many **Electric** and **Psychic** type Pokémon appear in **urban areas**, forming a distinct habitat-driven cluster.
- Interestingly, **Pichu** (an Electric type) shows up near **Bug types** like **Weedle** and **Kakuna**, which typically live in forest habitats. This may reflect overlapping stat profiles or evolutionary quirks.
- Aside from a few such cases, there aren’t many strong cross-habitat relationships visible in this embedding.

This visualization offers a high-level view of how Pokémon types and habitats can influence their stat-based groupings.

