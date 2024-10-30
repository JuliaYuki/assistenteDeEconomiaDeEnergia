# Assistente de Economia de Energia

### Usar Portugol Webstudio para rodar o código abaixo: [Portugol](https://portugol.dev/)

```plaintext
programa {
  funcao inicio() {
    // Programa feito no Portugol WebStudio
    inteiro quantidadeAparelhos // Variável para armazenar a quantidade de aparelhos
    real consumoTotal = 0.0 // Variável para armazenar o consumo total mensal

    // Solicita ao usuário a quantidade de aparelhos a serem cadastrados
    escreva("Quantos aparelhos deseja cadastrar? ")
    leia(quantidadeAparelhos)

    // Loop para cadastrar cada aparelho
    para (inteiro i = 1; i <= quantidadeAparelhos; i++) {
      real consumoPorHora, horasPorDia, consumoMensal

      escreva("\nAparelho ", i, ":")

      // Solicita e lê o consumo do aparelho em watts por hora
      escreva("\nConsumo em watts por hora: ")
      leia(consumoPorHora)

      // Solicita e lê as horas de uso do aparelho por dia
      escreva("\nHoras de uso por dia: ")
      leia(horasPorDia)

      // Calcula o consumo mensal do aparelho em kWh
      consumoMensal = consumoPorHora * horasPorDia * 30 / 1000
      consumoTotal += consumoMensal // Adiciona o consumo mensal ao total

      // Exibe o consumo mensal aproximado do aparelho
      escreva("Consumo mensal aproximado: ", consumoMensal, " kWh\n")
    }
    
    // Exibe o consumo total mensal
    escreva("\nConsumo total mensal: ", consumoTotal, " kWh\n")

    // Verifica se o consumo total é maior que 100 kWh e exibe dicas de economia
    se(consumoTotal > 100){
      escreva("\nDica de economia:\n")
      escreva("- Desligue aparelhos em standby para economizar energia.\n")
      escreva("- Reduza o tempo de uso de aparelhos de alto consumo.\n")
      escreva("- Considere trocar por aparelhos mais eficientes energeticamente.\n")
    } senao {
      escreva("\nSeu consumo está dentro de um nível eficiente. Continue assim.\n")
    }
  }
}

````

## 1. Problemática Identificada

Com o aumento dos custos de energia e a preocupação com o meio ambiente, as pessoas estão buscando formas de reduzir seu consumo elétrico em casa. Mas, sem uma ferramenta de acompanhamento, é difícil saber quanto cada aparelho consome e onde dá para economizar. A ideia deste projeto é criar um programa que ajude o usuário a entender e controlar melhor o consumo de energia dos aparelhos, dando mais clareza sobre o que está usando mais eletricidade e sugerindo mudanças para reduzir o consumo.

## 2. Funcionamento do Programa

O **Assistente de Economia de Energia** é um programa onde o usuário insere informações sobre os aparelhos que utiliza, como:
- O consumo médio do aparelho em watts por hora.
- Quantas horas por dia o aparelho fica ligado.

Com esses dados, o programa calcula o consumo mensal estimado de cada aparelho, mostra o total de consumo da casa e, se esse consumo for alto (mais de 100 kWh no mês, por exemplo), oferece algumas dicas práticas para economizar.

### Como o programa funciona
1. **Entrada de Dados:** O usuário insere quantos aparelhos quer analisar e os dados de cada um.
2. **Processamento:** O programa calcula o consumo mensal de cada aparelho e o total mensal.
3. **Saída de Dados:** Mostra o consumo de cada aparelho, o total mensal e dá sugestões de economia se o consumo for alto.




## 3. Exemplos de Uso

### Exemplo 1:
**Entrada:**
- Quantidade de aparelhos: 2
  - Aparelho 1: Consumo de 1500 W/h e 3 horas de uso diário.
  - Aparelho 2: Consumo de 60 W/h e 5 horas de uso diário.

**Saída:**
```plaintext
Aparelho 1:
Consumo mensal aproximado: 135.0 kWh

Aparelho 2:
Consumo mensal aproximado: 9.0 kWh

Consumo total mensal: 144.0 kWh

Dicas de economia:
- Desligue aparelhos em standby para economizar energia.
- Reduza o tempo de uso de aparelhos de alto consumo.
- Considere trocar por aparelhos mais eficientes energeticamente.
```
## 4. Potenciais Melhorias Futuras

1. **Interface Gráfica (GUI):** Transformar o programa em uma aplicação com interface gráfica (telas e botões), facilitando o uso para quem não tem experiência com linha de comando.

2. **Banco de Dados de Aparelhos:** Incluir uma lista de aparelhos com o consumo médio de cada um, facilitando o preenchimento dos dados para o usuário.

3. **Notificações de Economia:** Enviar alertas automáticos quando o consumo estiver alto ou próximo do limite definido pelo usuário.

4. **Customização de Dicas:** Oferecer recomendações personalizadas com base nos aparelhos e padrões de uso de cada pessoa.

5. **Agente de Monitoramento com IA:** Integrar uma IA que monitore o consumo diariamente, identificando padrões e sugerindo economias em tempo real. A IA poderia, por exemplo, alertar o usuário sobre aumentos incomuns no consumo e enviar dicas específicas para reduzir a energia.

6. **Chatbot de Assistência com IA:** Criar um chatbot interativo para que o usuário possa tirar dúvidas sobre consumo e economias a qualquer momento, recebendo respostas automáticas e sugestões práticas de um assistente virtual.

