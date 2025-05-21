# Segunda parte da atividade Gerência e Configuração de Servidores
A segunda parte desta atividade tem objetivo:
- Instalar o Apache Benchmark e realizar um teste de carga na aplicação que foi colocada no servidor Nginx.

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
> O localhost é a url da sua aplicação que está hospedada no Nginx