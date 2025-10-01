# StartupGame

```markdown
# 🚀 Startup Game (Refatoração)

![Java](https://img.shields.io/badge/Java-17+-red)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![License](https://img.shields.io/badge/license-MIT-green)

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
config/Config.java             # Leitura de game.properties
model/Startup.java             # Entidade principal
model/Deltas.java              # Variações de status
model/vo/                      # Value Objects
actions/                       # Estratégias de decisão (Strategy)
persistence/                   # Repositórios e integração com H2
engine/                        # Motor do jogo
ui/ConsoleApp.java             # Interface no terminal
Main.java                      # Ponto de entrada
resources/
game.properties                # Configurações do jogo
schema.sql                     # Script para criação de tabelas no H2

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

```bash
# Clone o projeto
git clone https://github.com/seu-usuario/startup-game.git
cd startup-game

# Compile o código
javac -d out -cp "lib/*" src/**/*.java

# Execute o jogo
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

Projeto desenvolvido como **trabalho final da disciplina de Programação Orientada a Objetos – 2025/2**.
Quer que eu também prepare um **RELATORIO.md** (como o professor pediu, listando os itens obrigatórios/opcionais implementados), para já deixar pronto no repositório?
```
