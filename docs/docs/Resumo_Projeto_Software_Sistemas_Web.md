# Projeto de Software e Sistemas Web — Resumo

## 1. O que é Projeto de Software

### Conceito de Projeto
Um **projeto** é um esforço temporário, com início e fim definidos, para criar um produto, serviço ou resultado único, envolvendo coordenação de recursos (humanos, materiais, financeiros) dentro de restrições de tempo e orçamento.

### Projeto de Software
É a etapa da engenharia de software que **antecede o desenvolvimento propriamente dito**. Envolve:
- Definir a **arquitetura** do software.
- Transformar especificações em **documentos** interpretáveis pelos programadores.
- Atividades do ciclo: **concepção → projeto → teste → manutenção pós-lançamento**.

**Duas fases principais:**
| Fase | Foco |
|---|---|
| **Projeto preliminar** | Converte requisitos em arquitetura geral (software + dados) |
| **Projeto detalhado** | Refina a arquitetura: estrutura de dados e representações algorítmicas |

### Objetivo do Projeto de Software (segundo Pressman)
Gerar um modelo/representação **sólido, conveniente e agradável**, praticando primeiro a **diversificação** (explorar soluções) e depois a **convergência** (escolher a melhor). Deve sempre considerar o escopo, a estratégia de negócio e as necessidades do cliente (do mais simples ao mais complexo).

### Documentação no Projeto de Software
Serve como:
- **Guia** para programadores.
- **Meio de comunicação** entre todos os envolvidos.
Precisa ser clara e **atualizada constantemente** para reduzir ambiguidades.

### Tipos de Projeto de Software
| Tipo | O que faz |
|---|---|
| **Projeto de Dados** | Transforma o modelo de domínio em estruturas de dados |
| **Projeto Arquitetural** | Define o relacionamento entre os grandes componentes do sistema |
| **Projeto de Interface** | Define a interação homem-máquina (layout, usabilidade) |
| **Projeto Procedimental** | Detalha os passos/processos de cada componente |
| **Projeto Preliminar** | Transforma requisitos em arquitetura de software/dados |
| **Projeto Detalhado** | Aprimora a arquitetura: estrutura de dados e algoritmos |

---

## 2. Projeto de Sistemas Web com Princípios da Engenharia de Software

- Sistemas Web são mais **complexos** que sistemas de outras plataformas, exigindo fundamentação em **princípios de engenharia**.
- Características essenciais que um projeto de sistema Web precisa garantir: **funcionalidade, eficiência, robustez, confiabilidade, portabilidade e facilidade de uso**.

### Arquitetura básica da Web (Figura 1)
```
Navegador (Cliente) --HTTP Request--> Internet --> Web Server (Servidor)
Navegador (Cliente) <--HTTP Response-- Internet <-- Web Server (Servidor)
```
O cliente faz uma requisição HTTP através da internet; o servidor recebe, processa e retorna a resposta HTTP com os dados solicitados.

### Importância do Projeto de Sistemas Web
- É tanto o **passo inicial** quanto o **final** no desenvolvimento (permeia todo o ciclo de vida).
- Opera em **alto nível de abstração**, definindo a estrutura geral do sistema.
- O refinamento busca sistemas **resistentes a mudanças** e adaptáveis a novas demandas.

### Características Essenciais de Qualidade (6 itens)
1. **Funcionalidade** – atende às necessidades dos usuários.
2. **Eficiência** – desempenho otimizado, resposta rápida.
3. **Robustez** – lida com falhas/condições inesperadas sem perder dados.
4. **Confiabilidade** – operação consistente, sem erros, com segurança e integridade dos dados.
5. **Portabilidade** – fácil transferência entre ambientes diferentes.
6. **Facilidade de Uso** – interfaces amigáveis e intuitivas.

> 💡 Dica de prova: essas 6 características costumam aparecer separadas — memorize-as junto com uma palavra-chave de cada.

---

## 3. Conceituação de Componente

### O que é um Componente de Software
Unidade **independente e reutilizável** que encapsula funcionalidade e dados para realizar tarefas específicas dentro de um sistema maior — os "blocos de construção" de um sistema. Possui **interface pública** bem definida para interação com outros componentes.

### Como Projetar Componentes (8 passos)
1. **Identificação e definição** — modularizar partes do sistema com propósito claro.
2. **Definição da interface** — métodos/propriedades disponíveis, estável e intuitiva.
3. **Encapsulamento** — expor só o necessário; esconder a implementação interna.
4. **Coesão e acoplamento** — **alta coesão** (partes internas relacionadas) e **baixo acoplamento** (independência entre componentes).
5. **Reusabilidade** — componentes genéricos e configuráveis.
6. **Testabilidade** — testes unitários individuais.
7. **Documentação** — interfaces, funcionalidades, limitações, exemplos.
8. **Performance** — otimização e monitoramento contínuo.

---

## 4. Projetar Componentes Baseados em Classes

Traduz componentes em **implementações orientadas a objetos**. Etapas:

1. **Identificação das classes**
   - Definir responsabilidades → cada responsabilidade pode virar uma classe.
   - Estabelecer relacionamentos (herança, associação, agregação, composição).
2. **Definição das interfaces**
   - Criar interfaces com métodos públicos.
   - Aplicar o **Interface Segregation Principle** (interfaces específicas, não monolíticas).
3. **Encapsulamento e design de classes**
   - Atributos privados, acessados via getters/setters.
   - **Single Responsibility Principle** (uma classe = uma responsabilidade).
4. **Implementação de métodos e propriedades**
   - Distinguir métodos públicos (interface) e privados (uso interno).
5. **Criação de artefatos de software**
   - Uso de **diagramas UML** (classe, sequência, caso de uso).
   - Documentação (ex.: Javadoc).
6. **Reusabilidade e modularidade**
   - Uso de **design patterns**; princípio "aberto para extensão, fechado para modificação".
7. **Teste e validação**
   - Testes unitários (ex.: JUnit); técnicas de **mocking e stubbing**.
8. **Performance e manutenção**
   - Otimização e **refatoração** sem alterar a funcionalidade externa.

---

## 5. Modelo de Domínio x Diagrama de Classes

| Aspecto | Modelo de Domínio | Diagrama de Classes |
|---|---|---|
| Nível de abstração | Alto (conceitual) | Baixo (técnico/detalhado) |
| Foco | "O quê" o sistema representa | "Como" o sistema será implementado |
| Detalhes técnicos | Não mostra métodos/atributos | Mostra classes, atributos, métodos e relacionamentos |
| Notação | Representação simplificada | UML (Unified Modeling Language) |

> Resumindo: o **Modelo de Domínio** captura os conceitos e regras do negócio (mundo real); o **Diagrama de Classes** concretiza essa abstração em uma estrutura de código, com atributos, métodos e visibilidade.

### Passos para criar um Diagrama de Classes
1. **Identificação de Classes**
   - Análise de requisitos (entidades do domínio).
   - Agrupamento de funcionalidades (aplicando o **SRP**).
2. **Definição de Atributos e Métodos**
   - Atributos = estado do objeto (com visibilidade: privado/público/protegido).
   - Métodos = comportamentos/ações (públicos ou privados).
3. **Relacionamentos entre Classes**
   | Tipo | Significado | Representação |
   |---|---|---|
   | **Associação** | Dependência/comunicação entre classes | Linha simples |
   | **Agregação** | Relação "parte-todo" — parte existe sem o todo | Losango vazio (◇) |
   | **Composição** | Parte-todo mais forte — parte não existe sem o todo | Losango preenchido (◆) |
   | **Herança** | Relação "é um" | Linha sólida + seta fechada |
   | **Implementação de Interface** | Classe implementa métodos de uma interface | Linha tracejada + seta fechada |
4. **Visibilidade**
   - **Público (+)** — acessível por qualquer classe.
   - **Privado (-)** — acessível só dentro da própria classe.
   - **Protegido (#)** — acessível pela classe e suas subclasses.
5. **Ferramentas** — UML, Lucidchart, Visio, StarUML, Visual Paradigm, Draw.io, plugins de IDEs (IntelliJ, Eclipse, Visual Studio).
6. **Revisão e refinamento** — iteração contínua + feedback dos interessados.
7. **Documentação e comunicação** — legendas, descrições, notas explicativas.
8. **Consistência com o código** — diagrama deve refletir fielmente o código implementado, mantendo sincronização.

---

## 6. Quadro-resumo geral

| Conceito | Definição-chave |
|---|---|
| Projeto de Software | Planejamento que precede o desenvolvimento (arquitetura + documentação) |
| Projeto de Sistemas Web | Aplica princípios de engenharia devido à complexidade da Web (cliente-servidor via HTTP) |
| Componente de Software | Unidade reutilizável e independente, com interface pública |
| Classe | Implementação concreta de um componente via POO |
| Modelo de Domínio | Abstração conceitual do negócio ("o quê") |
| Diagrama de Classes | Representação técnica em UML ("como") |

### Pontos de atenção para prova
- Diferença entre **projeto preliminar** e **projeto detalhado**.
- As **6 características de qualidade** de um sistema Web (funcionalidade, eficiência, robustez, confiabilidade, portabilidade, facilidade de uso).
- **Alta coesão x baixo acoplamento** como boas práticas de design de componentes.
- Diferença entre **agregação** e **composição** (existência independente ou não da parte).
- Diferença entre **Modelo de Domínio** (conceitual) e **Diagrama de Classes** (técnico/UML).
- Os **3 níveis de visibilidade** em UML: público (+), privado (-), protegido (#).
