# estudos_ciberseguranca
Este repositório documenta a execução de um cenário controlado de testes de intrusão focados na exploração de credenciais fracas no protocolo SMB (Server Message Lock), utilizando uma máquina Kali contra um alvo propositalmente vulnerável (Metasploitable 2).

## Sumário
1- [Objetivo](#-objetivo)
2- [Arquitetura do laboratório](#-arquitetura-do-laboratório)
3- Metodologia:
   Passo 1: Reconhecimento e Validação de Rede
   Passo 2: Preparação de Wordlists
   Passo 3: Execução de Força Bruta com Medusa
   Passo 4: Validação do Acesso com smbclient
4- Mitigação e Defesa

## Objetivo
Demonstrar na prática como a gestão inadequada de credenciais e a utilização de senhas fracas acabam expondo os sistemas a ataques de força bruta automatizados, permitindo assim o comprometimento de recursos partilhados na rede interna.

## Arquitetura

O ambiente foi isolado em uma infraestrutura virtualizada utilizando o Oracle VirtualBox:

* **Máquina Atacante (Kali Linux):** Responsável pela fase de reconhecimento e pela execução dos ataques.
* **Máquina Alvo (Metasploitable 2):** Máquina configurada propositalmente com vulnerabilidades.
* **Rede:** Isolação via adaptador Host-Only para um ambiente totalmente seguro.
