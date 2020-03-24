
#include <iostream>
#include <fstream>
#include <cstdlib>
#include <iomanip>
#include <string>
using namespace std;

// Declaração da struct de cadastro chamada lista 
	struct LISTA
	{
		int num;
		string nome;
		long int cpf;
		string size;
		int categoria;
		bool pago;
		LISTA *prox;
		
	};
	
// Declaração de variaveis do tipo static
 	
static LISTA cadastro[1]; // vetor de cadastro do tipo LISTA
static string nome;
static double cpf;
static int categoria;
static string size;
static bool pago;

// Função que busca o registro no arquivo txt com paramentro por referência lec do tipo ifstream
	void buscarregistro(ifstream &lec)
{
	system("cls"); // cmd limpa a tela
	lec.open("kids.txt", ios::in);// cmd de abertura de arquivo do tipo saida.
	string nome,cpf,codigo,aux,size,pago;// cmd declaração de variaveis.
	bool encontrado = false; // cmd booleano que verifica se foi encontrado o registro
	cout << "Digite o Codigo \n";// cmd que pede pra digitar o codigo
	cin >> aux;// comando input de aux
		char verificador[30]; // vetor do tipo char
		
	
	lec>>nome;// cmd de leitura apontando pra variavel nome
	while(!lec.eof() && !encontrado){// estrutura while verificando se foi até o final de arquivo  && e se foi econtrado.
			lec>>cpf;// cmd de leitura apontando pra variavel cpf
			lec>>codigo;// cmd de leitura apontando pra variavel codigo
			lec>>size;// cmd de leitura apontando pra variavel size
			lec>>pago;// cmd de leitura apontando pra variavel pagamento
			
			if(codigo == aux )// cmd de leitura comparando se o codigo do arquivo txt é igual o valor da variavel aux digitada pelo usuário
			{
		
				cout << "Nome     : "<<nome << endl ;// cmd que mostra os valores da variavel nome dentro do arquivo txt
				cout << "cpf      : "<<cpf  << endl;// cmd que mostra os valores da variavel cpf dentro do arquivo txt
				cout << "Codigo   : "<<codigo<< endl;// cmd que mostra os valores da variavel codigo dentro do arquivo txt
				cout << "Tamanho da Camiseta : " << size << endl;// cmd que mostra os valores da variavel size dentro do arquivo txt
				if(pago == "1")// cmd que verifica se pagamento foi efetuado
				{
					cout << "Pagamento: Efetuado \n";// cmd que mostra pagamento efetuado
				}else{
					cout << "Pagamento: Não há Pagamento Liberado \n";// cmd que mostra não há pagamento efetuado
				}
				cout << "========================== \n";// cmd separador de registro
				encontrado = true; // cmd que mostra se foi encontrado e muda o valor para true
				}
			lec>>nome;
			
	}
	
	lec.close();	
	if(!encontrado){
		cout << "Registro Não econtrado \n";
		system("pause");
	}

}
	
	incrementadorderegistro(ifstream &lec){
		
	system("cls"); // cmd limpa a tela
	lec.open("kids.txt", ios::in);// cmd de abertura de arquivo do tipo saida.
	string nome,cpf,codigo,aux,size,pago;// cmd declaração de variaveis.
		
	}

	verificapagamentos(ifstream &lec){
		
		system("cls");
		ifstream leitor("kids.txt",ios::in | ios::app);
char vetor[1000];
char temp;
int contp = 0, contm = 0, contg = 0, contgg = 0, contxg = 0, contxgg = 0;
string nome,cpf,codigo,camisa,pago;
string pagamento = "1";
int cont_recebe;
leitor>>nome;
while(!leitor.eof())
{
	
	leitor>>cpf;
	leitor>>codigo;
	leitor>>camisa;
	leitor>>pago;
	

	if(pago == pagamento && camisa == "P")
	{
		contp++;
	
	}else if(pago == pagamento && camisa == "M"){
		contm++;
	}
	else if(pago == pagamento && camisa == "G"){
		contg++;
	}
	else if(pago == pagamento && camisa == "GG"){
		contgg++;
	}
	else if(pago == pagamento && camisa == "XG"){
		contxg++;
	}
		else if(pago == pagamento && camisa == "XGG"){
		contxgg++;
	}else if(pago == "0")
	{
	 cont_recebe++;
	}
	leitor>>nome;

}
leitor.close();


cout << "Camisetas P:   [ " << contp << " ]" << endl;
cout << "Camisetas M:   [ " << contm << " ]" << endl;
cout << "Camisetas G:   [ " << contg << " ]" << endl;
cout << "Camisetas GG:  [ " << contgg << " ]" << endl;
cout << "Camisetas XG:  [ " << contxg<< " ]" << endl;
cout << "Camisetas XGG: [ " << contxgg << " ]" << endl;
cout <<"FALTA :        [ " << cont_recebe << " ]" << " ATLETAS PARA EFETUAREM O PAGAMENTO" << endl;
	
			


		
		
	}



	void buscarregistro2(ifstream &lec)
{
	system("cls");
	lec.open("caminhada.txt", ios::in);
	string nome,cpf,codigo,aux,size,pago;
	bool encontrado = false;
	cout << "Digite o Codigo \n";
	cin >> aux;
	
	
	lec>>nome;
	while(!lec.eof() && !encontrado){
			lec>>cpf;
			lec>>codigo;
			lec>>size;
			lec>>pago;
			
			if(codigo == aux )
			{
		
				cout << "Nome     : "<<nome << endl ;
				cout << "cpf      : "<<cpf  << endl;
				cout << "Codigo   : "<<codigo<< endl;
				cout << "Tamanho da Camiseta : " << size << endl;
				if(pago == "1")
				{
					cout << "Pagamento: Efetuado \n";
				}else{
					cout << "Pagamento: Não há Pagamento Liberado \n";
				}
				cout << "========================== \n";
				encontrado = true;
				}
			lec>>nome;
			
	}
	
	lec.close();	
	if(!encontrado){
		cout << "Registro Não econtrado \n";
		system("pause");
	}
		system("pause");
}

void buscarregistro3(ifstream &lec)
{
	system("cls");
	lec.open("corrida5k.txt", ios::in);
	string nome,cpf,codigo,aux,size,pago;
	bool encontrado = false;
	cout << "Digite o Codigo \n";
	cin >> aux;
	
	
	lec>>nome;
	while(!lec.eof() && !encontrado){
			lec>>cpf;
			lec>>codigo;
			lec>>size;
			lec>>pago;
			
			if(codigo == aux )
			{
		
				cout << "Nome     : "<<nome << endl ;
				cout << "cpf      : "<<cpf  << endl;
				cout << "Codigo   : "<<codigo<< endl;
				cout << "Tamanho da Camiseta : " << size << endl;
				if(pago == "1")
				{
					cout << "Pagamento: Efetuado \n";
				}else{
					cout << "Pagamento: Não há Pagamento Liberado \n";
				}
				cout << "========================== \n";
				encontrado = true;
				}
			lec>>nome;
			
	}
	
	lec.close();	
	if(!encontrado){
		cout << "Registro Não econtrado \n";
		system("pause");
	}
		system("pause");
}

void buscarregistro4(ifstream &lec)
{
	system("cls");
	lec.open("corrida10k.txt", ios::in);
	string nome,cpf,codigo,aux,size,pago;
	bool encontrado = false;
	cout << "Digite o Codigo \n";
	cin >> aux;
	
	
	lec>>nome;
	while(!lec.eof() && !encontrado){
			lec>>cpf;
			lec>>codigo;
			lec>>size;
			lec>>pago;
			
			if(codigo == aux )
			{
		
				cout << "Nome     : "<<nome << endl ;
				cout << "cpf      : "<<cpf  << endl;
				cout << "Codigo   : "<<codigo<< endl;
				cout << "Tamanho da Camiseta : " << size << endl;
				if(pago == "1")
				{
					cout << "Pagamento: Efetuado \n";
				}else{
					cout << "Pagamento: Não há Pagamento Liberado \n";
				}
				cout << "========================== \n";
				encontrado = true;
				}
			lec>>nome;
			
	}
	
	lec.close();	
	if(!encontrado){
		cout << "Registro Não econtrado \n";
		system("pause");
	}
		system("pause");
}

void buscarregistro5(ifstream &lec)
{
	system("cls");
	lec.open("corrida15k.txt", ios::in);
	string nome,cpf,codigo,aux,size,pago;
	bool encontrado = false;
	cout << "Digite o Codigo \n";
	cin >> aux;
	
	
	lec>>nome;
	while(!lec.eof() && !encontrado){
			lec>>cpf;
			lec>>codigo;
			lec>>size;
			lec>>pago;
			
			if(codigo == aux )
			{
		
				cout << "Nome     : "<<nome << endl ;
				cout << "cpf      : "<<cpf  << endl;
				cout << "Codigo   : "<<codigo<< endl;
				cout << "Tamanho da Camiseta : " << size << endl;
				if(pago == "1")
				{
					cout << "Pagamento: Efetuado \n";
				}else{
					cout << "Pagamento: Não há Pagamento Liberado \n";
				}
				cout << "========================== \n";
				encontrado = true;
				}
			lec>>nome;
			
	}
	
	lec.close();	
	if(!encontrado){
		cout << "Registro Não econtrado \n";
		system("pause");
	}
		system("pause");
}


void editaregistro(ifstream &lec){
	system("cls");
	string nome;
	string cpf;
	string codigo;
	string camisa;
	string pago;	
	string codaux;
	string nomeaux;
	
	cout << "Informe a tabela \n";
	
		
	lec.open("kids.txt", ios::in);
	ofstream aux("auxiliar.txt", ios::out);
	if(lec.is_open()){
		cout <<"Digite o Código do Atleta " << endl;
		cin >> codaux;
		lec>>nome;
		while(!lec.eof())
		{
			lec>>cpf;
			lec>>codigo;
			lec>>camisa;
			lec>>pago;
			if(codigo == codaux)
			{
				cout << "Digite Um Novo Nome: \n";
				cin >> nomeaux;
				aux << nomeaux <<" "<< cpf <<" "<< codigo <<" " << camisa<<" "<<pago<<"\n";
			}else{
				aux << nome <<" "<< cpf <<" "<< codigo <<" " << camisa<<" "<<pago<<"\n";
		
			}
			lec>>nome;
		}
		lec.close();
		aux.close();
	}else
		cout << "ERROR \n";
		remove("kids.txt");
		rename("auxiliar.txt", "kids.txt");
	}	

void busca_atleta(LISTA *buscar);
int main(int argc, char** argv) {
	setlocale(LC_ALL, "portuguese");
		int op, numero, achou, resp;
	ofstream esc;
	ifstream lec;

	LISTA *inicio = NULL;
	LISTA *fim = NULL;	
	LISTA *aux;
	LISTA *contador;
	LISTA *anterior;
	
	
	do{
		system("cls");
		
		
		cout << "\n\n\n\============== CORRE FOREST CORRE! ============= \n\n\n";
		cout <<"01 - Cadastro do Atleta \n\n";
		cout <<"02 - Consulta de Atleta \n\n";
		cout <<"03 - Editar Cadastro de Atleta \n\n";
		cout <<"04 - Atleta Que Pagaram as Taxas de Cada Categoria \n\n";
		
		
		
		cout <<"informe a operacão! \n\n";
		cin >> op;
	
		if(op < 1 || op > 6)
		{
			cout <<" operacao Invalida! \n";
	}else{
		
			if(op == 1)
			{
				
				cout << "digite o numero da inscrição\n";
				LISTA *novo = new LISTA();
				cin >> novo->num;
				cout <<"nome do atleta \n";
				cin >> novo->nome;
				cout <<"Numero do CPF: \n";
				cin >> novo->cpf;
				cout <<"Tamanho da Camiseta EX(P,M,G,GG,XG,XGG) letra Maiúscula : \n";
				cin >> novo->size;
				cout <<"Efetuar Pagamento ? (1/SIM / 0 NÂO)\n";
				cin >> novo->pago;
				
				system("pause");
				system("cls");
				
				cout <<" ========== Escolha A Categoria que mais se Adeque a você! ==========\n\n\n";
				cout <<"01 - KIDS - Corrida até 100 Metros! \n";
				cout <<"02 - CAMINHADA 5K - CAMINHADA até 5KM \n";
				cout <<"03 - CORRIDA 5K - Corrida até 5KM \n";
				cout <<"04 - CORRIDA 10K - Corrida até 10KM - PESSOAS COM PULMÃO TREINADO \n";
				cout <<"05 - CORRIDA 21K - Corrida até 21KM PULMÃO QUE O PROF ORLANDO NUNCA VAI TER \n";
				cin >> novo->categoria;	
				
				
				for(int c=0;c<1;c++)
				{
					cadastro[c].num = novo->num;
					cadastro[c].nome = novo->nome;
					cadastro[c].cpf = novo->cpf;
					cadastro[c].size = novo->size;
					cadastro[c].pago = novo->pago;
					cadastro[c].categoria = novo->categoria;
				
			
					
					
				}
				
					for(int c=0;c<1;c++)
				{
					
						if(cadastro[c].categoria == 1){
					
					ofstream arquivos;
				
					arquivos.open("kids.txt",ios::app);
					
					
					arquivos 
					<<cadastro[c].nome<<" "
					<<cadastro[c].cpf <<" "
					<<cadastro[c].num <<" "
					<<cadastro[c].size<<" "
					<<cadastro[c].pago<<'\n';
				
					}	
				}
				
					for(int c=0;c<1;c++)
				{
					
						if(cadastro[c].categoria == 3){
					
					ofstream arquivos;
				
					arquivos.open("corrida5k.txt",ios::app);
					
					
					arquivos 
					<<cadastro[c].nome<<" "
					<<cadastro[c].cpf <<" "
					<<cadastro[c].num <<" "
					<<cadastro[c].size<<" "
					<<cadastro[c].pago<<'\n';
				
					}	
				}
					
				
				for(int c=0;c<1;c++)
				{
					
						if(cadastro[c].categoria == 4){
					
					ofstream arquivos;
				
					arquivos.open("corrida10k.txt",ios::app);
					
					
					arquivos 
					<<cadastro[c].nome<<" "
					<<cadastro[c].cpf <<" "
					<<cadastro[c].num <<" "
					<<cadastro[c].size<<" "
					<<cadastro[c].pago<<'\n';
				
					}	
				}
				
				for(int c=0;c<1;c++)
				{
					
						if(cadastro[c].categoria == 5){
					
					ofstream arquivos;
				
					arquivos.open("corrida15k.txt",ios::app);
					
					
					arquivos 
					<<cadastro[c].nome<<" "
					<<cadastro[c].cpf <<" "
					<<cadastro[c].num <<" "
					<<cadastro[c].size<<" "
					<<cadastro[c].pago<<'\n';
				
					}	
				}
			
				system("pause");
							
				if(inicio == NULL){
					inicio = novo;
					fim = novo;
					fim->prox = NULL;
				}else{
					novo->prox = inicio;
					inicio = novo;
					
				}
				cout << "Cadastro Inserido com Sucesso!";
			}
			
			if(op == 2){
				

					system("cls");
					cout <<"\n\n\n Consultando os Cadastros! \n\n\n\n";
					int op;
					cout <<"Consultar Cadastro de Qual Tabela? \n";
					cout <<"01 -> KIDS \n";
					cout <<"02 -> Caminhada5k \n";
					cout <<"03 -> Corrida 5k \n";
					cout <<"03 -> Corrida 10k \n";
					cout <<"03 -> Corrida 21k \n";
					cin >> op;
					
			if(op == 1)
			{
			buscarregistro(lec);
			}
			
		
		 if(op == 2)
			{				
			buscarregistro2(lec);												
			}
			
		if(op == 3)
			{				
			buscarregistro3(lec);				
			}
		
	 	if(op == 4)
			{			
			 buscarregistro4(lec);				 
		    }
		if(op == 5)
			 {
			buscarregistro5(lec);	
		     }
			
			}
			
		}
					if(op == 3){
						
				editaregistro(lec);	
			
			
			}
					  
				if(op == 4)
				{
				
					verificapagamentos(lec);
				}
				
				cout << "\n Deseja Fazer Outra Operação? \n";
				cin >> resp;
				
	}while(resp == 1);

	return 0;
}
