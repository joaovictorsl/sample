# O que cada diretório contém?

`analysis` - Notebooks

`analysis/util` - Funções para plot ou processamento de dados que podem ser reutilizadas entre análises

`dashboard` - Dashboards do JMeter gerados automaticamente

`scripts` - Scripts utilizados para execução do teste, exceto aqueles que são puramente utilizados para automação da execução do teste, presentes no repositório `stress-testing-automation`

`tests` - Arquivos de teste, JMX

`docs` - Documentações

# Sobre documentação

Documentar o máximo possível () TODO: ESPECIFICAR MAIS, PADRONIZAR DOCUMENTAÇÃO

Assinaturas de funções devem possuir anotações de tipo

Deve possuir exemplo de uso

O caminho para o arquivo que será documentado deve ser o mesmo caminho em que ele se encontra a partir da raiz do projeto porém em `docs`

Exemplo:  
    Um arquivo em `analysis/util` que será documentado deve ter sua documentação em `docs/analysis/util`

# Sobre releases

Releases marcam um **ciclo de análise concluído**

Releases são criadas quando:
- Teste de um diferente aspecto da aplicação foi adicionado

- Um novo teste foi aplicado para duas versões diferentes da aplicação (quando sair uma nova versão da aplicação deve haver uma nova análise)


Releases devem possuir:
- Responsáveis pela análise

- Versões da aplicação envolvidas na análise

- Link para os dados no Google Drive

- Link para o plano de teste no Google Drive


## Template para Releases

**Sxxyy - [TÍTULO DO RELEASE]**

**Data:** [Data da conclusão da análise]  
**Responsáveis pela Análise:** [Nomes dos Responsáveis pela Análise]  
**Versões da Aplicação:** [Versões da Aplicação Envovidas na Análise]  
**Link para os dados:** [Link para os dados]  
**Link para o plano de teste:** [Link para o plano de teste]  

**Descrição:**
Durante este ciclo de análise, foram realizados testes abrangentes em vários aspectos da aplicação, incluindo [Listar os diferentes aspectos testados, por exemplo: segurança, desempenho, usabilidade]. Além disso, foram feitas análises comparativas entre diferentes versões da aplicação para identificar quaisquer discrepâncias ou melhorias necessárias.

**Resultados e Conclusões:**
Os resultados da análise indicam que a aplicação [Nome da Aplicação] se encontra em um estado satisfatório de acordo com os critérios definidos. Foram identificadas algumas áreas de melhoria, as quais serão priorizadas e incluídas no próximo ciclo de desenvolvimento.

# Boas práticas

- **Sempre** exportar logs do teste

- **Sempre** gerar dashboard do JMeter para métricas do cliente

- Métricas do servidor devem ser analisadas a partir dos logs em um notebook

- Utilizar Pandas

- Utilizar Matplotlib + Seaborn

- Testes o mais parametrizáveis possíveis

- Entre releases **manter apenas os arquivos utilizados**, arquivos de releases passadas estão armazenados no commit daquela release

- Cada release é um snapshot

# Revisando notebooks

Para revisar notebooks utilize o [GitNotebook](https://gitnotebooks.com/)
