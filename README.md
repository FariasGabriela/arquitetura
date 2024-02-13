# arquitetura
Anotações da aula de fundamentos de arquitetura de software

## Introdução

*Arquitetura de Software:* Diretamente ligada ao processo de desenvolvimento de software. Mais baixo nivel que solução. Afeta a estrutura organizacional da empresa, por causa de formação de times, estrutura dos componentes

Tipo de arquitetura:
1. **Software**: Transforma requisitos de negocio em padrões de arquitetura, muitas vezes também é desenvolvedor, arquestrar pessoas desenvolvedoras. Entender de forma profunda modelos arquiteturais. *Auxilia na tomada de decisão em momentos de crise*, por causa da sua experiencia e leque de possibilidades pode ajudar. Além de reforçar boas praticas de desenvolvimento. 
2. **Solução**: Entre a área de negocios e software com visão estrátegica. Vê as necessidades da empresa e transforma em software. Faz desenhos arquiteturais da solução. Analisa os impactos comerciais com a solução tecnologica para cada caso/cliente. Pode participar do processo comercial/de venda e faz uma análise de custo. 
3. **Tecnologica**: Especialista em tecnologias específicas de mercardo; Gera valor com a sua expertise.
4. **Corporativa**: Impactam a organização como um todo. Consegue fazer uma avaliação de custo para a área de engenharia por exemplo. Avaliação de possiveis novas tecnologias. 

**Arquitetura de software** : Como eu consigo desenvolver esse software em componentes, como esses componentes vão atingir os obejtivos de negocios, com as restriçoes necessárias. 

*Definição formal:* é a organização fundamental de um sistema e seus componentes, suas relações, seu ambiente, bem como os principios que giuam seu design e evolução.

A arte de um arquiteto é pensar em como isso vai evoluir e seja sustentável.

---

## Vantagens de ter conhecimento em arquitetura de software:
* Ter uma visão macro para a micro, te dando um maior dominio;
* Ter mais opções e poder escolher a melhor solução, entendo o contexto pode melhorar a solução;
* Pensar a longo prazo e na sustentabilidade;
* Ficar menos influenciável com "hypes" do mercado;
* Ter boas práticas, estar mergulhado nisso;
* Ter clareza do impacto do software possui na organização como um todo;
* Tomar decisões com mais segurança;

___

## Arquitetura e Design
Arquitetura é o nível mais alto, componentização, abstrações, o que os componentes tem em comum, como padronizar. 
Design: mais baixo nivel, escopo mais local, a classe com menos responsabilidade. 

## Sustentabilidade
Quanto mais tempo o software fica no ar, mais ele retorna, e desenvolver software é caro e precisa se pagar ao longo de tempo
A solução precisa ser arquitetada! ou seja, precisa ser pensado para ser sustentável desde o dia zero.

## Pilares da arquitetura de software:
* Estruturação
* Componentização
* Relacionamento entre sistemas
* Governança

## Requisitos Arquiteturais: consegue definir as "regras do jogo"
* Performance
* Armazenamento dos dados
* Escalabilidade
* Segurança
* Legal
* Audit
* Marketing

---

## Caracrteristicas arquiteturais
Esteja preparada com pontos e caracteristicas arquiteturais ( requisitos não funcionais ) para que o sistema consiga suportar carga, se manter online e crescer.

## Caracteristicas arquiteturais: Estruturais ( mais ligadas ao processo de desenvolvimento )
* Configurável: Trabalhar com variaveis de ambiente, key de facil acesso, está facil essa config?
* Extensibilidade: usar um gatewey de pagamento, foi feito uma implementação e precisa ser alterada para outro gateway, é facil? trocar banco de dados, message broker
* Facil instalação: padronização do ambiente, por exemplo, com containers
* Reuso de componentes: diferentes equipes podem criar a mesma coisa, e são duas coisas para serem mantidas.
* Internacionalização: Começou a trabalhar com real e mudou pra dolar, como vai funcionar o software? tem suporte para isso?
* Fácil manutenção: desde a estrutura, até mesmo correções rapidas.
* Portabilidade: os sistemas tem que ser menos dependentes de outras ferramentas. Mudar banco de dados sem impactar negativamente e trabalhosamente o sistema.
* Fácil suporte: entender rapidamente aonde acontece os problemas.
  

## Perspecticas para arquitetar software de qualidade
* Performance: Desempenho do software; Podem ser avaliadas por: Latencia ou response time (quanto menor, melhor. levando em consideração o fator rede), Throughput ( mostra o quando de requisição aguenta, quanto maior, melhor );
* Escalabilidade: Motivos que causam: Processamento ineficiente, como ele lida com a aplicação em si; Recursos computacionais limitados; Trabalhar de forma bloqueante (recebe  a requisição e nao trava); Acesso serial aos recursos; Para aumentar a escalabilidade:  
* Resiliencia

-----

## Escalabilidade

É a capacidade do sistema de suportar o aumento dos workloados incrementando ou reduzindo o custo em igual ou menor proporção.

**Escala vertical**: apenas uma maquina com mais recurso computacional

**Escala Horizontal**: varias maquinas ( caso caiu o sistema nao fica fora do ar )


Escalando aplicações: 
* Descentralizar: Disco efêmero, servidor de aplicação fica em um lugar e servidor de asstes em outro, cache centralizado, sessões centralizadas, upload e gravação de arquivos não ficam na sua maquina ( para conseguir fazer o download )

  Escalar é desencentralizar para remover a maquina quando quiser sem perder informações e aumentar o throwput.


**Escalar Banco de dados**
* Aumentar o recurso computacional;
* Distruibuindo responsabilidades (escrita vs leitura);
* Shards de forma horizontal (adicionar varias maquinas de leitura, mudar o formato do banco de dados, dividir partiçoes dentro do BD);
* Serverless ( qualquer coisa que nao se preocupe em nível de servidor )
  
Pontos que nos ajudam a ter mais resiliencia nas aplicações: 
* Health Check
* Rate Limit: Limitar trafico de rede;
* Circuit breaker: protege o sistema para negar as requisições em caso de sobrecarga, por exemplo;
* API Gateway: Centraliza todas as requisições, e aplica regras politicas para aceitar ou negar a requisição, entendendo as necessidades individuais do sistema, podemos evitar requisições inapropriadas. Implementa politicas de rate limiting, Health Check e outras.
* Service Mesh: Controla o trafico de rede. Evita implementação de proteção pelo próprio sistema.
* Comunicação assíncrona: Evita perda de dados, consegue dar vasão a mais requisições. Não perde dados caso o server estiver fora, o servidor pode processar a informação quando o sistema estiver online. Processar aos poucos os dados. Para começar entenda com profundidade o memessage broker / sistema de stream;


----

***Um sistema lento no ar muitas vezes é pior que um sistema fora do ar!***

----






  







