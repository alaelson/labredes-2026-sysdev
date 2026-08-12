# Laboratório de Sistemas Operacionais e Redes (LSOR) — BSI 2026.02

Repositório oficial para a organização e acompanhamento das práticas de laboratório da disciplina **Laboratório de Sistemas Operacionais e Redes (LSOR)** do curso de **Bacharelado em Sistemas de Informação (BSI)** no **Instituto Federal de Alagoas (IFAL) - Campus Maceió**, para o semestre letivo **2026.02** [48].

Esta disciplina tem natureza eminentemente prática e aplicada, na qual cada conceito de redes e sistemas operacionais é transformado em configuração, teste, diagnóstico e documentação técnica [66, 67].

---

## 💻 Informações Gerais do Laboratório

Para manter a padronização das práticas, a compatibilidade de redes e a segurança nos testes, adotamos as seguintes diretrizes de ambiente de hardware e credenciais:

*   **Hipervisor:** [VirtualBox](https://www.virtualbox.org/) (com o respetivo *Extension Pack* instalado no hospedeiro) [38, 70].
*   **Sistema Operacional Guest:** Ubuntu Server 26.04 LTS (64-bit) [1].
*   **Hardware Padrão da VM:** 512 MB de Memória RAM, 1 CPU Virtual e 32 GB de Disco Rígido (VDI, Alocação Dinâmica) [2].
*   **Usuário Administrativo Padrão:** `administrador` *(Nota: o usuário 'redes' do semestre anterior não é utilizado neste laboratório)*.
*   **Senha de Laboratório:** `adminifal` [36].

### 📁 Estrutura de Diretórios no Host (Windows do Laboratório)
*   **Armazenamento de ISOs originais:** `D:\2026\BSI\VM\original` [1].
*   **Diretório de Trabalho do Aluno:** `D:\2026\BSI\VM\<NomeDoAluno>` [1].

---

## 📚 Roteiros das Aulas Práticas

Os links abaixo apontam para os roteiros detalhados de cada prática realizada em laboratório. Cada roteiro contém as explicações conceituais, os comandos necessários e os testes de validação exigidos.

1.  **[Aula 01: Instalação e Configuração Básica do Ubuntu Server](Aula1.md)**
    *   Criação de VM no VirtualBox [2].
    *   Particionamento avançado de disco usando LVM: `/` (29 GB), `/boot` (1 GB) e `SWAP` (2 GB) [22].
    *   Primeiro boot, atualização de repositórios (`apt-get update`) e verificação de conectividade básica [13, 38].
2.  **[Aula 02: Administração de Usuários, Grupos e Permissões](Aula2.md)**
    *   Criação e gerenciamento de contas de usuários (`fulano`, `cicrano`, `beltrano` e `novato`).
    *   Criação de grupos de trabalho (`devs`) e atribuição de membros.
    *   Configuração fina de permissões em diretórios compartilhados (`chown`, `chgrp`, `chmod`).
    *   Testes de controle de acesso local e isolamento de segurança.
3.  *Aula 03: Interfaces e Endereçamento de Rede (Em breve)*
4.  *Aula 04: Configuração de Acesso Remoto Seguro com OpenSSH (Em breve)*
5.  *Aula 05: Conectividade Avançada via Rede Host-Only no VirtualBox (Em breve)*
6.  *Aula 06: Configuração de Nomes Estáticos de Host (Em breve)*
7.  *Aula 07: Implantação de Rede Virtual Privada com OpenVPN (Em breve)*

---

## 📝 Diretrizes para Entrega de Relatórios Técnicos

Como parte do comportamento profissional esperado na disciplina, todas as práticas de laboratório devem ser documentadas individualmente pelos alunos em seus respectivos repositórios pessoais no GitHub [62, 86].

Os relatórios devem seguir estritamente o **Modelo de 7 Passos** estabelecido [87]:

1.  **Identificação:** Nome completo, matrícula, turma, data e título da prática [87].
2.  **Objetivo:** Explicação clara do serviço ou configuração que se pretendia realizar [87].
3.  **Ambiente:** Detalhamento do cenário de testes (especificações da VM, endereços IP, etc.) [87].
4.  **Procedimento:** Descrição passo a passo dos comandos executados e arquivos de configuração modificados [87].
5.  **Testes:** Evidências de funcionamento (capturas de tela, saídas de comandos como `ping`, `ip addr`, etc.) [87].
6.  **Problemas e Soluções:** Registro de quaisquer erros encontrados durante a prática e como foram solucionados [87].
7.  **Conclusão:** Reflexão sobre o que foi validado e aprendido na atividade [87].

---

## 🛠️ Dicas de Laboratório e Solução de Problemas

*   **Teclado Desconfigurado no Console:** Caso o layout do seu teclado esteja incorreto no terminal virtual da VM, configure-o para o padrão brasileiro ABNT2 com o comando:
    ```bash
    sudo dpkg-reconfigure keyboard-configuration
    ```
*   **Isolamento no VirtualBox:** Ao realizar configurações de rede interna, lembre-se de que o modo *Host-Only* permite que a sua máquina real acesse a máquina virtual, mas impede que ela acesse a internet pública diretamente sem um serviço de NAT ou roteamento ativado.

---

## 📖 Referências Bibliográficas Recomendadas

*   LACROIX, Jay. **Mastering Ubuntu Server**. 4. ed. Packt Publishing, 2023 [93].
*   SOYINKA, Wale. **Linux Administration: A Beginner's Guide**. 8. ed. McGraw-Hill, 2020 [93].
*   KUROSE, James F.; ROSS, Keith W. **Redes de Computadores e a Internet**. 8. ed. Pearson, 2022 [93].
