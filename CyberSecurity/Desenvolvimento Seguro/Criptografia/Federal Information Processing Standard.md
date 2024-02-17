Referência pra validar um hardware criptográfico

# Níveis

São crescentes e qualitativos de segurança

##### Nível 1

Requer equipamento de primeira qualidade e algoritmos testados externamente

##### Nível 2

Agrega requisitos de prova física de violação e autenticação baseada em funções

>[!info]
>As implementações de software devem ser feitas em um SO aprovado de acordo com Common Criteria no EAL2

##### Nível 3

- Adiciona requisitos de resistência física à violação e autenticação baseada em identidade

- Deve haver uma separação física ou lógica entre as interfaces pelas quais parâmetros de segurança fundamentais entram e saem do módulo.

- As chaves privadas só podem entrar ou sair de forma criptografada

##### Nível 4

Apagar o conteúdo do dispositivo se detectar formas de ataque

---
# O que envolve a validação?

Este processo envolve a análise dos seguintes aspectos do producto e da documentação:

- Especificação do módulo criptográfico
- Portas e interfaces do módulo criptográfico
- Papéis, serviços e autenticação
- Modelo de estado finito
- Segurança física
- Ambiente operacional
- Gerenciamento de chaves
- Testes eletromagnéticos EMC[^3]/EMI[^4]
- Autoteste
- Garantia de design
- Mitigação de outros ataques

>[!QUESTION] Isso inclui o software?
>
>Sim, ela se aplica ao módulo como um todo. No caso de um PC executando o programa, o próprio PC, o SO e o Software Criptográfico são considerados parte do módulo

---

# Por que o FIPS é importante?

- Profissionais de segurança da América do Norte, bem como a indústria, reconhecem e procuram produtos certificados para proteger informações confidenciais.

- A maioria das organizações e agências exigem que qualquer novo produto usado para proteger suas informações possuam essa validação

- Os governos federais dos Estados Unidos (NIST[^1]) e Canadá (CSE[^2]) adotaram a FIPS PUB 140-2.

---

[^1]: National Institute of Standards and Technology
[^2]: Communications Security Stablishment
[^3]: Eletromagnetic Compatibility
[^4]: Eletromagnetic Interference