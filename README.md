# desafio-cloudformation-dio
 Implementando Infraestrutura Automatizada com AWS CloudFormation

# Desafio DIO - Implementando Infraestrutura Automatizada com AWS CloudFormation

Este repositório documenta o laboratório de **CloudFormation na AWS**, proposto pela **Digital Innovation One (DIO)**.  
O objetivo é consolidar o conhecimento adquirido sobre **infraestrutura como código (IaC)**, demonstrando como provisionar recursos na nuvem de forma automatizada e reprodutível.

---

## Objetivos do Desafio

- Aplicar conceitos de **CloudFormation** em um ambiente prático (simulado ou real).  
- Criar e entender **templates em YAML/JSON**.  
- Documentar o processo de forma clara e estruturada.  
- Utilizar o **GitHub** para compartilhar documentação técnica e exemplos.  

---

## Passo a Passo (Simulação do Laboratório)

### 1. O que é AWS CloudFormation?
O **AWS CloudFormation** é um serviço que permite **automatizar a criação de recursos** na AWS a partir de arquivos de configuração (`YAML` ou `JSON`).  
Com ele, você pode criar **pilhas (stacks)** que incluem instâncias EC2, buckets S3, VPCs e muito mais, sem precisar configurar manualmente pelo console.

---

### 2. Estrutura de um Template
Um template CloudFormation geralmente contém:
- **AWSTemplateFormatVersion** → versão do formato.  
- **Description** → descrição da stack.  
- **Resources** → onde os recursos são declarados (obrigatório).  
- **Parameters, Outputs, Mappings, Conditions** → opcionais, para customizar.  

---

### 3. Exemplo de Template (YAML)

Aqui está um exemplo simples que cria um **bucket S3** automaticamente:

```yaml
AWSTemplateFormatVersion: "2010-09-09"
Description: "Stack simples de exemplo - Criando um bucket S3"

Resources:
  MeuBucketS3:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: dio-desafio-cloudformation-exemplo
