# Respostas
1 - Nível 2 

2 - Os verbos HTTP são mais orientadas a documentos do que orientados a bancos de dados - enquanto você pode atualizar, excluir e criar novos recursos, isso nô é exatamente CRUD no sentido banco de dados da palavra, pelo menos quando se trata de utilizar verbos HTTP.

3 - Dá uma ideia de como este componente funciona em uma aplicaçâo RESTful. Ao ser implementado, a API passa a fornecer links que indicarão aos clientes como navegar através dos seus recursos.
Com isso, o cliente não precisa ter um conhecimento profundo da API, basta conhecer a URL de inicial e partir dos links fornecidos poderá acessar todos os recursos de forma circular, se guiando através das requisições realizadas.

4- Se uma requisiçâo identica  pode ser feita uma ou mais vezes em sequência com o mesmo efeito enquanto deixa o servidor no mesmo estado. Não deveria possuir nenhum efeito colateral. Tem a propriedade de ser aplicado mais do que uma vez sem que o resultado se altere.

5- São usados para indicar uma requisiçâode alteração de dados. Geralmente, ao usar-se o PUT. fica legível que a alteração do dado será com referência a entidade completa. O PATCH é usado para atualziação parcial, quando você não quer mandar o payload completo.

6- for (let i=0; i < obj.length; i++){
    let filme = obj[i]
    console.log(filme.Title)
    console.log(filme.Year)

    let genero = filme.Genre.split(",")
    for(let i=0; i < genero.length; i++){
        console.log(genero[i])
    }
}

7 - for (let rgb = 0; rgb < obj.length; rgb++){
    let cores = obj[rgb]
    for (item in cores){
        console.log(`${item} RGB: ${cores[item]}`)
    }
}

8- function buscar(cidade){
      const listarEstado = estados.filter(({sigla}) => sigla == cidade)
      for (let i of listarEstado){
        let municipio = i.cidades

        for (let j of municipio){
          console.log(j)
        }
      }

  }

buscar("CA")