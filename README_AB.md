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
> <svg xmlns="http://www.w3.org/2000/svg" width="34" height="34" viewBox="0 0 24 24"><g fill="none" stroke="#e11d48" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M12 16v-4m0-4h.01"/></g></svg> O localhost é a url da sua aplicação que está hospedada no Nginx
