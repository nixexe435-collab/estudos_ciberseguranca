# estudos_ciberseguranca
Este repositório documenta a execução de um cenário controlado de testes de intrusão focados na exploração de credenciais fracas no protocolo SMB (Server Message Lock), utilizando uma máquina Kali contra um alvo propositalmente vulnerável (Metasploitable 2).

## Sumário
* [Objetivo](#-objetivo)
* [Arquitetura do laboratório](#-arquitetura-do-laboratório)
* [Relatório técnico detalhado](#-relatório-técnico-detalhado)
* [Metodologia](#-metodologia)
* [Mitigação e Defesa](#-mitigação-e-defesa)

## Objetivo
Demonstrar na prática como a gestão inadequada de credenciais e a utilização de senhas fracas acabam expondo os sistemas a ataques de força bruta automatizados, permitindo assim o comprometimento de recursos partilhados na rede interna.

## Arquitetura do Laboratório
O ambiente foi isolado em uma infraestrutura virtualizada utilizando o Oracle VirtualBox:

* **Máquina Atacante (Kali Linux):** Responsável pela fase de reconhecimento e pela execução dos ataques.
* **Máquina Alvo (Metasploitable 2):** Máquina configurada propositalmente com vulnerabilidades.
* **Rede:** Isolação via adaptador Host-Only para um ambiente totalmente seguro.

## Relatório Técnico Detalhado
A documentação deste projeto foi dividida de forma modular em relatórios específicos por fase de execução:
1- **[Fase 1: Reconhecimento e Mapeamento de Rede](docs/01-reconhecimento.md)**
   * Detecção de hosts ativos e identificação do serviço SMB ('445/tcp') com Nmap.

2- **[Fase 2: Execução de Ataque de Força Bruta](docs/02-forca_bruta.md)**
   * Preparação das wordlists de utilizadores/senhas e automatização das tentativas via Medusa.

3- **[Fase 3: Validação do Acesso e Prova de Conceito (PoC)](docs/03-validacao_poc.md)**
   * Confirmação das credenciais válidas e enumeração de partilhas de rede com smbclient.
