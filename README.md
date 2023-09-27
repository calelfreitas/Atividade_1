# Atividade_1
#include <iostream>
#include <stdio.h>
#include <conio.h>

using namespace std;

class Dados{
    protected:
    string nome;
    int id, rg;
    public:
  Dados( string _nome, int _id, int _rg){
    ~Dados( void );
    void MostrarDados( void );
};
Dados::Dados( string _nome,int _rg, int _id){
    nome=_nome;
    rg=_rg;
    id=_id;
}
Dados::~Dados( void ){
    cout<<"Dados inexistentes!"
}
Dados::MostrarDados(void){
    cout<<"Dados da pessoa:"<<endl;
    cout<<"Nome: "<<nome<<endl;
    cout<<"Idade: "<<idade<endl;
}
class Pessoa:public Dados{
    private:
    double renda;
    public:
    Pessoa( string _nome, int _id, int _rg);
    void MostrarPessoa();
};
Pessoa::Pessoa( string _nome, int _id, int _rg, double _renda): Dados( string _nome, int _id, int _rg){
    renda=_renda;
}
Pessoa::MostrarPessoa(){
    cout<<"Nome: "<<nome<<endl;
    cout<<"Idade: "<<id<<endl;
    cout<<"Rg: "<<rg<<endl;
    cout<<"Renda: "<<renda<<endl;
}
int main() {
    MostrarPessoa();
    getch();

    return 0;
}
