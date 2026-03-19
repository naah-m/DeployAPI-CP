# Deploy - Previsão de Diabetes (Povo Pima)

Este repositório contém a API em Flask para realizar previsões de diabetes utilizando um modelo Random Forest treinado, e faz parte de um projeto acadêmico realizado na disciplina de Disruptive Architectures IoT, IOB e Generative IA da faculdade FIAP.

Grupo:
- Nathália Mantovani de Falco - RM 99904
- 
- 

## Como rodar localmente com Docker
1. Construa a imagem executando no terminal: 
   `docker build -t modelo-diabetes .`
2. Inicie o container executando: 
   `docker run -p 8000:8000 modelo-diabetes`

## Como testar (Postman)
Abra o Postman e faça uma requisição **POST** para `http://localhost:8000/predict`. 
Na aba **Body**, selecione **raw** e o formato **JSON**. Cole os dados abaixo e clique em Send:

[
  {
    "Pregnancies": 6,
    "Glucose": 148.0,
    "BloodPressure": 72.0,
    "SkinThickness": 35.0,
    "Insulin": 0.0,
    "BMI": 33.6,
    "DiabetesPedigreeFunction": 0.627,
    "Age": 50
  }
]