# Modelo Latex (GAMBIARRA) de Tese PPGCC - UFMG

O Modelo para Dissertação e Tese [disponibilizado](https://ppgcc.dcc.ufmg.br/informacoes-para-alunos/) pelo PPGCC/UFMG, não atende às [diretrizes de normalização](https://repositorio.ufmg.br/static/politica/diretrizes-para-normalizacao-de-trabalhos-academicos-da-UFMG.pdf) atuais (em 2021) do Repositório Institucional da UFMG.
Eu tinha escrito a minha tese de doutorado em Latex utilizando o template citado, mas ela foi rejeitada pelo Repositório da UFMG por não seguir as diretrizes atuais.

Eu conversei então com o [Vilar Neto](https://bitbucket.org/vilarneto/ppgccufmg) que mantinha um repositório com uma versão (inclusive mais atual) do template PPGCC/UFMG, e ele me informou que seriam necessárias muitas alterações no template, devido ao grande número de modificações das novas diretrizes.
Para conseguir entregar [minha tese](https://repositorio.ufmg.br/handle/1843/38570), eu fiz então várias alterações, ou **gambiarras** como preferir, no arquivo `ppgccufmg.cls` e tive que colocar algumas linhas adicionais no meu arquivo `.tex`.

Depois disso, o Marcelo Pita, também aluno do PPGCC, já me procurou para saber como eu tinha feito as adaptações na minha tese e eu forneci a ele o arquivo `ppgccufmg.cls` alterado e as duas linhas que incluí no meu arquivo `.tex`. Ele depois me reportou que o arquivo modificado o poupou de um grande trabalho.

Resolvi então criar este repositório para facilitar o compartilhamento deste arquivo.
Gostaria, entretanto, de ressaltar que conheço de latex apenas o suficiente para escrever meu próprio texto (e mesmo assim com muita ajuda do Google, Stack Overflow, etc.) e, portanto, **não tenho condições de fornecer suporte ou disponibilizar alterações adicionais no arquivo disponibilizado**.

## Para usar o Modelo Gambiarra

1. Use o arquivo `ppgccufmg.cls` que tem as minhas alterações (gambiarras).

2. É necessário adicionar as linhas abaixo no seu próprio arquivo `.tex`, imediatamente **antes** do capítulo de introdução. Lembre-se de alterar o número da página, de acordo com o seu documento.

```
\setcounter{page}{26}
\makeoddhead{chapter}{}{}{\thepage}
```

3. Quando o Marcelo utilizou este modelo, ele tinha escrito sua tese em inglês e com epígrafe e, por isso, precisou fazer as seguintes modificações adicionais:

- Remover *na marra* a folha de rosto para a versão em inglês (pois apareciam duas folhas de rosto).
- Acrescentar um comando para omitir o número de página da epígrafe, similar ao que eu tinha feito para as demais seções.

**IMPORTANTE**:
- Não há nenhuma garantia de que o modelo atende às diretrizes. Posso dizer apenas que ele foi utilizado com sucesso por mim e pelo Marcelo.
- O arquivo não foi testado para dissertações ou projetos de tese, então pode ser que sejam necessárias modificações adicionais.
- Como já mencionado, não tenho condições fazer alterações no arquivo disponibilizado.

De toda forma, espero que este repositório possa ser útil.


## Alterações feitas no arquivo `ppgccufmg.cls`

Para saber exatamente o que eu fiz talvez o mais prático seja ver o [diff para a versão 1.60][issue1] do modelo (contribuição de [@renatolfc](https://github.com/renatolfc)).

[issue1]: https://github.com/caburu/modelo-ppgccufmg/issues/1

Mas a maioria das alterações possui uma linha de comentário com o meu nome. Obs.: na correria para entregar a tese, não garanto que lembrei de colocar comentário em todas elas.
