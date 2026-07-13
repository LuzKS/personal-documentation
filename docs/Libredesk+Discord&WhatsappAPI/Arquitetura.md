[[Documentação]]

Sumário:
 - [[#HTTP]]
 - [[#Requests]]
### HTTP 
 Protocolo que permite conexão e envio de recursos na web, permite a troca de dados e funciona como cliente-servidor. Um doc completo é reconstriido a partir de diferentes sub-docs 
![[Pasted image 20260713123548.png]]

os dados enviados pelo cliente são chamados de *request*/requisições e as respostas recebidas do servidor são *reponses*.
O HTTP também pode ser usado para buscar partes de documentos para atualizar páginas da Web sob demanda.

### Proxy e Cache
Um **servidor proxy** é um computador ou programa **intermediário (gateway)** usado ao navegar em conexões de internet diferentes.

- Um **proxy de encaminhamento** que lida com pedidos de e para qualquer lugar na internet.
- Um **proxy reverso** que recebe pedidos da Internet e os encaminha para servidores numa rede interna. (tipo o que fazemos no nginx)

![A HTTP request from a client forwarded by several proxies to a server and a response taking the same route back to the client.|601](https://mdn.github.io/shared-assets/images/diagrams/http/overview/client-server-chain.svg)

Cachê seria uma forma de armazenar dados temporariamente para serem usados em requests subsequentes, isso diminui o tempo de resposta, otimizando..

### Cliente: o agente-usuario
Agente-Usuário seria qualquer sistema que age em nome do usuário. Essa função é predominantemente realizada pelo navegador Web.

No caso do meu sistema, o bot é o cliente (pede algo) e a API é o garçom pq entrega algo (garçom)

### Requests

```
import requests

payload = {'key1': 'value1', 'key2': 'value2'}
r_pay = requests.get('https://httpbin.org/get', params=payload)
print(r_pay.url)

# r =  requests.get('https://api.github.com/events')

r = requests.get('https://httpbin.org/post', data={'key': 'value'})
print(f'\n{r.text}')

r_post = requests.post('https://httpbin.org/post', data={'key': 'value'})
print(f'\n{r_post.text}')
```
