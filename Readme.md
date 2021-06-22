# Algoritmo de _Path Computation Element_ usando _Planning_

### Aluno: [Márcio de Freitas Minicz](https://github.com/minicz)
### Orientador: [Felipe Borges Coelho](https://github.com/FelipeBorgesC)

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

- [Código](https://github.com/minicz/PathComputationElement).

---

## Resumo

Qualquer operadora de telecomunicações precisa se preocupar em fazer engenharia de tráfego na sua rede, de forma a garantir que as demandas contratadas sejam plenamente atendidas, dentro dos parâmetros de qualidade de serviço (QoS - _Quality of Service_) combinadas. Nas redes MPLS (_MultiProtocol Label Switching_) é utilizado um elemento que escolhe quais enlaces (PCE - _Path Computation Element_) serão utilizados dentro da rede.

A parte crítica na construção de um PCE é a escolha do algoritmo que será utilizado para a escolha dos enlaces a serem utilizados por cada demanda.

Aqui propomos a utilização da biblioteca _planner_ que é implementada na linguagem [Picat](http://www.picat-lang.org). Essa linguagem tem por características ser uma linguagem que trabalha com múltiplos paradigmas de programação e que possui embutido mecanismos para planejamento, programação por restrição, programação linear e SAT.

O objetivo é obter um planejamento, isto é, qual caminho deve ser utilizado por cada uma das demandas.

Para modelar o problema é considerado:

- Os enlaces são simétricos - mesma largura de banda para cada direção;

- As demandas são simétricas - mesma velocidade deverá ser disponibilizada entre quais dois pontos;

- O cálculo não é em tempo real.

Da maneira que o problema ficou modelado é possível considerar diferentes parâmetros de qualidade de serviço, sendo que o _planner_ sempre tenta utilizar o caminho com melhor QoS. Nos testes foi considerado a quantidade de saltos entre os dois pontos.

O _planner_ em si é definido pelo estado final (função `final()`) e as ações a serem feitas (`action()`), que neste caso foi somente uma.

Ao se executar o programa é encontrado a primeira solução de planejamento que atenda às demandas e que respeite a capacidade da rede (largura de banda no início). Como resultado é informado o estado final da rede e quais caminhos cada demanda deverá utilizar.

Com a solução obtida é possível fazer a análise de redes reais, de forma a permitir a configuração dos caminhos a serem utilizados por cada demanda. Também permite a análise de cenários _what-if_ para estudar necessidades de crescimento ou a possibilidade de falhas na infraestrutra atual.

---

Matrícula: 192.671.072

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
