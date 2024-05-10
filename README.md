## Sistema de Detecção de Roubo de Carga

### Descrição

Este sistema visa combater o roubo de carga através da monitorização do peso e tipo de veículo em pontos de saída específicos.

### Funcionamento

1. **Verificação de Peso:**

    * Ao sair do local, o veículo passa por uma balança rodoviária.
    * **Carreta carregada:**
        * Se o peso registrado for compatível com a carga, a saída é liberada.
        * Caso contrário, há indício de desvio de carga e a equipe de segurança é acionada.
    * **Carreta vazia ou outro tipo de veículo:**
        * A saída é liberada automaticamente.

2. **Captura de Imagem:**

    * Uma câmera na portaria captura uma foto do veículo ao detectar movimento.
    * A foto é salva no banco de dados.

3. **Análise de Imagem:**

    * A imagem é enviada para o **GEMINI**, um sistema de inteligência artificial, para identificar o tipo de veículo.
    * **Caminhão:**
        * Se confirmado, o **GEMINI** verifica se o veículo está carregado.
        * **Vazio:**
            * A saída na cancela é liberada.
        * **Carregado:**
            * O sistema consulta o banco de dados para verificar se o veículo foi pesado e se a nota fiscal foi emitida.
            * **Pesado com nota fiscal:**
                * A saída na cancela é liberada.
            * **Não pesado ou sem nota fiscal:**
                * A equipe de segurança patrimonial é acionada para investigar o possível desvio de carga.

### Benefícios

* Reduz o índice de roubo de carga.
* Agiliza o processo de liberação de saída para veículos em situação regular.
* Permite a identificação rápida de veículos suspeitos.

### Componentes

* Balança rodoviária.
* Câmera.
* Sistema **GEMINI** de inteligência artificial.
* Banco de dados com informações de pesagem e notas fiscais.
* Cancel
