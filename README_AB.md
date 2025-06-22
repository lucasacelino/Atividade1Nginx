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

**Após a execução do comando, os seguintes dados do teste e carga são mostrados abaixo:**

```
Server Software:        nginx/1.24.0
Server Hostname:        localhost
Server Port:            80

Concurrency Level:      100
Time taken for tests:   0.124 seconds
Complete requests:      1000
Failed requests:        0
Total transferred:      626000 bytes
HTML transferred:       384000 bytes
Requests per second:    8038.65 [#/sec] (mean)
Time per request:       12.440 [ms] (mean)
Time per request:       0.124 [ms] (mean, across all concurrent requests)
Transfer rate:          4914.25 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    5   1.2      5       9
Processing:     3    7   2.3      6      15
Waiting:        0    5   2.0      4      12
Total:          7   12   2.0     11      20

Percentage of the requests served within a certain time (ms)
  50%     11
  66%     12
  75%     13
  80%     13
  90%     14
  95%     16
  98%     17
  99%     19
 100%     20 (longest request)
```

Como podemos observar, o teste de carga foi feito na aplicação que está hospedada em um servidor nginx - `Server Software: nginx/1.24.0`. Todas as 1000 requisições foram feitas em - `0.124` segundos, menos de 1 segundo. Nenhuma requisição falhou - `Failed requests: 0`. Cada requisição levou em média 12 ms para ser processada, se caso fossem feitas executadas de forma serial(uma por uma) - `Time per request: 12.440 [ms] (mean)`. A maioria das requisições foram executadas entre 11 e 13 ms - 
```
50%  11
66%  12
75%  13
80%  13
```
A requisição mais lenta demorou 20 ms - `100% 20 (longest request)`