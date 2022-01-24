# BancoFC
Utilização básica dos métodos: Herança, JOptionPaine, UIManager(Obtido pela comunidade).

/*
São 3 classes, sendo a principal BancoFC, e demais: Pessoa, Cliente;

 Notas TiagoFloresCorrea:
Modelo simples apenas para botar em prática conceitos.
"Eu poderia ter feito algo mais complexo que demandasse tempo, entretanto, iniciei alguns projetos que nunca foram terminados, neste mais simples fiz em um dia."

Utilizando métodos: Herança, JOptionPaine, UIManager(Obtido pela comunidade).

PS: O mais engraçado é que os erros apresentados no desenvolvimento deste codigo, foram detalhes na sintaxe.
 */
 
// CLASSE BancoFC===============================================================================================================================================================
 
package bancofc;


import java.awt.Dimension;
import javax.swing.JOptionPane;
import javax.swing.UIManager;

public class BancoFC {

  
    
    public static void main(String[] args) {
        
        Cliente cliente1 = new Cliente("Jose", "Porto Alegre",2, 2021);
        Cliente cliente2 = new Cliente("Maria", "Rio Grande",1, 2019);
        
        UIManager.put("OptionPane.minimumSize", new Dimension(300, 100));
        
        JOptionPane.showMessageDialog (null,"Relatório de contas ativas** " , "BancoFC (Seu investimento, nosso interesse)", JOptionPane.PLAIN_MESSAGE );
        
 
        JOptionPane.showMessageDialog (null,"Em nosso sistema temos estes Clientes atualmente: \n Nome: "+cliente1.getNome()+",  Cidade: "+cliente1.getCidade()+",  Numero da Conta: "+cliente1.getCodigo()+",  Data de Abertura de conta: "+cliente1.getIngresso()+
                ". \n Nome: "+cliente2.getNome()+",  Cidade: "+cliente2.getCidade()+",  Numero da Conta: "+cliente2.getCodigo()+",  Data de Abertura de conta: "+cliente2.getIngresso()+" \n Encerramento de dados! \n Clique OK para sair.", "BancoFC (Seu investimento, nosso interesse)" , JOptionPane.PLAIN_MESSAGE );
        

    }
    
}


// CLASSE Pessoa===============================================================================================================================================================
package bancofc;

/**
 *
 * @author TFCorrea
 */
public class Pessoa {
   
   private String nome;
   private String cidade;
   
   public Pessoa (String nome, String cidade){
       this.nome=nome;
       this.cidade=cidade;
 
   }
   
   public String getNome (){
   return nome;
   }
   
   public void setNome (String nome){
       this.nome=nome;
   }
   
   public String getCidade (){
       return cidade;
   }
   
   public void setCidade (String cidade){
       this.cidade=cidade;
   }
   
}


// CLASSE Cliente===============================================================================================================================================================

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package bancofc;

/**
 *
 * @author TFCorrea
 */
public class Cliente extends Pessoa{
 
    private int codigo;
    private int ingresso;
    
    public Cliente(String nome, String cidade,int codigo, int ingresso){
    
    super(nome, cidade);
    this.codigo=codigo;
    this.ingresso=ingresso;
    }
    
    public int getCodigo (){
        return codigo;
    }
    
    public void setCodigo (int codigo){
        this.codigo=codigo;
    }
    
    public int getIngresso (){
        return ingresso;
    }
    
    public void setIngresso (int ingresso){
        this.ingresso=ingresso;
    }
    
}


