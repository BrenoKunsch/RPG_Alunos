# ⚔️ RPG Battle System

Um mini sistema de **batalha em turnos de RPG** desenvolvido em **PHP + MySQL**.  
O objetivo é simular batalhas entre jogadores em um coliseu, com atributos como **vida, ataque, defesa, força e sorte**.

---

## 📦 Como usar

### 1. Configuração do Banco de Dados
- Abra o **MySQL Workbench**.
- Rode o esquema `RPG_BATTLE.sql` para criar as tabelas e inserir os dados iniciais.

### 2. Configuração do Servidor
- Extraia o arquivo **RPG** no diretório do seu servidor local (**XAMPP** ou **WAMP**).
- Configure a comunicação entre o PHP e o MySQL no arquivo de conexão.

---

## 🗄️ Comandos MySQL Importantes

⚠️ **Antes de iniciar uma batalha, é necessário configurar via MySQL.**

### ➕ Criar um novo Coliseu

INSERT INTO rpg_battle(title_battle) 
VALUES ("Coliseu Charmosa");

### 🔄 Adicionar um turno à batalha de ID 1 (começando pelo jogador de ID 1)

INSERT INTO rpg_battle_turn(rpg_battle_id, current_player) 
VALUES (1, 1);

### ▶️ Iniciar a batalha

Atualize o status da batalha de ESPERA para ATIVA:

UPDATE rpg_battle 
SET status_battle = 'ATIVA' 
WHERE id_battle = 1;

### ⚠️ Observação Importante

Atualmente não existe tela de criação de salas.
Portanto, a criação de batalhas e turnos deve ser feita diretamente no MySQL utilizando os comandos acima.

### 🕹️ Recursos do Sistema

    🎯 Sistema de turnos (cada jogador joga na sua vez).

    💥 Cálculo de dano com chance de crítico.

    🛡️ Defesa e atributos básicos já aplicados.

    🏟️ Batalhas em coliseus configurados manualmente.

### 🚀 Tecnologias Utilizadas

    🐘 PHP

    🗄️ MySQL

    ⚡ XAMPP / WAMP (servidor local)
