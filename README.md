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
- **Filter 2**: fitting and simulation.  
- **Filter 3 (optional)**: benchmark comparisons.  

This project is an invitation to **open critique** and **collaboration**: the code, data, and interpretations are public, reproducible, and ready to be enriched.  

