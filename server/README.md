# PhotoSpice

An electronic circuit simulator that receives a schematic image as Input for Integrated Project course (EELX00 - Projeto Integrado)

## Configuração do Ambiente

**Importante**: Pode ser necessário executar o comando abaixo no diretório raiz (`../PhotoSpice/`) para permitir que o Python importe corretamente os módulos do PhotoSpice:

```sh
conda develop .
```

## Sobre o Servidor

Este componente é o backend do sistema PhotoSpice, responsável pelo processamento de imagens, detecção de componentes eletrônicos, geração de netlist e simulação de circuitos. O servidor é desenvolvido em Python utilizando o framework Flask.

## Funcionalidades

- Processamento de imagens de circuitos esquemáticos
- Binarização e identificação de contornos para detectar conexões
- Detecção de componentes, conexões, valores e polaridades utilizando redes neurais
- Geração automática de netlist no padrão Spice
- Simulação de circuitos utilizando PySpice (interface para NGSpice)
- API REST para comunicação com a interface web

## Componentes Suportados

Atualmente, o sistema reconhece e simula:

- **Componentes passivos**:
  - Resistor
  - Capacitor
  - Indutor
- **Diodos**
- **Fontes de tensão**:
  - Contínua
  - Alternada

## Tecnologias Utilizadas

- **Flask** - Framework web Python
- **PyTorch** - Framework de aprendizado de máquina para as redes neurais
- **Yolo** - Arquitetura de rede para detecção de componentes e conexões
- **OpenCV** - Processamento e manipulação de imagens
- **PySpice** - Interface Python para o simulador NGSpice
- **Matplotlib** - Geração de gráficos para os resultados da simulação
- **Albumentations** - Data augmentation para treinamento das redes neurais
- **NumPy** - Computação numérica
- **pycocotools** - Ferramentas para manipulação de conjuntos de dados no formato COCO

## Estrutura de Redes Neurais

O sistema utiliza três redes neurais treinadas:
1. Rede para detecção de componentes e conexões (baseada em Yolo)
2. Rede para reconhecimento de valores numéricos e unidades (baseada em Yolo)
3. Rede para identificação de polaridades (baseada em R-CNN keypoints models)

## Tipos de Simulação

O servidor suporta dois tipos de simulação:
- **Ponto de operação**: Exibe as tensões dos nós do circuito
- **Análise transiente**: Exibe gráficos de tensão nodal ou corrente em componentes ao longo do tempo

## API do Servidor

Os principais endpoints da API incluem:
- Recebimento e processamento de imagens
- Geração de netlist
- Configuração e execução de simulação
- Retorno dos resultados (tensões nodais ou gráficos)

## Integração com o Frontend

Este servidor é projetado para trabalhar em conjunto com a interface web Vue.js localizada na pasta `web` do projeto. Os resultados das simulações são enviados para a interface web para visualização pelo usuário.

## Projetos Futuros

- Implementação de mais componentes eletrônicos (transistores, MOSFETs, amplificadores operacionais)
- Geração de diagramas esquemáticos com visualização das tensões e correntes
