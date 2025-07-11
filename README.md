# Modelagem de Ameaças Utilizando IA

## Integrantes
- Arilson Florencio Pereira Filho
- Pablo Jose Ribeiro do Carmo
- Rafael Barbosa Conceição

## Descrição do Projeto

Este projeto desenvolve uma solução de Inteligência Artificial para automatizar a modelagem de ameaças em arquiteturas de software, utilizando a metodologia STRIDE. A solução é capaz de interpretar diagramas de arquitetura de sistema em imagens, identificar componentes automaticamente e gerar relatórios de segurança abrangentes.

## Objetivo

Desenvolver um sistema que:
- Interprete automaticamente diagramas de arquitetura de sistema
- Identifique componentes como usuários, servidores, bases de dados, APIs, etc.
- Gere relatórios de modelagem de ameaças baseados na metodologia STRIDE
- Forneça análises de vulnerabilidades e contramedidas específicas

## Tecnologias Utilizadas

- **Roboflow**: Plataforma para gerenciamento de datasets e anotações
- **YOLOv11**: Modelo de detecção de objetos para identificação de componentes
- **Google Gemini 2.5 Flash**: IA generativa para criação de relatórios STRIDE
- **Ultralytics**: Framework para treinamento e inferência de modelos YOLO
- **Python**: Linguagem principal do projeto

## Arquitetura da Solução

### 1. Preparação do Dataset
- Utilização do Roboflow para download e gerenciamento do dataset
- Dataset anotado com componentes de arquitetura de software
- Formato YOLOv11 para treinamento

### 2. Treinamento do Modelo
- Modelo base: YOLOv11s
- Treinamento supervisionado com 25 épocas
- Resolução de imagem: 640x640 pixels
- Confiança mínima: 0.6

### 3. Detecção de Componentes
- Processamento de imagens de arquitetura
- Identificação automática de componentes
- Extração de lista de componentes únicos

### 4. Geração de Relatórios STRIDE
- Integração com Google Gemini para análise de segurança
- Relatório estruturado seguindo metodologia STRIDE
- Análise de ameaças específicas por componente

## Como Usar

### 1. Abrir o Google Colab
- Acesse [Google Colab](https://colab.research.google.com/)
- Faça upload do arquivo `hackathonf5.py` ou copie o código para um novo notebook

### 2. Executar o Sistema
Execute as células do notebook na ordem:
1. Instalação das bibliotecas
2. Imports necessários
3. Download do dataset via Roboflow
4. Treinamento do modelo YOLOv11
5. Detecção de componentes na imagem
6. Geração do relatório STRIDE com Google Gemini

### 3. Fluxo de Execução
O sistema seguirá automaticamente as etapas:
- Download e preparação do dataset
- Treinamento do modelo
- Processamento da imagem de arquitetura
- Identificação dos componentes
- Geração do relatório de seguranç

## Metodologia STRIDE

O relatório gerado segue a metodologia STRIDE, analisando:

- **S**poofing (Falsificação)
- **T**ampering (Violação)
- **R**epudiation (Repúdio)
- **I**nformation Disclosure (Divulgação de Informações)
- **D**enial of Service (Negação de Serviço)
- **E**levation of Privilege (Elevação de Privilégios)

## Componentes Suportados

O modelo é treinado para detectar os seguintes componentes de arquitetura:

- **User**
- **Load Balancer**
- **Compute**
- **Database**
- **API Gateway**
- **Storage**
- **Cache**
- **Network Security**
- **Message Queue**
- **Identity Service**

## Limitações

- Dependente da qualidade e clareza dos diagramas de entrada
- Requer conexão com internet para APIs do Roboflow e Google Gemini
- Precisão limitada pela qualidade do dataset de treinamento
- Análise de ameaças baseada em padrões gerais, não específicos do contexto

## Resultados

O sistema gera um relatório completo seguindo a metodologia STRIDE com:
- Identificação automática de componentes da arquitetura
- Análise de ameaças específicas por componente
- Recomendações de segurança
- Tabela detalhada com vulnerabilidades e contramedidas

## Conclusão

A solução desenvolvida demonstra a viabilidade de usar IA para automatizar a modelagem de ameaças em arquiteturas de software, proporcionando uma análise de segurança rápida e abrangente baseada na metodologia STRIDE.
