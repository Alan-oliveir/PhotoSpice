# PhotoSpice

PhotoSpice é uma aplicação que captura um circuito esquemático a partir de uma imagem, gera automaticamente uma netlist no padrão Spice e simula o circuito mostrando ao usuário as tensões nodais ou gráfico de tensão ou corrente dependendo do tipo de simulação e dos componentes presentes no circuito.

## 📋 Sobre o Projeto

Este projeto foi desenvolvido como parte do Projeto Integrado do Departamento de Engenharia Eletrônica (DEL) da Escola Politécnica da UFRJ (2022.1), sob orientação dos professores Casé e Juarez.

### Motivação

Os simuladores SPICE atualmente são ótimas ferramentas ao se trabalhar com eletrônica, no entanto é preciso lidar com interfaces gráficas desses programas que podem não ser padronizadas e dependem do hardware e sistemas onde estão instaladas, o que pode atrasar o processo de simulação como um todo. 

O PhotoSpice busca simplificar o processo de simulação para fins de estudo, permitindo que os usuários tirem uma foto do circuito com um smartphone e enviem para análise imediata. O projeto também teve inspiração em aplicações similares que fazem a solução de equações matemáticas a partir de fotos.

### Vídeo do Projeto  

[PhotoSpice](https://youtu.be/VwTYSiOtutM)

## 🚀 Funcionalidades

- **Captura de imagem**: Use seu smartphone ou upload de arquivo para enviar o esquemático do circuito
- **Processamento automático**: Binarização e identificação de contornos dos componentes
- **Detecção inteligente**: Reconhecimento de componentes, conexões, valores e polaridades
- **Geração de Netlist**: Criação automática de netlist no padrão Spice
- **Simulação interativa**: Possibilidade de correção de parâmetros e seleção do tipo de simulação
- **Visualização de resultados**: Exibição das tensões nodais ou gráficos de tensão/corrente

## 🔌 Componentes Suportados

Atualmente, o sistema suporta os seguintes componentes:

- **Componentes passivos**:
  - Resistor
  - Capacitor
  - Indutor
- **Diodos**
- **Fontes de tensão**:
  - Contínua
  - Alternada

## 💻 Tecnologias Utilizadas

- **Yolo**: Ferramenta de visão computacional para detecção e classificação de objetos em tempo real
- **PySpice**: Interface open source Python com o simulador NGSpice
- **PyTorch**: Framework de aprendizado de máquina
- **Matplotlib**: Biblioteca para visualização dos gráficos da simulação
- **Albumentations**: Ferramenta para data-augmentation das imagens de treinamento
- **Vue.js e Bootstrap**: Frontend
- **Flask**: Backend
- **Outras bibliotecas**: NumPy, OpenCV, pycocotools

## 📝 Como Usar

1. Acesse a aplicação web
2. Selecione uma foto do esquemático do circuito
3. Clique no botão "Analisar"
4. Verifique e corrija (se necessário) os valores detectados na netlist
5. Selecione o tipo de simulação:
   - **Ponto de operação**: Exibe as tensões dos nós
   - **Análise transiente**: Exibe gráficos de tensão nodal ou corrente em componentes
6. Para análise transiente, defina:
   - Tempo inicial
   - Tempo final
   - Passo máximo
   - Componente ou nó para visualização
7. Visualize os resultados da simulação

## 🧠 Redes Neurais

O sistema utiliza três redes neurais treinadas:
- Detecção geral de componentes e conexões
- Identificação de números, unidades e múltiplos
- Identificação das polaridades de determinados componentes

## 🔜 Desenvolvimento Futuro

- Inclusão de mais componentes eletrônicos (transistores bipolares, MOSFETs, amplificadores operacionais)
- Geração de diagrama esquemático com indicação visual das correntes e tensões nos nós

## 👥 Autores

- Alan de Oliveira
- Lucas Tiné
- Matheus Felinto
