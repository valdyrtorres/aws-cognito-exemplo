1) Criar o projeto usando o serverless framework
serverless create --template aws-nodejs-typescript --path aws-cognito-example

2) Configurar o projeto alterando o serverless.ts na raiz do projeto

3) npm install

4) serverless deploy

5) 
Deploying aws-cognito-example to stage dev (us-east-1)

Deploying aws-cognito-example to stage dev (us-east-1)

✔ Service deployed to stack aws-cognito-example-dev (71s)

endpoints:
  1) Cria o usuário
  POST - https://a6rlm1hop0.execute-api.us-east-1.amazonaws.com/dev/signup
  2) Faz o login e recebe o accessTokem
  POST - https://a6rlm1hop0.execute-api.us-east-1.amazonaws.com/dev/login
  3) Faz o get, mas tem que passar o accessToken via Bearer
  GET - https://a6rlm1hop0.execute-api.us-east-1.amazonaws.com/dev/hello
  4) Faz o get, mas tem que passar o accessToken via Bearer
  GET - https://a6rlm1hop0.execute-api.us-east-1.amazonaws.com/dev/welcome
functions:
  signup: aws-cognito-example-dev-signup (159 kB)
  login: aws-cognito-example-dev-login (159 kB)
  hello: aws-cognito-example-dev-hello (12 kB)
  welcome: aws-cognito-example-dev-welcome (12 kB)



validateCredentials: é responsável por validar a entrada dos dados fornecidos pelos usuários, conferindo se o e-mail e senha são válidos. Para isso, é verificado se a senha possui pelo menos oito caracteres. E, para validar o e-mail, é utilizada uma biblioteca externa para verificar se segue o padrão esperado. Para instalá-la em seu projeto, basta executar o comando npm i validator ou yarn add validator.