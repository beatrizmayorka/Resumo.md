# Resumo sobre alocação de memória/listas/pilhas

### Alocação de memória

<p> Na <strong>alocação estática</strong> o tamanho do vetor é pré-definido antes da execução do programa. O compilador aloca de forma automática quanto do espaço da memória será preciso. Esse tipo de alocação tende a desperdiçar memória, pois o usuário não saberá ao certo quanto de espaço será necessário para armazenar as informações e, dessa forma, irá reservar mais memória do que seria o essencial. </p>
<p> Já na <strong>alocação dinâmica</strong>, a especificação do tamanho do vetor é feita quando o programa está em execução. Isso é feito através da leitura de um arquivo ou da informação digitada pelo usuário. Também é possível aumentar ou diminuir a quantidade de memória alocada. </p><p> Em outro âmbito, é possível explorar três funções que o C possui para tratar a alocação de memória. Abaixo estão: </p>
      <li><strong>Sizeof</strong>: é uma função utilizada para estabelecer o número de bytes para um tipo de dados. Cada compilador possui um número de bytes a ser retornado.</li>
      <li><strong>Malloc</strong>: é uma função usada para alocar um espaço de memória. Ela recebe números inteiros como argumento e esse números correspondem ao número de bytes a serem alocados. No fim, a função retornará um ponteiro do tipo void.</li>
      <li><strong>Free</strong>: serve para liberar o espaço de memória alocado.</li>

### Listas

<p> Estrutura que armazena um conjunto de elementos em sequência. Essa estrutura contém nós interligados por ponteiros, onde o ponteiro apontará para o próximo nó até que esse ponteiro seja Null, o que representará o fim da lista. </p>
<p> A <strong>lista encadeada</strong> está associada a alocação dinâmica de memória. Então, para cada novo elemento na estrutura é alocado um espaço na memória para poder armazená-lo. Sendo assim, o espaço total de memória consumido pela estrutura será equivalente ao número de elementos armazenados nessa memória. Nessa lista, o ponteiro aponta para o primeiro elemento e para percorrer os próximos é preciso seguir o encadeamento. Quando o último elemento da lista retornar Null, significará que não existe um próximo elemento. </p>
<p> Com a <strong>lista circular duplamente encadeada</strong> é possível pecorrer a lista em ambos os lados. Assim, o último elemento da lista tem como próximo o primeio elemento, que terá o último elemento como anterior.
<img src="data:image/png;base64,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" alt="Lista circular duplament encadeada" />


<p><p> 
      <strong>**Vetor</strong> é uma lista, pois possui elementos do mesmo tipo que estão fisicamente na memória um ao lado do outro.
</p></p>

### Pilhas

<p> A pilha é uma forma de organizar um conjunto de elementos através de uma determinada ordem, ou seja, o último elemento do conjunto será sempre o primeiro a sair (a sigla LIFO - Last In, First Out - descreve essa estratégia). </p>
<p> O manuseio da pilha é feito através de cinco operações, dentre elas: </p>
      <li><strong>Push</strong> - empilhar</li>
      <li><strong>Pop</strong> - desempilhar</li>
      <li><strong>Top</strong> - mostra qual elemento está no topo</li>
      <li><strong>isEmpty</strong> - verifica se está vazia</li>
      <li><strong>isFull</strong> - verifica se está cheia</li>

<p><p> 
      <strong>**isFull</strong> é utilizado somente com a estratégia correta. 
</p></p>

<p> Existem duas estratégias usadas para implementar uma pilha, são elas: alocação dinâmica e alocação estática. </p>
      <li><strong>Alocação estática</strong>: utilizará um vetor com tamanho fixo e limitado. Dessa forma, é será possível usufruir da operação * isFull para verificar se o vetor está completo.</li> 
      <li><strong>Alocação dinâmica</strong>: possibilita fazer o empilhamento de elementos enquanto houver memória.</li>
