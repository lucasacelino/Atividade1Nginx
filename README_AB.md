# Segunda parte da atividade Gerência e Configuração de Servidores
A segunda parte desta atividade tem objetivo:
- Instalar o Apache Benchmark e realizar um teste de carga na aplicação React que está hospedada no servidor Nginx.

## 1º Passo - Instalar o Apache Benchmark:
Para instalar o ApacheBenchmark, execute o comando abaixo:
```
sudo apt install apache2-utils
```

## 2º Passo - Realizar o teste de carga na aplicação
Abra a sua aplicação em sua IDE de preferência. Logo após, abra o terminal e execute o seguinte comando:
```
ab -n 1000 -c 100 http://localohost/
```
> ![alt text](image-1.png) O localhost é a url da sua aplicação que está hospedada no Nginx

### Significado detalhado de execução para realizar o teste de carga:
`-n`: número de requisições que serão realizados na aplicação, no caso do comando acima serão feitas 1000 requisições.
`-c`: número de requisições concorrentes que serão feitas na aplicação, ou seja, ao mesmo tempo. No comando acima serão feitas 100 concorrentes.
