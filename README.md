# Cosmic Tension Equation  
### Un modèle universel pour la propagation épidémique  
### A universal model for epidemic propagation  

---

## 🇫🇷 Version française

### 🎯 Vision  
Ce projet explore une idée simple mais puissante : **une seule équation** peut décrire la dynamique de maladies très différentes, de la grippe saisonnière (Influenza) à la pandémie de COVID‑19.  

Notre **fil rouge** :  
- Une **dérive quadratique** \(\mu(t) = at^2 + bt + c\) qui capture la montée et la descente d’une vague.  
- Un **bruit stochastique de type Ornstein‑Uhlenbeck (OU)** qui reproduit la variabilité aléatoire (super‑spreaders, fluctuations de tests, bruit de mesure).  

---

### 🔹 Filter 1 — Ingestion et normalisation  
- **Sources de données** :  
  - *Influenza* : WHO FluNet (`VIW_FNT.csv`)  
  - *COVID‑19* : Our World in Data (`owid-covid-data.csv`)  
- **Étapes** :  
  - Filtrage par pays (ex. Canada).  
  - Normalisation par population (cas pour 100k habitants).  
  - Visualisation côte à côte.  

👉 Résultat : une comparaison directe entre la **grippe saisonnière** (pics réguliers) et la **COVID‑19** (vagues multiples et chaotiques).  

---

### 🔹 Filter 2 — Ajustement et simulation  
- Ajustement d’une **dérive quadratique** sur une vague donnée (ex. grippe 2017‑2018, COVID printemps 2020).  
- Simulation d’une trajectoire stochastique avec bruit OU.  
- Comparaison avec les données observées.  

👉 Résultat :  
- La dérive capture la **forme générale** de la vague.  
- Le bruit OU reproduit la **variabilité aléatoire**.  
- Le même modèle fonctionne pour deux maladies très différentes.  

---

### 🔹 Comparaisons (Filter 3, en annexe)  
Pour anticiper les critiques, nous avons testé des benchmarks classiques :  
- **ARIMA** (séries temporelles).  
- **Logistique** (croissance saturée).  
- **SEIR** (modèle compartimental).  

👉 Ces comparaisons sont disponibles en **ressources complémentaires** (notebooks séparés).  
Mais le cœur du projet reste le **fil rouge** : une équation unique, élégante et robuste.  

---

### ✅ Conclusion  
Le **Cosmic Tension Equation** démontre qu’une approche simple, transparente et reproductible peut rivaliser avec des modèles plus lourds.  
- **Filter 1** : ingestion et visualisation.  
- **Filter 2** : ajustement et simulation.  
- **Filter 3 (optionnel)** : comparaison avec les standards.  

Ce projet est une invitation à la **critique ouverte** et à la **collaboration** : le code, les données et les interprétations sont publics, reproductibles et prêts à être enrichis.  

---

## 🇬🇧 English version

### 🎯 Vision  
This project explores a simple yet powerful idea: **a single equation** can describe the dynamics of very different diseases, from seasonal influenza to the COVID‑19 pandemic.  

Our **red thread**:  
- A **quadratic drift** \(\mu(t) = at^2 + bt + c\) capturing the rise and fall of an epidemic wave.  
- A **stochastic Ornstein‑Uhlenbeck (OU) noise** term reproducing random variability (super‑spreaders, testing fluctuations, reporting noise).  

---

### 🔹 Filter 1 — Ingestion and normalization  
- **Data sources**:  
  - *Influenza*: WHO FluNet (`VIW_FNT.csv`)  
  - *COVID‑19*: Our World in Data (`owid-covid-data.csv`)  
- **Steps**:  
  - Filter by country (e.g., Canada).  
  - Normalize by population (cases per 100k inhabitants).  
  - Visualize side by side.  

👉 Result: a direct comparison between **seasonal influenza** (regular peaks) and **COVID‑19** (multiple chaotic waves).  

---

### 🔹 Filter 2 — Fitting and simulation  
- Fit a **quadratic drift** to a given wave (e.g., influenza 2017‑2018, COVID spring 2020).  
- Simulate a stochastic trajectory with OU noise.  
- Compare with observed data.  

👉 Result:  
- The drift captures the **general shape** of the wave.  
- The OU noise reproduces **random variability**.  
- The same model works for two very different diseases.  

---

### 🔹 Comparisons (Filter 3, appendix)  
To anticipate critiques, we tested standard benchmarks:  
- **ARIMA** (time series).  
- **Logistic growth**.  
- **SEIR** (compartmental model).  

👉 These comparisons are available as **complementary resources** (separate notebooks).  
But the main narrative remains the **red thread**: a single, elegant, robust equation.  

---

### ✅ Conclusion  
The **Cosmic Tension Equation** shows that a simple, transparent, and reproducible approach can rival heavier models.  
- **Filter 1**: ingestion and visualization.


---

# Conclusion et perspectives / Conclusion and Perspectives  

---

## 🇫🇷 Version française  

Dans ce travail, nous avons montré qu’une équation unique, composée d’une **dérive quadratique** et d’un **bruit stochastique de type Ornstein‑Uhlenbeck (OU)**, permet de décrire la dynamique de maladies très différentes : la **première vague de COVID‑19 au Canada (2020)** et la **saison de grippe 2017‑2018**.  

Les résultats comparatifs mettent en évidence plusieurs points clés :  
- Sur la COVID‑19, le modèle proposé rivalise avec la **croissance logistique**, un standard classique, avec des performances similaires en termes d’erreur (RMSE/MAE).  
- Sur l’Influenza, le modèle **surpasse nettement la logistique**, qui impose une dynamique en S inadaptée aux épidémies saisonnières.  
- Dans les deux cas, la **dérive quadratique** capture la tendance générale, tandis que le **bruit OU** reproduit la variabilité aléatoire observée dans les données.  

Ces résultats soulignent trois atouts majeurs du modèle :  
1. **Simplicité** — peu de paramètres, calibrage rapide, reproductibilité élevée.  
2. **Universalité** — applicable à des maladies de nature très différente sans modification structurelle.  
3. **Interprétabilité** — chaque terme possède une signification claire (tendance, retour vers la moyenne, bruit).  

### Perspectives  
- **Filter 4** : extension vers des comparaisons multi‑vagues et multi‑pays, afin de tester la robustesse du modèle dans des contextes épidémiologiques variés.  
- **Domaines connexes** : l’approche pourrait être transposée à d’autres systèmes dynamiques soumis à des tensions et fluctuations, tels que la **finance** (cycles de marché), le **climat** (fonte des glaces, anomalies de température), ou encore la **dynamique sociale** (propagation d’idées ou de comportements).  
- **Collaboration ouverte** : le code, les données et les résultats sont mis à disposition pour encourager la critique, la reproduction et l’amélioration collective.  

**Conclusion générale :** En démontrant que le **Cosmic Tension Equation** peut rivaliser avec des modèles établis tout en restant plus souple et universel, nous proposons une nouvelle voie pour la modélisation des phénomènes complexes.  

---

## 🇬🇧 English version  

In this work, we have shown that a single equation, composed of a **quadratic drift** and a **stochastic Ornstein‑Uhlenbeck (OU) noise**, can describe the dynamics of very different diseases: the **first wave of COVID‑19 in Canada (2020)** and the **2017‑2018 influenza season**.  

The comparative results highlight several key points:  
- For COVID‑19, the proposed model competes with **logistic growth**, a classical standard, achieving similar error levels (RMSE/MAE).  
- For influenza, the model **clearly outperforms logistic growth**, which enforces an S‑shaped dynamic unsuited to seasonal epidemics.  
- In both cases, the **quadratic drift** captures the general trend, while the **OU noise** reproduces the random variability observed in the data.  

These results emphasize three major strengths of the model:  
1. **Simplicity** — few parameters, fast calibration, high reproducibility.  
2. **Universality** — applicable to very different diseases without structural changes.  
3. **Interpretability** — each term has a clear meaning (trend, mean reversion, noise).  

### Perspectives  
- **Filter 4**: extend to multi‑wave and multi‑country comparisons to test robustness in diverse epidemiological contexts.  
- **Other domains**: the approach could be applied to other dynamic systems under tension and fluctuation, such as **finance** (market cycles), **climate** (ice melt, temperature anomalies), or **social dynamics** (spread of ideas or behaviors).  
- **Open collaboration**: code, data, and results are shared to encourage critique, reproduction, and collective improvement.  

**General conclusion:** By demonstrating that the **Cosmic Tension Equation** can rival established models while remaining more flexible and universal, we propose a new pathway for modeling complex phenomena.  



This project is an invitation to **open critique** and **collaboration**: the code, data, and interpretations are public, reproducible, and ready to be enriched.  

MIT License
