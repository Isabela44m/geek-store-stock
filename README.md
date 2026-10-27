# Geek Store

## Introdução

Este repositório é destinado ao cliente Júnior, responsável pela Geek Store.

O objetivo do sistema é auxiliar no gerenciamento da loja de action figures, permitindo controlar produtos, estoque, usuários e movimentações de entrada e saída de mercadorias.

#MER
### **1\. Produto**

* id\_produto — SERIAL PRIMARY KEY  
* nome — VARCHAR(100)  
* franquia\_anime — VARCHAR(100)  
* preco\_venda — NUMERIC(10,2)  
* quantidade\_estoque — INTEGER

### **2\. Usuário**

* id\_usuario — SERIAL PRIMARY KEY  
* nome — VARCHAR(100)  
* email — VARCHAR(100)   
* senha — CHAR(8)

### **3\. Pedidos**

* id\_pedido — SERIAL PRIMARY KEY  
* situacao\_pedido — ENUM(situação)  
* quantidade — INTEGER  
* data\_pedido — TIMESTAMP  
* id\_produto — INTEGER FOREIGN KEY  
* id\_usuario — INTEGER FOREIGN KEY

## **Relacionamentos**

* Produto — Pedidos (1:N): um produto pode ter vários pedidos registradas ao longo do tempo.  
* Usuário — Pedidos (1:N): um usuário pode registrar vários pedidos , e cada pedido fica associada a um usuário.
<img width="1408" height="422" alt="image" src="https://github.com/user-attachments/assets/4689e7a9-fa63-4c82-82d0-b3ee2ac19eda" />

