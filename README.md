# 🚀 Startup Game (Refatoração)

![Java](https://img.shields.io/badge/Java-17+-red)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)

## 📌 Descrição
O **Startup Game** é uma simulação em turnos onde o jogador gerencia uma startup tomando decisões estratégicas.  
Cada escolha impacta indicadores como **Caixa, Receita, Reputação e Moral**.  
Ao final das rodadas, o jogo calcula um **score final** e apresenta o ranking entre os participantes.

Este projeto é uma **refatoração** do código original, aplicando **Programação Orientada a Objetos**, **padrões de projeto** e **persistência de dados**.

---

## 🛠️ Tecnologias e Conceitos
- **Java 17+**
- **Banco de dados H2** (persistência em memória/arquivo)
- **Padrão Strategy** (decisões)
- **Value Objects (VOs):** `Dinheiro`, `Percentual`, `Humor`
- **Configuração via `game.properties`**
- **Arquitetura modular**: `model`, `actions`, `engine`, `persistence`, `ui`

---

## 📂 Estrutura do Projeto
```
src/
├── config/
│   └── Config.java
├── model/
│   ├── Startup.java
│   ├── Deltas.java
│   ├── Rodada.java
│   ├── DecisaoAplicada.java
│   └── vo/
│       ├── Dinheiro.java
│       ├── Percentual.java
│       └── Humor.java
├── actions/
│   ├── DecisaoStrategy.java
│   ├── DecisaoFactory.java
│   ├── MarketingStrategy.java
│   ├── EquipeStrategy.java
│   ├── ProdutoStrategy.java
│   ├── InvestidoresStrategy.java
│   └── CortarCustosStrategy.java
├── persistence/
│   ├── DataSourceProvider.java
│   ├── StartupRepository.java
│   ├── RodadaRepository.java
│   └── DecisaoRepository.java
├── engine/
│   ├── GameEngine.java
│   └── ScoreService.java
└── ui/
    └── ConsoleApp.java

````

---

## ⚙️ Configuração
Edite `resources/game.properties` para definir parâmetros do jogo:
```properties
total.rodadas=8
max.decisoes.por.rodada=3
````

---

## ▶️ Como Executar

Clone o repositório, compile e execute o projeto.

# Clone o projeto
```bash
git clone https://github.com/seu-usuario/startup-game.git
cd startup-game
```
# Compile o código
```
javac -d out -cp "lib/*" src/**/*.java
```
# Execute o jogo
```
java -cp "out:resources:lib/*" Main
```

---

## 🧪 Testes

* Testes escritos com **JUnit 5**
* Possibilidade de **seed determinística** para resultados reproduzíveis

Execute os testes com:

```bash
mvn test
```

---

## 📊 Funcionalidades Extras (opcionais)

* 🔔 **Observer**: eventos com listeners
* ↩️ **Command**: undo/replay de decisões
* 🏁 **State**: máquina de estados
* 🤖 **Bots**: decisões automáticas
* 📑 **Exportação CSV** com métricas e ranking

---

## 👨‍💻 Autores

João de Sá Calvano Bezerra (JooJdeSaaS)

Projeto desenvolvido como **trabalho final da disciplina de Programação Orientada a Objetos – 2025/2**.

