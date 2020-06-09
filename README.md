# Resumo sobre alocação de memória/listas/pilhas

### Alocação de memória

<p> Na alocação estática o tamanho do vetor é pré-definido antes da execução do programa. O compilador aloca de forma automática quanto do espaço da memória será preciso. Esse tipo de alocação tende a desperdiçar memória, pois o usuário não saberá ao certo quanto de espaço será necessário para armazenar as informações e, dessa forma, irá reservar mais memória do que seria o essencial. </p>
<p> Já na alocação dinâmica, a especificação do tamanho do vetor é feita quando o programa está em execução. Isso é feito através da leitura de um arquivo ou da informação digitada pelo usuário. Também é possível aumentar ou diminuir a quantidade de memória alocada. </p><p> Em outro âmbito, é possível explorar três funções que o C possui para tratar a alocação de memória. Abaixo estão: </p>
      <li> **Sizeof** : é uma função utilizada para estabelecer o número de bytes para um tipo de dados. Cada compilador possui um número de bytes a ser retornado. </li>
      <li> **Malloc** : é uma função usada para alocar um espaço de memória. Ela recebe números inteiros como argumento e esse números correspondem ao número de bytes a serem alocados. No fim, a função retornará um ponteiro do tipo void. </li>
      <li> **Free** : serve para liberar o espaço de memória alocado.  </li>
