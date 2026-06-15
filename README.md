# Financial Volatility Forecasting Using Graph Neural Networks — Master Dissertation

## Abstract

Volatility forecasting is a central challenge in financial modeling, particularly under non-stationary and rapidly evolving market conditions. Existing models often assume feature independence or focus solely on global temporal dynamics, overlooking the complex and transient relationships that emerge across time, features, and assets.

While spectral-based models such as Neural Fourier Machines (NFM) achieve strong performance in multi-hundred-step forecasting horizons, they struggle to accurately capture 22-day volatility, an important monthly-scale horizon in financial time-series applications.

To address this limitation, this dissertation proposes **NFM-GNN**, a hybrid framework that integrates graph-based attention modules with frequency-aware forecasting.

---

## Background

The stock market is one of the most important asset classes in modern finance, offering investors opportunities for higher returns while exposing them to significant uncertainty and risk. Financial markets are inherently complex systems influenced by economic conditions, geopolitical events, investor sentiment, and technological developments.

Volatility forecasting plays a critical role in:

* Portfolio allocation and optimization
* Risk management and hedging
* Derivative pricing
* Regulatory capital planning
* Systemic risk monitoring

The development of **Realized Volatility (RV)** has transformed volatility modeling by enabling market variance to be directly measured from high-frequency financial data. As a result, RV has become a standard benchmark for both academic research and practical financial applications.

Despite decades of research, volatility remains difficult to forecast due to its nonlinear, noisy, and highly dynamic nature. Volatility is also characterized by spillover effects, where shocks originating in one market propagate across regions and asset classes, creating complex dependency structures that conventional forecasting models often fail to capture.

---

## Research Gap

Existing approaches exhibit several limitations:

### Econometric Models

Traditional methods such as:

* ARCH
* GARCH
* EGARCH
* GJR-GARCH
* HAR

provide interpretable volatility forecasts but rely heavily on linearity and stationarity assumptions. Their performance often deteriorates during structural breaks and market regime changes.

### Machine Learning Models

Machine learning approaches such as:

* Random Forest
* XGBoost
* LSTM
* CNN-LSTM
* N-BEATS
* NHITS

improve nonlinear modeling capabilities but generally operate in the time domain and struggle to capture evolving cross-asset dependencies.

### Frequency-Domain Models

Recent spectral forecasting architectures, including:

* FEDformer
* FourierGNN
* Neural Fourier Machines (NFM)

demonstrate strong long-horizon forecasting performance by learning global frequency representations. However, they typically assume independent input features and often underperform on shorter forecasting horizons such as 22-day volatility prediction.

### Graph Neural Networks

Graph Neural Networks (GNNs) effectively model relationships between financial assets through graph structures. Nevertheless, most existing financial GNN frameworks focus solely on cross-asset interactions and neglect:

1. Temporal propagation within individual assets
2. Feature-level interactions
3. Dynamic multi-scale dependencies

As a result, a significant research gap remains between frequency-domain forecasting and structure-aware relational learning.

---

## Proposed Framework: NFM-GNN

To bridge this gap, this dissertation introduces **NFM-GNN**, a hybrid architecture that combines graph-based relational reasoning with frequency-domain forecasting.

The model constructs relational graphs along three complementary dimensions:

### Temporal Graph

Captures volatility propagation and dependency patterns across time.

### Feature Graph

Models interactions among financial indicators within each stock index.

### Spatial Graph

Represents dynamic co-movements and spillover effects among different market indices.

These graph representations are encoded before Fourier-based forecasting, allowing the model to preserve structural information while benefiting from the long-range modeling capabilities of NFM.

---

## Key Contributions

* Identifies a structural limitation in existing frequency-domain volatility forecasting models.
* Proposes **NFM-GNN**, a novel architecture integrating graph-based attention modules with Neural Fourier Machines.
* Introduces temporal, feature, and spatial graph representations for volatility forecasting.
* Combines structure-aware learning with spectral forecasting to improve both short- and long-horizon predictions.
* Demonstrates significant forecasting improvements through extensive empirical evaluation.

---

## Results

Experiments conducted on eight representative stock market indices show that NFM-GNN consistently improves 22-step-ahead volatility forecasting performance.

The model is further validated through:

* Ablation Studies
* Model Confidence Set (MCS) Analysis
* Diebold–Mariano (DM) Statistical Tests

Results demonstrate that graph-enhanced spectral forecasting effectively captures both cyclical market behavior and dynamic relational dependencies.

---

## Thesis Structure

* **Chapter 1:** Introduction
* **Chapter 2:** Literature Review
* **Chapter 3:** Research Questions
* **Chapter 4:** NFM-GNN Framework
* **Chapter 5:** Data and Preprocessing
* **Chapter 6:** Experimental Results and Evaluation
* **Chapter 7:** Conclusion and Future Research
