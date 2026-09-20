# 📅 Senai_LLP_Switch_DiasDoMes

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-brightgreen)
![Contexto](https://img.shields.io/badge/contexto-acad%C3%AAmico%20SENAI%2FFATESG-blue)

## 📌 Sobre o projeto

Programa em Java que informa quantos dias tem um determinado mês, aceitando tanto o número do mês (1 a 12) quanto o nome por extenso em português, e tratando corretamente o caso especial de fevereiro em anos bissextos. Desenvolvido na disciplina de **Linguagem e Lógica de Programação (LLP)** do curso de **Análise e Desenvolvimento de Sistemas do SENAI/FATESG**.

## 🎯 Objetivo

Praticar o uso de `switch/case` para múltiplas decisões (dias por mês) e a implementação da regra matemática de **ano bissexto**, além de trabalhar conversão e validação flexível de entrada (aceitando tanto números quanto texto para o mesmo dado).

## 🛠️ O que foi desenvolvido

Um único programa, `DiasNoMes.java`, que:

- Lê uma entrada de texto que pode ser o número do mês ou seu nome por extenso (em português, incluindo a variação "marco"/"março");
- Tenta primeiro interpretar a entrada como número; se falhar, tenta reconhecê-la como o nome de um mês via `switch`;
- Usa um segundo `switch` para determinar quantos dias tem o mês identificado (31, 30, ou 28/29 no caso de fevereiro);
- Para fevereiro, pergunta o ano e aplica a regra de bissextilidade para decidir entre 28 e 29 dias;
- Informa mensagens de erro específicas para mês inválido, seja por número fora do intervalo ou por texto não reconhecido.

## ⚙️ Como funciona

1. O programa lê a entrada do usuário como uma linha de texto e a normaliza (`trim()` + `toLowerCase()`);
2. Tenta converter a entrada para número com `Integer.parseInt`, dentro de um `try/catch`;
3. Se a conversão falhar (`NumberFormatException`), interpreta a entrada como nome do mês através de um `switch` sobre `String`;
4. Com o número do mês já definido, um segundo `switch` decide a quantidade de dias, com múltiplos `case` agrupados para os meses de mesma duração (31 ou 30 dias);
5. No caso de fevereiro, pede o ano e calcula a bissextilidade com o método auxiliar `ehBissexto`.

Para executar:

```bash
javac DiasNoMes.java
java DiasNoMes
```

## 💻 Tecnologias utilizadas

- **Java (SE)** — linguagem do projeto, sem dependências externas.
- **`java.util.Scanner`** — leitura da entrada do usuário (mês, e ano quando necessário).
- **`switch/case` sobre `String` e sobre `int`** — usados tanto para reconhecer o nome do mês quanto para determinar a quantidade de dias, incluindo o agrupamento de múltiplos `case` para meses com a mesma duração.
- **Tratamento de exceções (`try/catch`)** — usado para diferenciar entrada numérica de entrada textual sem duas rotinas de leitura separadas.
- **Método auxiliar (`ehBissexto`)** — implementa a regra matemática de ano bissexto (divisível por 4, exceto séculos não divisíveis por 400).

## ✅ Principais funcionalidades

- Entrada flexível: aceita tanto o número do mês quanto seu nome por extenso.
- Cálculo correto da quantidade de dias para todos os 12 meses do ano.
- Tratamento especial de fevereiro, considerando anos bissextos.
- Mensagens de erro específicas para entradas inválidas.

## 📚 O que foi aprendido

- Como aceitar formatos de entrada diferentes para o mesmo dado (número ou texto) usando `try/catch` como estratégia de decisão.
- Implementação da regra de ano bissexto a partir da sua definição matemática (divisibilidade por 4, 100 e 400).
- Uso de `switch/case` com múltiplos rótulos por bloco para simplificar decisões repetitivas (meses com 31 ou 30 dias).

## 🎓 Contexto acadêmico

Este projeto está entre os **primeiros repositórios que publiquei no GitHub** durante minha formação em **Análise e Desenvolvimento de Sistemas no SENAI/FATESG**. Ele documenta uma etapa inicial da minha evolução como desenvolvedor, com foco em consolidar estruturas de seleção múltipla e regras de negócio baseadas em cálculo (como a bissextilidade), antes de avançar para conceitos mais complexos em projetos posteriores.

## ⚠️ Observações

É um programa de console simples e sem persistência de dados, focado exclusivamente na lógica de decisão sobre meses e dias — sem interface gráfica, testes automatizados ou tratamento de exceções para todos os casos possíveis de entrada (por exemplo, um ano não numérico para fevereiro interromperia o programa), o que é esperado em um exercício introdutório de lógica de programação.

## 👤 Autor

**João Pedro Abdala** — estudante de Análise e Desenvolvimento de Sistemas (SENAI/FATESG)
[github.com/joaoabdala05](https://github.com/joaoabdala05)
