<!-- PROJECT LOGO -->
<div align="center">
   <a href="https://github.com/othneildrew/Best-README-Template">
      <img src="https://logodownload.org/wp-content/uploads/2014/12/estacio-logo-1-2048x1641.png" alt="estacio logo" width="80"                  height="80">
   </a>
    <h1 align="center"> Universidade Estácio de Sá </h1>
     <hr>
</div> 

* DESENVOLVIMENTO FULL STACK- TURMA 9003
* Disciplina: RPG0014  - Iniciando o caminho pelo Java
* Semestre Letivo: 2023.2
<hr>

* [EMERSON GREGORIO ALVES](https://github.com/Gregdev22) - MATRICULA: 2022.0908.4986
<hr>
 <h1 align="center"> Missão Prática | Nível 1 | Mundo 3 </h1>
 <h2 align="left" > Implementação de um cadastro de clientes em modo texto, com persistência
em arquivos, baseado na tecnologia Java. </h2> 
 <h3>Procedimento 1: Criação das Entidades e Sistema de Persistência </h3>
 <h3>Procedimento 2: Criação do Cadastro em Modo Texto </h3>
 <hr>


 <h2> :clipboard: Objetivos da Prática </h2>

* Utilizar herança e polimorfismo na definição de entidades.
* Utilizar persistência de objetos em arquivos binários.
* Implementar uma interface cadastral em modo texto.
* Utilizar o controle de exceções da plataforma Java.
* No final do projeto, o aluno terá implementado um sistema cadastral em Java, utilizando os recursos da
* programação orientada a objetos e a persistência em arquivos binários.


<h2> Códigos </h2>
 [Procedimento 1](https://github.com/Gregdev22/Missao-1-Mundo-3/tree/main/CadastroPOO)
 <br>
 Procedimento 2: (Link para a pasta com os codigos do procedimento)
<hr>
<br>
Entidades:
<br>

* Classe Pessoa
  
```java

package model;

/**
 *
 * @author grego
 */

import java.io.Serializable;

public class Pessoa implements Serializable{
    private int id;
    private String nome;
    
    // construtor
    public Pessoa(int id, String nome) {
        this.id = id;
        this.nome = nome;
    }
    
    public int getId() {
        return id;
    }
    
    public void setId(int id){
        this.id = id;
    }
    
    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }
    
    //Método exibir
    public void exibir(){
        System.out.print("id: "+this.id + "\n" + "Nome: " + this.nome + "\n");
    }
}
```

* Classe PessoaFisica


```java
  package model;

/**
 *
 * @author grego
 */

import java.io.Serializable;

public class PessoaFisica extends Pessoa implements Serializable {
    
    private String cpf;
    private int idade;
    
    //Constutor
    public PessoaFisica(int id, String nome, String cpf, int idade){
        super(id, nome);
        this.cpf = cpf;
        this.idade = idade;
    }
    
    public String getCpf() {
        return cpf;
    }

    public void setCpf(String cpf) {
        this.cpf = cpf;
    }
    
    public int getIdade(){
        return idade;
    }
    
    public void setIdade(int idade){
        this.idade = idade;
    }
    
    //Método exibir
    public void exibir(){
        System.out.print("\n"+"id: "+getId()+"\nNome: "+getNome()+ "\nCPF: "+this.cpf + "\n" + "Idade: " + this.idade + "\n");
    }
}
```
* Classe PessoaJuridica
  
```java
package model;

/**
 *
 * @author grego
 */

import java.io.Serializable;

public class PessoaJuridica extends Pessoa implements Serializable{
    
    private String cnpj;
    
     //Constutor
    public PessoaJuridica(int id, String nome, String cnpj){
        super(id, nome);
        this.cnpj = cnpj;
    }
    
    public String getCnpj() {
        return cnpj;
    }

    public void setCnpj(String cnpj) {
        this.cnpj = cnpj;
    }
    
    public void exibir(){
        System.out.print("\n" + "id: "+getId()+ "\nNome: "+getNome()+"\nCNPJ: "+this.cnpj+"\n");
    }
}
```
