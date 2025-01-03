# Reconhecimento de Celebridades com Amazon Rekognition

![Workflow Overview](https://example.com/hero-image.jpg)

## **Visão Geral**

Este projeto demonstra como utilizar o serviço **Amazon Rekognition** para identificar celebridades em imagens. O reconhecimento de celebridades é uma funcionalidade poderosa, que pode ser integrada a diversas aplicações, desde sistemas de mídia até soluções de marketing.

## **Objetivos do Projeto**

- Explorar o **Amazon Rekognition** e suas funcionalidades.
- Demonstrar a identificação automatizada de celebridades em imagens.
- Aprender a configurar e integrar os serviços da AWS para tarefas de visão computacional.
- Criar um portfólio rico que destaque habilidades técnicas em IA e cloud computing.

## **Tecnologias Utilizadas**

![AWS](https://img.shields.io/badge/AWS-Textract-orange)
![Amazon Rekognition](https://img.shields.io/badge/Amazon-Rekognition-green)
![Python](https://img.shields.io/badge/Python-3.x-blue)

- **Amazon Rekognition:** Serviço de visão computacional da AWS para análise de imagens e vídeos.
- **Python (boto3):** SDK para interação com os serviços AWS.
- **Amazon S3:** Armazenamento de imagens para análise.

## **Fluxo de Trabalho**

1. **Upload da Imagem:**
   - As imagens são enviadas para um bucket no Amazon S3.

2. **Análise com Amazon Rekognition:**
   - A imagem é processada pelo serviço de **Celebrities Recognition**, que retorna as seguintes informações:
     - Nome da celebridade.
     - Pontuação de confiança.
     - Links relacionados.

3. **Exibição dos Resultados:**
   - Os dados processados são apresentados de forma estruturada e visual.

## **Configuração do Ambiente**

### Pré-requisitos

- Conta ativa na AWS.
- Python 3.x instalado.
- Credenciais da AWS configuradas no ambiente local (via AWS CLI ou arquivo `.aws/credentials`).

### Instalação das Dependências

```bash
pip install boto3
```

### Configuração do Bucket S3

1. Crie um bucket no Amazon S3 para armazenar suas imagens.
2. Garanta que o bucket tenha permissões adequadas para leitura/escrita pelo Amazon Rekognition.

## **Como Executar**

1. **Suba uma Imagem para o S3:**
   - Utilize a interface do Amazon S3 ou um script Python para enviar imagens ao bucket configurado.

2. **Execute o Script:**
   - Use o código disponibilizado para analisar as imagens e obter resultados:

```python
import boto3

def analyze_image(bucket, photo):
    client = boto3.client('rekognition')
    response = client.recognize_celebrities(
        Image={
            'S3Object': {
                'Bucket': bucket,
                'Name': photo
            }
        }
    )
    return response

# Exemplo de uso
response = analyze_image('meu-bucket', 'imagem.jpg')
print(response)
```

3. **Visualize os Resultados:**
   - Verifique os nomes das celebridades e outros detalhes retornados pelo Amazon Rekognition.

## **Aprendizados e Insights**

- **Visão Computacional:** Compreensão do processamento de imagens em escala e detecção automatizada de objetos e rostos.
- **Integração com AWS:** Configuração e uso do S3 e Rekognition para análise de dados.
- **Automação e Escalabilidade:** Como soluções em cloud tornam processos como este rápidos e escaláveis.
- **Possibilidades Práticas:**
  - Aplicações em gerenciamento de mídia.
  - Identificação de celebridades em eventos ao vivo.
  - Marketing direcionado com base em conteúdo visual.

## **Possíveis Expansões**

- Exportação dos resultados para um arquivo CSV.
- Integração com uma interface web (usando Flask ou Streamlit).
- Processamento em lote de várias imagens ao mesmo tempo.

## **Capturas de Tela**

Adicione capturas de tela do processo ou resultados aqui:

![Resultados do Projeto](./reconhecimento_celebridadas/images/bbc-resultado.jpg)

## **Contribuição**

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---

**Autor:** Seu Nome  
**LinkedIn:** [Júlio César Linkedin](https://www.linkedin.com/in/julio-cesar-candeia-818a26241/)  
**Portfólio:** [Júlio César github](https://github.com/juliocesar710)
