
# Painel de Contratos e Obras

Este pacote contém um painel estático pronto para publicação no GitHub Pages.

## Arquivos

- `index.html`: painel principal.
- `contratos_tratados.csv`: base tratada no nível do contrato.
- `contratos_municipios_rateados.csv`: base expandida por município.
- `rs_municipios.geojson`: malha municipal usada no mapa.
- `municipios_sem_correspondencia_no_geojson.csv`: diagnóstico de municípios da planilha que não foram encontrados no GeoJSON.

## Correções desta versão

- Ranking de empresas em largura inteira.
- Ranking de municípios em largura inteira.
- Nomes longos são encurtados no eixo, mas o nome completo aparece no hover.
- Valores das barras não ficam cortados.
- Mapa sempre mantém todos os municípios do RS visíveis.
- Seleção de uma obra multimunicipal destaca todos os municípios envolvidos.
- Filtros por município, empresa, situação, contrato/obra e período.
- Botão para limpar filtros.

## Metodologia

Contratos com mais de um município foram separados em linhas municipais individuais.

Para mapa e ranking municipal foram criadas três métricas:

1. `valor_rateado_municipio`: divide o valor do contrato pelo número de municípios envolvidos.
2. `valor_integral_envolvido`: atribui o valor integral do contrato a cada município envolvido.
3. `qtd_contratos`: conta o número de contratos em que o município aparece.

A métrica padrão é o valor rateado, pois evita multiplicação artificial dos valores.

## Geração

Data de geração: 11/06/2026 19:20
Data de referência para vencimento: 11/06/2026
