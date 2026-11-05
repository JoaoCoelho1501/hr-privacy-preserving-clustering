# Clustering com Preservação de Privacidade: Dados de RH

> Proteger dados sensíveis de colaboradores (anonimização, pseudonimização, codificação) e mostrar que o clustering continua a dar os mesmos perfis.

**Mestrado em Business Intelligence & Analytics (ISCAP)**, 2025/26

## O problema
É possível proteger os dados de saídas de colaboradores, como avaliações, motivos de saída e entrevistas, **sem perder a utilidade analítica**?

## Abordagem
1. Dataset **sintético** de 10.000 colaboradores, gerado no próprio notebook. Não tem dados reais.
2. Dicionário de dados com **classificação de sensibilidade** de cada variável.
3. Clustering (K-Means) na base de dados **original**.
4. Base de dados **protegida**: anonimização, pseudonimização (hash) e codificação.
5. Clustering na base de dados **protegida**.
6. Desanonimização interpretativa através de tabelas de mapeamento com acesso restrito.
7. Comparação dos dois resultados com o **Adjusted Rand Index (ARI)**.

## Resultados
O ARI entre os clusters da base original e os da protegida foi **elevado**, por isso os perfis mantiveram-se depois da proteção:
- **Progressão de carreira**: mais jovens, menor antiguidade, avaliação boa.
- **Underperformance**: avaliação mais baixa e entrevistas de saída negativas.
- **Reforma**: mais velhos, maior antiguidade.

## Stack
`pandas` · `scikit-learn` (K-Means, ARI) · `hashlib` · `matplotlib`

## Estrutura
```
notebooks/  processo completo
data/       dataset sintético (10.000 registos)
docs/       relatório
```

## Autores
Débora Jesus · João Coelho
