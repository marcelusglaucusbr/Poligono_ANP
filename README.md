# Poligono_ANP
## Criação automatizada de dados geoespaciais conforme rege o Padrão ANP4C, estabelecido pela Resolução ANP N° 70/2014.

Esse script em Python visa criar automaticamente polígonos delimitadores para áreas de Avaliação, Desenvolvimento e Produção, seguindo as normas vigentes da ANP em 29/11/2023. O script faz uso de diversas bibliotecas, incluindo Pandas e GeoPandas para manipulação de dados e dados geoespaciais, Matplotlib para visualização e Folium para visualização interativa.

O fluxo de trabalho abrange as seguintes etapas principais:

Carregamento de Dados: O script carrega dados geoespaciais em diferenter formatos, como linhas, multilinhas, polígonos ou multipolígonos.
Pré-processamento: verifica o tipo de dado faz ajustes e realiza operações de simplificação e correção de geometrias para garantir que não haja problemas na execução.
Geração do Buffer: Cria buffers ao redor dos dados já em formato de polígono(s) de referência(s) a partir de uma distância específica (ex: 1000 metros).
Criação de um Grid: Gera um grid regular de polígonos múltiplo de 9,375 segundos de arco.
Operações Topológicas: Realiza operações de interseção e dissolução entre o buffer e o grid, criando uma área delimitadora.
Geração de Vértices: Extrai os vértices dos polígonos resultantes e os integra a um novo GeoDataFrame.
Projeções e Visualização: Realiza projeções e cria visualizações das etapas de trabalho para verificação do processo.
Exportação de Dados: Exporta os resultados em formatos shapefiles e Excel para remessa a ANP e em formato GeoPackage para uso de todas as informações em outros aplicativos GIS, caso se deseje realizar adequações manuais.

Adicionalmente há uma etapa não automatizada para realização de operação topológica com polígonos pré-existentes.
Por fim, é importante mencionar que o script está organizado em células, permitindo a execução passo a passo para verificação e ajustes conforme necessário.