

# poolvroJAVA


package com.mycompany.projetolivro;


public class  Livro implements Publicacao{
    private String titulo;
    private String Autor;
    private int totPaginas;
    private int pagAtual;
    private boolean aberto;
    private String leitor;

    public Livro(String titulo, String Autor, int totPaginas, String leitor) {
        this.titulo = titulo;
        this.Autor = Autor;
        this.totPaginas = totPaginas;
        this.aberto = false;
        this.pagAtual = 0;
        this.leitor = leitor;
    }

    public String getTitulo() {
        return titulo;
    }

    public void setTitulo(String titulo) {
        this.titulo = titulo;
    }

    public String getAutor() {
        return Autor;
    }

    public void setAutor(String Autor) {
        this.Autor = Autor;
    }

    public int getTotPaginas() {
        return totPaginas;
    }

    public void setTotPaginas(int totPaginas) {
        this.totPaginas = totPaginas;
    }

    public int getPagAtual() {
        return pagAtual;
    }

    public void setPagAtual(int pagAtual) {
        this.pagAtual = pagAtual;
    }

    public boolean isAberto() {
        return aberto;
    }

    public void setAberto(boolean aberto) {
        this.aberto = aberto;
    }

    public String getLeitor() {
        return leitor;
    }

    public void setLeitor(String leitor) {
        this.leitor = leitor;
    }

    
    public String detalhes() {
        return "Livro{" + "titulo=" + titulo + "\n, Autor=" + Autor + "\n, totPaginas=" 
                + totPaginas + "\n, pagAtual=" + pagAtual 
                + "\n, aberto=" + aberto + "\n, leitor=" + leitor +  '}';
    }

    @Override
    public void abrir() {
        this.aberto = true;
    }

    @Override
    public void fechar() {
        this.aberto = false;
    }

    @Override
    public void folhear(int p) {
        if (p> this.totPaginas){
            this.pagAtual=  0;
        }else{
         
        this.pagAtual = p;
    }
    }

    @Override
    public void avancarPag() {
        this.pagAtual++; 
    }

    @Override
    public void voltarPag() {
    this.pagAtual--;
    }

    
    
   

  
    
    
    
}
