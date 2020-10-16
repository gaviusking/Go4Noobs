[← Pagina Inicial](../README.md#go4noobs)

# Regexp Cheat sheet

| Token | Descrição |
|-------|-----------|
| `\n` | Corresponde a um caractere de nova linha |
| `\r` | Corresponde a um caractere de retorno de cursor, caractere Unicode 2185. |
| `\t` | Corresponde a um caractere de tabulação. Historicamente, as paradas de tabulação acontecem a cada 8 caracteres. |
| `\0` | Corresponde a um caractere nulo, geralmente representado visualmente em Unicode usando U+2400. |
| `[abc]` | Corresponde a um caractere `a`, `b` ou `c`. |
| `[^abc]` | Corresponde a qualquer caractere, exceto para um `a`, `b` ou `c`. |
| `[a-z]` | Corresponde a qualquer caractere entre `a` e `z`, incluindo `a` e `z`. |
| `[^a-z]` | Corresponde a qualquer caractere, exceto aqueles no intervalo `a-z`. |
| `[a-zA-Z]` | Corresponde a qualquer caractere entre `a-z` ou `A-Z`. Você pode combinar o quanto quiser. |
| `[[:alnum:]]` | Uma forma alternativa de corresponder a qualquer letra ou dígito. Equivalente a `[A-Za-z0-9]`. |
| `[[:alpha:]]` | Uma maneira alternativa de combinar letras do alfabeto. Equivalente a `[A-Za-z]`. |
| `[[:ascii:]]` | Corresponde a qualquer caractere no intervalo ASCII válido. Equivalente a `[-]`. |
| `[[:blank:]]` | Corresponde espaços e tabulações (mas não novas linhas). Equivalente a `[ ]`. |
| `[[:cntrl:]]` | Corresponde a caracteres que geralmente são usados ​​para controlar a apresentação de texto, incluindo novas linhas, caracteres nulos, tabulações e o caractere de escape. Equivalente a `[\x00-\x1F\x7F]`. |
| `[[:digit:]]` | Corresponde a dígitos decimais. Equivalente a `[0-9]`. |
| `[[:graph:]]` | Corresponde apenas a caracteres imprimíveis, sem espaço em branco e sem incluir caracteres de controle. Equivalente a `[!-~]`. |
| `[[:lower:]]` | Corresponde a letras minúsculas. Equivalente a `[a-z]`. |
| `[[:print:]]` | Corresponde a caracteres imprimíveis, parte do conjunto latino básico, como letras e espaços, sem incluir caracteres de controle. |
| `[[:punct:]]` | Corresponde a caracteres que não sejam espaços em branco, letras ou números. |
| `[[:space:]]` | Corresponde a caracteres de espaço em branco. Equivalente a `\s`. |
| `[[:upper:]]` | Corresponde a letras maiúsculas. Equivalente a `[A-Z]`. |
| `[[:word:]]`  | Corresponde letras, números e sublinhados. Equivalente a `\w` ou `[a-zA-Z0-9_]`. |
| `[[:xdigit:]]` | Corresponde a dígitos hexadecimais, não diferencia maiúsculas de minúsculas. Equivalente a `[0-9a-fA-F]`. |
| `[[:<:]]` | Este equivalente POSIX do limite da palavra `\\b` é interpretado como `\b(?=\W)` |
| `[[:>:]]` | Este equivalente POSIX do limite de palavra `" \b "` é interpretado como `\\b(?<=\\w)` |
| `.` | Corresponde a qualquer caractere diferente de nova linha (ou incluindo nova linha com o sinalizador `/s`) |
| `\s` | Corresponde a qualquer espaço, tabulação ou caractere de nova linha. |
| `\S` | Corresponde a qualquer coisa diferente de um espaço, tabulação ou nova linha. |
| `\d` | Corresponde a qualquer dígito decimal. Equivalente a `[0-9]`. |
| `\D` | Matches anything other than a decimal digit. |
| `\w` | Corresponde a qualquer letra, dígito ou sublinhado. Equivalente a `[a-zA-Z0-9_]`. |
| `\W` | Corresponde a qualquer coisa diferente de uma letra, dígito ou sublinhado. |
| `\v` | Corresponde a novas linhas e guias verticais. Funciona com Unicode. As guias verticais podem ser inseridas em alguns processadores de texto usando `CMD/CTRL+ENTER`. |
| `\pX` | Corresponde a um caractere Unicode com a [propriedade fornecida](http://www.fileformat.info/info/unicode/category/index.htm). |
| `\p{...}` | Corresponde a um caractere Unicode com o determinado grupo de [propriedades](http://www.fileformat.info/info/unicode/category/index.htm) ou [categorias](http://www.regular-expressions.info/unicode.html#category).
| `\PX` | Corresponde a um caractere Unicode sem a propriedade fornecida. |
| `\P{...}` | Corresponde a um caractere Unicode que não possui nenhuma das propriedades fornecidas. |
| `\Q...\E` | Quaisquer caracteres entre `\Q` e `\E`, incluindo metacaracteres, serão tratados como literais. |
|  |