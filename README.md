# Deploy - Previsão de Diabetes (Povo Pima)

Este repositório contém uma API em Flask para realizar previsões de diabetes utilizando um modelo de Machine Learning (Random Forest) previamente treinado. A aplicação foi conteinerizada com Docker e hospedada na nuvem.

Este trabalho faz parte de um projeto acadêmico realizado na disciplina de Disruptive Architectures IoT, IOB e Generative IA da faculdade FIAP.

## Integrantes de Grupo
- Nathália Mantovani de Falco - RM99904
- João Victor Ignacio Madella - RM561007
- Renato de Angelo - RM560585

## ☁️ Acesso em Produção (Nuvem)

A API está publicada e pode ser acessada publicamente através do link:
**https://deployapi-cp.onrender.com**

### Endpoints disponíveis:

* **`GET /`**: Rota de verificação de status da API. Retorna uma mensagem confirmando que o servidor está online.
* **`POST /predict`**: Rota que recebe os dados médicos da paciente em formato JSON e retorna o diagnóstico de diabetes (0 = Sem Diabetes, 1 = Com Diabetes).

### Como testar na nuvem (via Postman)
1. Abra o Postman e crie uma requisição **POST**.
2. Insira a URL: `https://deployapi-cp.onrender.com/predict`
3. Vá na aba **Body**, selecione **raw** e escolha o formato **JSON**.
4. Cole o payload de teste abaixo e clique em Send:

```json
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