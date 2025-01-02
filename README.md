# Nexa - 🧠 Análise Avançada de Imagens e Texto com IA na AWS

Automatize o processamento de documentos digitalizados usando Amazon Textract e crie soluções inteligentes para extração e estruturação de dados com alta precisão.

![Workflow Overview](./ocr_cnh/images/aws_textract.png)

## 📋 Visão Geral

Este projeto demonstra como utilizar o Amazon Textract para extrair texto, tabelas e campos-chave de documentos como faturas, contratos e reclamações. Foi desenvolvido para aplicar técnicas de Intelligent Document Processing (IDP), reduzindo o tempo e o esforço manual em tarefas repetitivas.

### 🚀 Objetivo
- Criar uma solução automatizada para extrair e estruturar informações de documentos digitalizados.
- Demonstrar a integração do Textract com outros serviços AWS, como S3 e Lambda.

### 🛠️ Configuração
![AWS](https://img.shields.io/badge/AWS-Textract-orange)
![Python](https://img.shields.io/badge/Python-3.x-blue)

**Pré-requisitos**
- Conta ativa na **AWS**.
- Python 3.x instalado.
- Bibliotecas: boto3, pandas, etc.

**Passo a Passo**
1. Clone o repositório:
`git clone <URL>`
2. Configure as permissões no IAM para usar o Amazon Textract.
3. Envie seus documentos para o bucket do Amazon S3.
4. Execute o script para processar os documentos e salvar os resultados em CSV ou JSON.

## 💡 Insights e Aprendizados
- Automação de Decisões Simples: Foi possível criar regras de negócio para validar documentos, como checar campos obrigatórios ou calcular totais automaticamente.
- Precisão na Extração de Dados: O Amazon Textract demonstrou alta eficiência ao lidar com documentos complexos, extraindo tabelas e campos-chave com precisão.
- Redução de Tempo e Esforço: Processos manuais que antes levavam horas foram reduzidos a minutos com automação.
- Desafios Superados:
  - Garantir a consistência no formato dos documentos processados.
  - Configurar corretamente permissões no IAM para evitar falhas de acesso.

## 📊 Resultados
**Exemplo de Entrada**
Documento de fatura enviado no formato PDF ou imagem.

**Exemplo de Saída**
- Texto extraído em JSON.
- Tabela estruturada em CSV pronta para análise.







Contém os projetos desenvolvidos durante o curso `Nexa - Análise Avançada de Imagens e Texto com IA na AWS`.

## Projetos

- [OCR CNH](./ocr_cnh/)
- [OCR Lista Escolar](./ocr_lista_escolar/)
- [Reconhecimento de Atacantes](./reconhecimento_atacantes/)
- [Reconhecimento de Celebridades](./reconhecimento_celebridades/)


