# 🎮 Caça ao Tesouro

Um jogo de aventura em modo texto desenvolvido em Java, utilizando estrutura de dados de **Árvore Binária**.

## 📋 Sobre o Projeto

Trabalho prático da disciplina de **Estrutura de Dados** que implementa um jogo de exploração onde o jogador navega por uma floresta misteriosa em busca de um tesouro escondido. O jogador deve gerenciar sua vitalidade enquanto enfrenta desafios como armadilhas e locais perigosos.

## 🎯 Objetivo

Encontrar o tesouro escondido antes que sua vitalidade chegue a zero, navegando por diferentes locais interconectados em forma de árvore binária.

## 🌳 Estrutura do Projeto

O jogo é composto por 5 classes principais:

- **`No.java`** - Representa cada localização do mapa
- **`MapaArvore.java`** - Constrói e gerencia a estrutura da árvore binária
- **`Jogador.java`** - Controla o estado e movimentação do jogador
- **`SistemaArmadilha.java`** - Gerencia o sistema de armadilhas com dados
- **`CacaAoTesouro.java`** - Classe principal com o loop do jogo

## 🗺️ Mapa do Jogo

```
                    Entrada da Floresta (Raiz)
                           /            \
                    Clareira          Pântano
                    (+15 vida)        (-20 vida)
                     /    \            /      \
                Caverna   Rio      Aldeia   Templo
                (-10)    (+20)    (-15)⚠️   (-5)
                          |                   |
                       TESOURO🏆         Armadilha⚠️
                                          (-30)
```

**Legenda:**

- 🏆 = Tesouro (Objetivo final)
- ⚠️ = Armadilha (Sistema de dados)
- (+) = Ganha vitalidade
- (-) = Perde vitalidade

## ⚙️ Mecânicas do Jogo

### Sistema de Vitalidade

- Vitalidade inicial: **100 pontos**
- Vitalidade máxima: **100 pontos**
- Vitalidade mínima: **0 pontos**
- Cada local pode aumentar, diminuir ou manter a vitalidade

### Sistema de Armadilhas

Quando o jogador entra em uma sala com armadilha, ele deve lançar um dado (1-6):

- **Resultado ≥ 4**: Desvia parcialmente (perde 10 de vitalidade)
- **Resultado < 4**: Não consegue escapar (perde 30 de vitalidade)

### Navegação

- **Esquerda**: Move para o nó filho da esquerda
- **Direita**: Move para o nó filho da direita
- **Voltar**: Retorna ao nó pai (local anterior)
- **Sair**: Encerra o jogo

## 🚀 Como Executar

### Pré-requisitos

- Java JDK 8 ou superior instalado

### Compilação

```bash
# Navegue até o diretório do projeto
cd caminho/para/Caca

# Compile todos os arquivos .java
javac *.java
```

### Execução

```bash
# Execute o jogo
java CacaAoTesouro
```

## 🎮 Como Jogar

1. O jogo começa na **Entrada da Floresta**
1. Em cada turno, você verá:
- Nome e descrição do local atual
- Alteração de vitalidade (se houver)
- Sua vitalidade atual
- Opções de movimento disponíveis
1. Digite o número da opção desejada e pressione ENTER
1. Se encontrar uma armadilha, pressione ENTER para lançar o dado
1. Continue explorando até:
- ✅ **Encontrar o tesouro** (VITÓRIA!)
- ❌ **Vitalidade chegar a zero** (GAME OVER)

## 📊 Condições de Vitória/Derrota

### ✅ Vitória

Chegar ao local “Universidade Católica” onde o tesouro está escondido.

### ❌ Derrota

A vitalidade do jogador chegar a zero em qualquer momento.

## 🛠️ Tecnologias Utilizadas

- **Linguagem**: Java
- **Estrutura de Dados**: Árvore Binária (implementação própria)
- **Paradigma**: Programação Orientada a Objetos

## 📝 Requisitos Atendidos

- ✅ Implementação de árvore binária sem uso de Collections
- ✅ Sistema de navegação (esquerda, direita, voltar)
- ✅ Sistema de vitalidade com ganhos e perdas
- ✅ Tesouro posicionado em nó folha
- ✅ Condições de vitória e derrota
- ✅ Interface em modo texto
- ✅ Encapsulamento (atributos private com getters/setters)
- ✅ Funcionalidade extra: Sistema de armadilhas com dados

## 👥 Autor

Trabalho desenvolvido para a disciplina de Estrutura de Dados.

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais.

-----

⭐ **Dica**: O caminho mais seguro para o tesouro é: Esquerda → Direita → Esquerda

🎲 **Boa sorte na sua caça ao tesouro!**