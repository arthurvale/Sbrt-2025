Repositório oficial do artigo "Classificação de Feixes Baseada em Métricas da Rede 5G e Velocidade do Usuário" submetido ao XLIII SBrT 2025.

# **Análise de Seleção de Beamforming a Partir de Métricas da Rede 5G**

- Arthur V. Fonseca, Lucas L. de Oliveira e Álvaro A. M. de Medeiros
- Este projeto implementa uma solução de Machine Learning para otimização de beamforming em redes 5G NR, utilizando dados reais de medição coletados em ambientes urbanos e rodoviários. Nosso objetivo é prever o feixe ótimo (SSBIdx) com base em métricas de qualidade de sinal e velocidade do usuário, garantindo atendimento aos requisitos URLLC (Ultra-Reliable Low-Latency Communications).


# Arquivos

- **Dataset**: https://ieee-dataport.org/documents/large-scale-dataset-4g-nb-iot-and-5g-non-standalone-network-measurements
- **Artigo de origem do conjunto de dados**: https://ieeexplore.ieee.org/document/10239125
- **EDA_Feature_Selection_sbrt_2025.ipynb**: exploração inicial do banco de dados e seleção de atributos relevantes.
- **Agrupamento_sbrt_2025.ipynb**: agrupamento realizado com o intuito de encontrar grupos com velocidades bem definidas.
- **Treinamento_modelos_sbrt_2025.ipynb**: ajsute de hiperparâmetros e treinamento dos melhores modelos para cada cenário.

# Principais Resultado

| Velocidade(Km/h)| Modelo       | Macro-Recall (%) | Tempo Predição (ms) |
|-----------------|--------------|------------------|---------------------|
| 0 ≤ v < 10      | Ensemble     | 93.53 ± 0.02     | 0.035 ± 0.005       |
| 10 ≤ v < 40     | Ensemble     | 93.57 ± 0.03     | 0.185 ± 0.052       |
| v ≥ 40          | Random Forest| 90.85 ± 0.22     | 0.029 ± 0.007       |
