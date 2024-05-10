# imersao_ia




Criando um sistema de detecção de "Roubo de Carga"

O sistema possui um banco de dados com acesso a placas e se o veiculo pesou, puxando por exemplo de um sistema de pesagem de balança rodoviária

Ao sair em um ponto especificio de uma empresa por exemplo, esse local so pode sair veiculo em algumas condições


Carreta carregada     > Se estiver pesado pode sair, caso contrario existe um possível desvio de carga!
Carreta vazia         > Permite a saída
Outro tipo de veiculo > Permite a saída

Dessa forma entao ao sair pela portaria onde existe uma possivel cancela automatizada, o sistema de camera realiza um snapshot ao detectar um movimento na area de interesse da câmera e salva ela no banco de fotos

Nesse caso, simulei com o random, envio a foto para o GEMINI fazer a primeira tratativa em relação a qual o tipo do veículo.

Caso se trata de um "caminhão" faço uma nova tratativa com o GEMINI para identificar se o veículo esta carregado ou nao.

Estando vazio, ja libero a saída na cancela, caso contrario, faço uma consulta no banco de dados relacionado a essa placa pelo ID da foto e consulto se pesou ou não

Caso tenha efetuado a pesagem e a emissão da nota fiscal para transporte, libero a saída. Se o veículo foi pego saindo cheio e sem pesar, aciono a equipe da segurança patrimonial para tratar um possível desvio de carga da empresa!


Fim!
