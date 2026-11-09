# estudos_ciberseguranca
Este repositório documenta a execução de um cenário controlado de testes de intrusão focados na exploração de credenciais fracas no protocolo SMB (Server Message Lock), utilizando uma máquina Kali contra um alvo propositalmente vulnerável (Metasploitable 2).

## Sumário
* [Objetivo](#-objetivo)
* [Arquitetura do laboratório](#-arquitetura-do-laboratório)
* [Metodologia](#-metodologia)
* [Mitigação e Defesa](#-mitigação-e-defesa)

## Objetivo
Demonstrar na prática como a gestão inadequada de credenciais e a utilização de senhas fracas acabam expondo os sistemas a ataques de força bruta automatizados, permitindo assim o comprometimento de recursos partilhados na rede interna.

## Arquitetura

O ambiente foi isolado em uma infraestrutura virtualizada utilizando o Oracle VirtualBox:

* **Máquina Atacante (Kali Linux):** Responsável pela fase de reconhecimento e pela execução dos ataques.
* **Máquina Alvo (Metasploitable 2):** Máquina configurada propositalmente com vulnerabilidades.
* **Rede:** Isolação via adaptador Host-Only para um ambiente totalmente seguro.
