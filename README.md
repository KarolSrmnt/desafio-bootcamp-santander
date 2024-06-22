
# Release notes

O desafio consistia em aprimorar o código já existente e disponível no github: https://github.com/cami-la/desafio-poo-dio/tree/master

## Funcionalidades
Foram implementados os seguintes métodos:

**exibirConteudo() - Class Conteudo**
- Visando tornar a classe mais genérica e facilitar a implementação do toString() nas classes filhas **Mentoria** e **Curso**, foi criado este método protected:
- Código antigo: Inexistente
- Código novo:
`  protected String exibirConteudo() {
  return "Título: '" + titulo + '\'' + ", Descrição: '" + descricao; }`

**Melhorias no toString() - Class Mentoria**
- Melhoria na impressão do método:
  `return "{Mentoria - " + exibirConteudo() +", Data: " + data +'}';`

**Melhorias no toString() - Class Curso**
- Melhoria na impressão do método:
- Código antigo:
`  public String toString() {
  return "Curso{" + "titulo='" + getTitulo() + '\'' + ", descricao='" + getDescricao() + '\'' + ", cargaHoraria=" + cargaHoraria + '}'; }`
- Código novo:
`  public String toString() {
  return "{Curso - " + exibirConteudo() + ", Carga Horária: " + cargaHoraria + "h}"; }`

**exibirDevsInscritos() - Class Bootcamp**
- Este método foi criado para exibir a lista de devs inscritos, fazendo uso do Stream Api.
`  public void exibirDevsInscritos() {
  devsInscritos.forEach(dev -> System.out.println(dev.getNome()));}`
