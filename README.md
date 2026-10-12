# Automação de Relatório de Vendas com Python

Projeto que automatiza uma tarefa diária de um analista: baixar a base de vendas do dia anterior, calcular os indicadores principais e enviar um e-mail para a diretoria com o resultado.

## O que o código faz

1. Abre o navegador e acessa o sistema da empresa (uma pasta no Google Drive)
2. Navega até a base de vendas e faz o download do arquivo Excel
3. Lê a base com **pandas** e calcula:
   - Faturamento total (soma da coluna `Valor Final`)
   - Quantidade de produtos vendidos (soma da coluna `Quantidade`)
4. Abre o Gmail e envia um e-mail com esses indicadores

A automação de mouse e teclado é feita com **pyautogui**, e o texto do e-mail é colado com **pyperclip** para preservar acentos.

## Tecnologias

- Python
- Jupyter Notebook
- pandas e openpyxl (análise de dados e leitura de Excel)
- pyautogui (automação de mouse e teclado)
- pyperclip (área de transferência)

## Como executar

```bash
pip install -r requirements.txt
```

Depois, abra `automacao-relatorio-vendas.ipynb` no VS Code ou no Jupyter e execute as células em ordem.

> **Atenção:** as coordenadas de clique (`x`, `y`) dependem da resolução e do layout da sua tela. Use a última célula do notebook (`pyautogui.position()`) para descobrir as posições corretas no seu computador. Ajuste também o caminho do arquivo Excel baixado.

## Créditos

Projeto desenvolvido durante o curso da Hashtag Treinamentos.
