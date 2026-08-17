# Heitor Abreu Ramos/ RA: 4251922978

Nivel 1: O que o Codigo Faz?

A)  Esse  código é uma função que verifica se o texto é uma palavra ou frase que se lê igual de trás para frente, ou seja se é um palíndromo
​
Como funciona?

Respostas: 
​Tratamento: Remove espaços, pontuações e caracteres especiais, mantendo apenas letras/números e convertendo tudo para minúsculas.

​Inversão: Inverte a ordem do texto limpo.

​Validação: Retorna True se o texto limpo for idêntico ao invertido, ou False se forem diferentes.

B) O que é um palíndromo?

Resposta:

Um palíndromo é uma palavra, frase ou número que pode ser lido da mesma forma tanto da esquerda para a direita quanto da direita para a esquerda, ignorando espaços, acentos e pontuações.

Nivel 2: Como Executar?

Resposta:

Primeiramente, devo  Corrigir o erro na linha 17.

obs: Antes de executar, devo arrumar a quebra de linha da variável (texto2).

​Deixando a frase inteira na mesma linha:

 texto2 = "Socorram-me, subi no ônibus em Marrocos"
​
- Logo em seguida devo  Copiar o código corrigido e pedir para o  Copilot executar em na liguagem de Python.

- Sendo assim a saida será exibida como:

Exemplo:

text

teste 1: true 
teste 2: true

Nivel 3: Exemplo de Saida:


A) O método analisar(entrada) verifica se uma string de entrada é um palíndromo através das seguintes etapas:

- ​Tratamento de nulos: A primeira linha (if entrada is None: return False) verifica se o parâmetro recebido é nulo, retornando False imediatamente para evitar erros de execução.

- ​Sanitização da string: A instrução re.sub(r'[^a-zA-Z0-9]', '', entrada).lower() 

* utiliza expressão regular para remover todos os caracteres que não sejam letras sem acento ou números (como espaços, hífens e vírgulas). Em seguida, converte todo o texto para letras minúsculas (.lower()), garantindo uma comparação padronizada.

- ​Inversão: O fatiamento limpa[::-1] cria uma nova string com os caracteres da frase sanitizada em ordem invertida.

- ​Validação: A instrução return limpa == invertida compara a string tratada com sua versão invertida, retornando True se forem idênticas (caracterizando um palíndromo) ou False caso contrário.

B) Misterio dos testes:

​Resposta:

​A função valida se o texto é um palíndromo após remover espaços, pontuações e padronizar o texto em minúsculas. 

-O comportamento de cada teste ocorre pelos seguintes motivos:

​•Teste 1 (False): A frase "A sacada da casa de cadasa" contém um erro de digitação na palavra final ("cadasa" em vez de "casa"). Após a remoção de espaços e a conversão para minúsculas, obtém-se a string asacadadacasadecadasa.
- Ao invertê-la, o resultado é asadacedasacadacasa. 

- Como as strings não são idênticas, a função retorna False.
• ​Teste 2 (True): A frase "Socorram-me, subi no ônibus em Marrocos" é um palíndromo. Após a sanitização — que remove o hífen, a vírgula e os espaços —, a string resultante é socorrammesubinoonibusemmarrocos.

- A sua inversão gera exatamente a mesma sequência de caracteres, fazendo com que a verificação de igualdade retorne True.



