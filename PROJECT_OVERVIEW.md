# 🧪 Experimental Protocol — Epidemic Propagation with the Cosmic Tension Equation

## 1. 🎯 Scientific Rationale
Epidemics are complex dynamical systems that combine:
- **Deterministic trends** (growth and decline of cases).  
- **Stochastic variability** (super-spreader events, local outbreaks, reporting noise).  

Traditional models:  
- **SEIR models**: structured but deterministic.  
- **Agent-based models**: detailed but computationally heavy.  

The **Cosmic Tension Equation (Quadratic Ornstein–Uhlenbeck process)** offers a **lightweight, interpretable alternative**:  
- Drift = epidemic wave shape (quadratic trend).  
- Noise = random fluctuations.  
- Threshold = epidemic peak or hospital capacity.  

---

## 2. 📊 Datasets

### Seasonal Influenza
- **WHO FluNet**: [https://www.who.int/tools/flunet](https://www.who.int/tools/flunet)  
  - Weekly influenza cases by country, since 1995.  
- **CDC FluView (US)**: [https://gis.cdc.gov/grasp/fluview/](https://gis.cdc.gov/grasp/fluview/)  
  - Weekly influenza-like illness (ILI) data.  

### COVID-19
- **Johns Hopkins CSSE COVID-19 Dataset**: [https://github.com/CSSEGISandData/COVID-19](https://github.com/CSSEGISandData/COVID-19)  
  - Daily confirmed cases and deaths, global coverage.  
- **Our World in Data (OWID)**: [https://ourworldindata.org/coronavirus](https://ourworldindata.org/coronavirus)  
  - Cases, deaths, vaccinations, testing.  

---

## 3. 🔬 Model Formulation

Quadratic OU equation:

\[
d\phi_t = -\gamma \, (\phi_t - \mu(t)) \, dt + \sqrt{2D}\, dW_t
\]

with

\[
\mu(t) = a t^2 + b t + c
\]

- \(\phi_t\): normalized epidemic intensity (cases/population).  
- \(\mu(t)\): quadratic drift (epidemic wave).  
- \(\gamma\): mean reversion speed.  
- \(D\): stochastic variance.  
- \(W_t\): Wiener process (Gaussian noise).  

---

## 4. 🧪 Validation Filters

### Filter 1 — Data ingestion & normalization
- Import WHO FluNet (weekly) and JHU COVID-19 (daily).  
- Normalize by population.  
- For influenza: baseline = average of 2010–2019.  
- For COVID-19: baseline = pre-epidemic period (Jan–Feb 2020).  

### Filter 2 — Internal consistency
- Compare deterministic drift vs stochastic ensemble.  
- Check if OU captures both epidemic curve and variability.  

### Filter 3 — Advanced validation
- **Benchmarks:**  
  - SEIR (deterministic).  
  - Logistic growth.  
  - ARIMA (time series).  
- **Out-of-sample:** Train on first half of epidemic wave, test on second half.  
- **Sensitivity:** γ and D grid search → distribution of epidemic peaks.  
- **Robustness:** Compare across countries (e.g., US vs Spain vs Japan).  
- **Reproducibility:** Export epidemic peaks and thresholds to CSV.  

---

## 5. ⚖️ Benchmark Comparisons
- **SEIR model**: baseline epidemiological framework.  
- **Logistic growth**: simple epidemic curve.  
- **ARIMA**: statistical time series benchmark.  
- **Quadratic OU**: interpretable hybrid capturing both drift + noise.  

---

## 6. 🔁 Reproducibility Guidelines
- Provide **Jupyter/Colab notebooks** for each filter.  
- Export results to `results/` folder:  
  - `epidemic_peaks.csv` (predicted vs observed).  
  - `sensitivity_heatmap.png`.  
- Document every step in `docs/overview.md`.  
- Use `CHANGELOG.md` to log updates (new datasets, new filters).  

---

## 7. 📚 References
- Korzin & Leonenko (2025). *Lightweight Models for Influenza and COVID-19 Prediction*. MDPI Mathematics.  
- Andreu-Vilarroig et al. (2025). *Mathematical Modeling of Influenza Dynamics: Integrating Seasonality and Waning Immunity*. Bulletin of Mathematical Biology.  
- WHO FluNet — Global influenza surveillance.  
- Johns Hopkins CSSE COVID-19 Dataset — Global COVID-19 data.  

---

## 8. ✅ Expected Outcomes
- Demonstrate that the **Cosmic Tension Equation** reproduces epidemic dynamics across **two very different diseases** (seasonal influenza and COVID-19).  
- Show robustness across **time scales** (weekly vs daily) and **geographies**.  
- Provide reproducible outputs (CSV, figures) for epidemic peaks and thresholds.  
- Strengthen credibility by connecting to **public health datasets** and **peer-reviewed epidemic modeling literature**.  
