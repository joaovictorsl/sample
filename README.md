# O que cada diretório contém?

`analysis` - Notebooks

`analysis/util` - Funções para plot ou processamento de dados que podem ser reutilizadas entre análises

`dashboard` - Dashboards do JMeters

`scripts` - Scripts utilizados para execução do teste, exceto aqueles que são puramente utilizados para automação da execução do teste, presentes no repositório `stress-testing-automation`

`tests` - Arquivos de teste, JMX

`docs` - Documentações

# Sobre documentação

Para documentar um arquivo, siga o seguinte padrão de organização de pastas: o caminho para o arquivo que será documentado deve corresponder ao caminho relativo a partir da raiz do projeto, mas dentro da pasta docs.

Exemplo:  
Se você deseja documentar um arquivo que está localizado em `analysis/util`, a documentação correspondente deve ser colocada em `docs/analysis/util`.

Assinaturas de funções Python devem possuir anotações de tipo

Funções devem possuir exemplo de uso

## Template para documentação de scripts
```md
# [NOME DO SCRIPT]

## PRÉ REQUISITOS

[Liste as dependências necessárias para utilizar seu script]

## USO

[Enumere o passo a passo para utilizar o seu script]

## ARGUMENTOS

[Liste e descreva o que cada argumento faz e se ele é obrigatório ou não]

## EXEMPLOS

[Liste exemplos sobre como utilizar seu script]
```

## Template para documentação de funções
```python
    def sua_funcao(parametro1: tipo_parametro1, parametro2: tipo_parametro2) -> tipo_retorno:
        """
        [Breve descrição da função]

        @param parametro1: [Descrição do primeiro parâmetro]
        @param parametro2: [Descrição do segundo parâmetro]

        @return tipo_retorno: [Descrição do valor de retorno, se houver]

        Exemplos:
        >>> sua_funcao(1, 2)
        resultado_do_exemplo

        >>> sua_funcao('a', 'b')
        resultado_do_exemplo

        Notas:
        [Informações adicionais, se necessário]
        """
        # Código da função aqui
        # Pode incluir comentários para explicar o código

        return valor_de_retorno
```

# Sobre releases

Releases marcam um **ciclo de análise concluído**

Releases são criadas quando:
- Teste de um diferente aspecto da aplicação foi adicionado

- Um novo teste foi aplicado para duas versões diferentes da aplicação (quando sair uma nova versão da aplicação deve haver uma nova análise)

Releases devem possuir:
- Responsáveis pela análise

- Versões da aplicação envolvidas na análise

- Link para os dados

- Link para o plano de teste

## Template para Releases
```md
**[SPRINT] - [TÍTULO DO RELEASE]**

**Data:** [Data da conclusão da análise]  
**Responsáveis pela análise:** [Nomes dos Responsáveis pela Análise]  
**Versões da aplicação:** [Versões da Aplicação Envovidas na Análise]  
**Link para os dados:** [Link para os dados]  
**Link para o plano de teste:** [Link para o plano de teste]  

**Descrição:**
[Descrição do que foi feito nessa release]

**Resultados e Conclusões:**
[Resultados e conclusões sobre a análise em bullet points]
```

# Boas práticas

- Em nosso contexto, uma release é um snapshot de uma análise, portanto **mantenha apenas os arquivos utilizados**. O intuito dessa abordagem é facilitar a replicação dessa análise. Arquivos de releases passadas estão armazenados no commit daquela release

- Testes o mais parametrizáveis possíveis

- **Sempre** exportar logs do teste

- **Sempre** gerar dashboard do JMeter para métricas do cliente

- Métricas do servidor devem ser analisadas a partir dos logs em um notebook

- Utilizar Pandas

- Utilizar Matplotlib + Seaborn

- Documentar e anotar os tipos na assinatura das funções em Python

# Revisando notebooks

Para revisar notebooks utilize o [GitNotebook](https://gitnotebooks.com/)