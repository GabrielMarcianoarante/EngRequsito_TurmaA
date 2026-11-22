<p align="center">
  <img src="logo-ceub-assinatura-conceito-deslocado-01.webp" alt="Logomarca do CEUB" width="300">
</p>

# Qualidade de software: guia de estudo da ISO/IEC 25010

**Material do estudante**  
**Curso:** Engenharia de Software  
**Disciplina:** Engenharia de Requisitos  
**Profª:** Kadidja Valéria  
**Tema:** Modelo de qualidade de produto da ISO/IEC 25010

🔗 **Atividade prática complementar:** [Aplicação da ISO/IEC 25010 — Projeto FlowOps](https://github.com/gabrielmarciano-dev/sistema-de-gestao-de-projetos-agil/blob/main/Documentacao/ISO_IEC%2025010.md)

---

## 1. Por que falar de qualidade?

Fazer o que foi pedido é só uma parte da qualidade de um software. Também importa saber se ele responde em tempo adequado, protege as informações, funciona de modo consistente e pode ser usado e atualizado sem dificuldade.

A **ISO/IEC 25010:2023** oferece um modelo para descrever e avaliar a qualidade de produtos de software e de Tecnologia da Informação e Comunicação (TIC). Publicada como segunda edição, ela substitui a versão de 2011.

> **Para pensar:** como sair de frases genéricas como “precisa ser rápido e seguro” e chegar a algo que a equipe consiga testar?

## 2. O que você vai estudar

Ao final da leitura, a ideia é que você consiga:

- compreender o conceito de qualidade de produto de software;
- reconhecer a finalidade da família SQuaRE;
- identificar as nove características da ISO/IEC 25010:2023;
- relacionar problemas de software às características de qualidade;
- diferenciar requisitos vagos de requisitos mensuráveis;
- elaborar requisitos de qualidade e critérios de aceitação;
- analisar conflitos entre diferentes características de qualidade.

## 3. Um caso para analisar

Imagine o seguinte cenário:

> Um sistema acadêmico possui todas as funcionalidades solicitadas. Entretanto, demora 15 segundos para abrir a página de notas, não funciona corretamente em celulares, apresenta mensagens difíceis de compreender e permite que usuários visualizem informações que não deveriam acessar.

Converse com o grupo e anote:

1. O sistema pode ser considerado de qualidade? Justifique.
2. Cumprir os requisitos funcionais é suficiente?
3. Quais problemas podem ser identificados?
4. Como esses problemas poderiam ser avaliados objetivamente?

## 4. Entendendo qualidade de software

Em termos simples, qualidade é o quanto o produto atende ao que as pessoas precisam, levando em conta o ambiente e as condições reais de uso.

Essa avaliação muda conforme o ponto de vista:

- **usuário:** o produto é útil, compreensível e confiável?
- **cliente:** o produto atende às necessidades do negócio?
- **desenvolvedor:** o código pode ser compreendido, testado e modificado?
- **organização:** o produto é seguro, sustentável e economicamente viável?
- **equipe de testes:** existem critérios objetivos para verificar sua qualidade?

### Não basta não apresentar erros

Mesmo que as funções estejam corretas, ainda podem existir problemas como:

- concluir uma compra, mas demorar excessivamente;
- possuir todas as funções, mas não oferecer recursos adequados de acessibilidade;
- executar as operações, mas expor dados pessoais;
- atender às necessidades atuais, mas ser difícil de modificar;
- funcionar em computadores, mas não se adaptar aos ambientes previstos.

## 5. Onde entra a família SQuaRE?

A ISO/IEC 25010 faz parte da família **SQuaRE — Systems and Software Quality Requirements and Evaluation**, que reúne referências para:

- modelos de qualidade;
- definição de requisitos de qualidade;
- medição da qualidade;
- avaliação de produtos;
- planejamento e gerenciamento da qualidade.

Na prática, o modelo pode ajudar a levantar requisitos, conferir se aspectos importantes foram considerados e definir objetivos para projeto, testes e critérios de aceitação.

## 6. Nove aspectos para avaliar

> Os nomes em português abaixo servem como apoio didático. Para uso técnico formal, consulte a norma oficial ou sua versão adotada no país.

| Característica | Pergunta para orientar a análise | Exemplo |
|---|---|---|
| Adequação funcional | As funções atendem ao que é necessário e produzem resultados corretos? | Aplicar corretamente as regras de cálculo das médias. |
| Eficiência de desempenho | O sistema responde bem sem consumir recursos em excesso? | Medir o tempo de resposta com vários acessos simultâneos. |
| Compatibilidade | Ele consegue trabalhar junto com outros sistemas? | Trocar dados com o sistema financeiro. |
| Capacidade de interação | As pessoas entendem como usar as funções? | Apresentar formulários claros e acessíveis. |
| Confiabilidade | O produto continua funcionando como esperado? | Manter o serviço disponível em períodos importantes. |
| Segurança | As informações e operações estão protegidas? | Controlar permissões e guardar o histórico de alterações. |
| Manutenibilidade | A equipe consegue entender, testar e alterar o produto? | Atualizar um módulo sem causar falhas nos outros. |
| Flexibilidade | O produto pode ser ajustado a novas condições? | Instalar o sistema em ambientes diferentes. |
| Proteção contra riscos (*safety*) | O uso pode causar danos a pessoas, bens ou ao ambiente? | Impedir uma ação quando há uma condição perigosa. |

### 6.1 Adequação funcional

Aqui se verifica se as funções necessárias existem, se os resultados estão corretos e se elas ajudam o usuário a concluir suas tarefas.

**Exemplo:** um sistema bancário precisa oferecer as operações necessárias, calcular corretamente juros e saldos e permitir que o usuário alcance seus objetivos.

### 6.2 Eficiência de desempenho

Neste aspecto, observam-se o tempo de resposta, o processamento, o consumo de recursos e a quantidade de acessos que o produto suporta.

**Exemplo de requisito:**

> O sistema deverá apresentar o resultado da consulta em até dois segundos para, no mínimo, 95% das requisições realizadas com até 500 usuários simultâneos.

### 6.3 Compatibilidade

Compatibilidade trata de como o produto funciona junto a outros sistemas ou componentes e de como consegue trocar informações com eles.

Isso pode aparecer, por exemplo, em:

- aplicativos executados no mesmo ambiente;
- comunicação entre sistemas por uma API;
- importação e exportação de dados;
- integração com sistemas externos.

### 6.4 Capacidade de interação

Esta característica olha para a experiência de quem usa o produto: se as funções são fáceis de encontrar, se as instruções ajudam e se os erros podem ser evitados ou corrigidos.

**Exemplo:** um formulário informa quais campos são obrigatórios, apresenta instruções compreensíveis e explica como corrigir dados inválidos.

### 6.5 Confiabilidade

Confiabilidade indica se o produto mantém o funcionamento previsto nas condições estabelecidas. Disponibilidade, recuperação após falhas e continuidade do serviço são alguns pontos que podem ser avaliados.

**Exemplo de requisito:**

> O serviço de matrícula deverá permanecer disponível em pelo menos 99,5% do período oficial de matrículas.

### 6.6 Segurança

Este aspecto considera a proteção de dados, contas e operações, incluindo quem pode acessar ou alterar cada informação.

**Exemplo:** um sistema acadêmico restringe a alteração de notas às pessoas autorizadas e registra quem realizou cada modificação.

### 6.7 Manutenibilidade

Manutenibilidade diz respeito ao esforço necessário para compreender o produto, testar suas partes e fazer mudanças com segurança.

**Exemplo:** uma alteração no módulo de pagamentos pode ser realizada e testada sem exigir mudanças indevidas no módulo de autenticação.

### 6.8 Flexibilidade

Flexibilidade é a possibilidade de ajustar o produto a mudanças de ambiente, de volume de uso ou de necessidade.

**Exemplo:** um sistema aumenta sua capacidade de atendimento durante o período de matrículas e pode ser implantado nos ambientes computacionais previstos.

### 6.9 Proteção contra riscos — *Safety*

Esta característica é importante quando uma falha pode causar danos a pessoas, equipamentos ou ao ambiente. Por isso, aparece com frequência em sistemas hospitalares, veículos, indústria, aviação e outras áreas críticas.

**Exemplo:** uma bomba de infusão impede a execução de uma operação quando os parâmetros informados ultrapassam limites de segurança previamente estabelecidos.

## 7. Escrevendo requisitos que possam ser verificados

As características ajudam a indicar o que merece atenção, mas ainda são amplas. No projeto, elas precisam virar requisitos específicos, com condições que permitam conferir se foram atendidas.

### Exemplo — desempenho

**Formulação vaga:**

> O sistema deve ser rápido.

**Formulação verificável:**

> O sistema deverá concluir a consulta de notas em até dois segundos para 95% das requisições, considerando até 500 usuários simultâneos.

### Exemplo — capacidade de interação

**Formulação vaga:**

> O sistema deve ser fácil de usar.

**Formulação verificável:**

> Em teste com usuários, pelo menos 90% dos estudantes deverão concluir a solicitação de matrícula sem ajuda e em até cinco minutos.

### Exemplo — segurança

**Formulação vaga:**

> O sistema deve ser seguro.

**Formulação verificável:**

> Após cinco tentativas consecutivas de autenticação inválida, a conta deverá ser temporariamente bloqueada por 15 minutos e o evento deverá ser registrado.

### Uma forma de escrever

> O sistema deverá **[o que precisa fazer]**, em **[quais condições]**, dentro de **[qual limite]**, verificado por **[qual teste]**.

## 8. Atividade — analisando um sistema acadêmico

**Organização:** grupos de três a cinco estudantes  
**Entregável:** tabela de análise da qualidade  
**Valor sugerido:** 0,5 ponto

### Estudo de caso

Uma instituição colocou um aplicativo acadêmico em uso. No primeiro mês, surgiram estas situações:

1. O cálculo da média final apresenta valores incorretos.
2. A página de notas demora aproximadamente 12 segundos para abrir.
3. Estudantes têm dificuldade para localizar a renovação de matrícula.
4. O aplicativo deixa de funcionar quando muitos usuários acessam simultaneamente.
5. Um estudante conseguiu visualizar o histórico de outro usuário.
6. Uma pequena alteração no cadastro provocou falhas em outros módulos.
7. O aplicativo não consegue importar informações do sistema financeiro.
8. A implantação em um novo servidor exige diversas alterações manuais.
9. Em uma funcionalidade de laboratório, um equipamento pode ser acionado mesmo quando o sensor informa condição insegura.

### O que fazer

Para cada item, o grupo deve:

1. identificar a característica de qualidade predominante;
2. justificar a classificação;
3. formular um requisito de qualidade mensurável ou verificável;
4. estabelecer um critério de aceitação;
5. indicar uma forma de teste ou avaliação.

Alguns casos podem envolver mais de uma característica. Escolham a principal e expliquem brevemente as outras relações que perceberem.

### Formulário de resposta

| Nº | Ocorrência | Característica Predominante | Justificativa | Requisito de Qualidade Mensurável | Critério de Aceitação | Teste ou Avaliação |
|--:|---|---|---|---|---|---|
| **1** | O cálculo da média final apresenta valores incorretos. | **Adequação funcional** | O sistema executa a função principal, mas gera resultados matematicamente incorretos. | O sistema deverá calcular a média final das disciplinas aplicando 100% das regras acadêmicas oficiais. | 0% de divergência entre a média calculada e a regra oficial em 1.000 simulações. | Testes unitários e de integração automatizados. |
| **2** | A página de notas demora aproximadamente 12 segundos para abrir. | **Eficiência de desempenho** | A espera atrapalha o uso da página. | A página deve carregar em até 2 segundos com até 500 usuários simultâneos. | Pelo menos 95% das consultas terminam dentro desse limite. | Teste de desempenho com carga simulada. |
| **3** | Estudantes têm dificuldade para localizar a renovação de matrícula. | **Capacidade de interação** | A navegação não deixa claro onde encontrar essa função. | O acesso à renovação deve estar disponível em até dois cliques a partir da página inicial. | Pelo menos 90% dos participantes encontram a opção em até um minuto, sem ajuda. | Teste de usabilidade com estudantes. |
| **4** | O aplicativo deixa de funcionar quando muitos usuários acessam simultaneamente. | **Confiabilidade** (e eficiência de desempenho) | O serviço não se mantém estável quando aumenta o número de acessos. | O sistema deve atender até 5.000 usuários simultâneos durante o período de matrículas. | Menos de 0,1% das requisições devem retornar erro HTTP 5xx no teste de carga. | Teste de carga e de estresse. |
| **5** | Um estudante conseguiu visualizar o histórico de outro usuário. | **Segurança** | A falha de autorização permite acesso a dados de outra pessoa. | Cada estudante deve consultar somente o próprio histórico acadêmico. | Nenhum dos casos de teste deve permitir a consulta de dados de outra conta. | Testes de autorização e análise de segurança. |
| **6** | Uma pequena alteração no cadastro provocou falhas em outros módulos. | **Manutenibilidade** | Uma mudança localizada está afetando partes que não deveriam depender dela. | Alterações no cadastro não devem interromper as funções dos outros módulos. | Todos os testes de regressão relacionados devem passar após a alteração. | Testes de regressão e análise do código. |
| **7** | O aplicativo não consegue importar informações do sistema financeiro. | **Compatibilidade** | Os dois sistemas não conseguem trocar os dados necessários. | O aplicativo deve importar os dados previstos pela integração com o sistema financeiro. | Pelo menos 99,9% dos registros válidos devem ser sincronizados corretamente. | Testes de integração e conferência dos dados importados. |
| **8** | A implantação em um novo servidor exige diversas alterações manuais. | **Flexibilidade** (instalação e adaptação) | A mudança de ambiente depende de muitos ajustes feitos à mão. | A instalação deve seguir o mesmo procedimento automatizado nos servidores homologados. | A implantação deve terminar sem etapas manuais fora do procedimento documentado. | Teste de instalação em ambiente homologado. |
| **9** | Em uma funcionalidade de laboratório, o equipamento pode ser acionado mesmo quando o sensor indica uma condição insegura. | **Proteção contra riscos (*safety*)** | O equipamento pode ser ligado em uma situação que oferece risco. | O sistema deve bloquear o acionamento sempre que o sensor indicar uma condição insegura. | O bloqueio deve ocorrer em todos os cenários de teste com alerta do sensor. | Simulação de sinais de alerta e teste de segurança operacional. |

## 9. Análise de conflitos de qualidade

As características de qualidade estão relacionadas. Uma decisão de projeto pode beneficiar uma característica e produzir impactos em outra.

Analise as situações:

1. A inclusão de novas verificações de segurança pode produzir algum impacto no desempenho? Explique.
2. Como mecanismos adicionais de autenticação podem afetar a interação do usuário?
3. Uma arquitetura muito flexível pode aumentar a complexidade de desenvolvimento e manutenção?
4. Que impactos técnicos e financeiros podem surgir quando a equipe aumenta a redundância para melhorar a confiabilidade?
5. Como a equipe deve decidir quais características terão maior prioridade em um projeto?

## 10. Exercícios de revisão

### Questão 1

Um sistema apresenta todas as funções necessárias, mas leva 20 segundos para processar uma consulta. Qual característica está mais diretamente comprometida?

A. Compatibilidade  
B. Eficiência de desempenho  
C. Manutenibilidade  
D. Segurança

### Questão 2

A capacidade de trocar dados corretamente com outro sistema está relacionada principalmente a:

A. Compatibilidade  
B. Confiabilidade  
C. Proteção contra riscos  
D. Adequação funcional

### Questão 3

Qual alternativa representa um requisito mensurável?

A. O sistema deve ser intuitivo.  
B. O sistema deve ser bastante seguro.  
C. O sistema deve ser moderno.  
D. A consulta deve ser concluída em até dois segundos para 95% das requisições.

### Questão 4

A facilidade para alterar e testar um componente está relacionada a:

A. Flexibilidade  
B. Manutenibilidade  
C. Compatibilidade  
D. Capacidade de interação

### Questão 5

Impedir que um sistema hospitalar execute uma operação que coloque o paciente em risco está relacionado principalmente a:

A. Adequação funcional  
B. Eficiência de desempenho  
C. Proteção contra riscos (*safety*)  
D. Compatibilidade

### Questão 6 — Produção textual

Escolha uma característica da ISO/IEC 25010:2023 e produza:

1. um exemplo de requisito vago;
2. uma versão mensurável ou verificável desse requisito;
3. um critério de aceitação;
4. uma estratégia de teste.

## 11. Síntese para estudo

- Qualidade de software não significa apenas ausência de erros.
- A ISO/IEC 25010 oferece uma linguagem comum para discutir a qualidade de produtos.
- A edição de 2023 apresenta nove características de qualidade.
- As características relevantes devem ser selecionadas conforme o contexto, os usuários e os riscos do produto.
- Um requisito de qualidade deve apresentar condições e critérios que permitam sua verificação.

> **Para lembrar:** uma característica indica **o que observar**; uma medida define **como avaliar**; e um critério de aceitação determina **qual resultado será considerado satisfatório**.

## 12. Referências

- INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. **ISO/IEC 25010:2023 — Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — Product quality model**. 2. ed. Genebra: ISO, 2023. Disponível em: <https://www.iso.org/standard/78176.html>.
- INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. **ISO/IEC 25002:2024 — Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — Quality model overview and usage**. Genebra: ISO, 2024. Disponível em: <https://www.iso.org/standard/78175.html>.

---

