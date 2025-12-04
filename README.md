# PerformanceTestAgiBank

Este repositório contém o projeto de testes de performance da AgiBank, desenvolvido utilizando o Apache JMeter.

## Objetivo

Avaliar o desempenho e a estabilidade das aplicações da AgiBank simulando cargas reais de acesso, identificando possíveis gargalos, tempos de resposta e comportamento sob diferentes níveis de estresse.

## Ferramentas Utilizadas

- [Apache JMeter](https://jmeter.apache.org/): Ferramenta de código aberto para testes de performance.
- Java 8 ou superior

## Estrutura do Projeto

- `jmx/` — Scripts dos planos de teste JMeter (`.jmx`).
- `results/` — Relatórios e logs gerados após a execução dos testes.
- `docs/` — Documentação dos cenários, evidências, e instruções adicionais.

## Como Executar os Testes

### Pré-requisitos

- Java instalado (`java -version`)
- Apache JMeter instalado ([Download aqui](https://jmeter.apache.org/download_jmeter.cgi))

### Passos

1. Clone este repositório:
    ```bash
    git clone https://github.com/GabrielMeloQA/PerformanceTestAgiBank.git
    cd PerformanceTestAgiBank
    ```
2. Abra o script de teste desejado no JMeter GUI ou execute via linha de comando:
    ```bash
    jmeter -n -t jmx/teste_performance.jmx -l results/resultados.jtl -e -o results/relatorio
    ```
   - `-n` modo não-interativo
   - `-t` caminho para o arquivo `.jmx`
   - `-l` arquivo de saída com os resultados
   - `-e -o` gera relatório HTML

3. Visualize o relatório na pasta `results/relatorio/index.html`.

## Cenários de Teste

Os principais cenários contemplados são:

- Teste de carga: avalia o tempo de resposta sob número crescente de usuários.
- Teste de estresse: identifica o limite máximo suportado pela aplicação.
- Teste de pico: simula grandes volumes de acesso em curtos períodos.
- Teste de longa duração (soak test): verifica estabilidade ao longo do tempo.
- Teste de throughput: avalia a quantidade de transações processadas por segundo.

## Como Contribuir

1. Faça um fork deste repositório.
2. Crie um branch: `git checkout -b feature/novo-cenario`
3. Submeta um Pull Request descrevendo sua contribuição.

## Referências

- [Documentação oficial do JMeter](https://jmeter.apache.org/usermanual/index.html)
- [Boas práticas em testes de performance (PT-BR)](https://pt.wikipedia.org/wiki/Teste_de_performance)
- [Exemplo de relatório JMeter Dashboard](https://jmeter.apache.org/usermanual/generating-dashboard.html)

---

**Autor:** Gabriel Melo  
**Contato:** [linkedin.com/in/gabrielmeloqa](https://linkedin.com/in/gabrielmeloqa)
