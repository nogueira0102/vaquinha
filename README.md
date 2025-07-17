# vaquinha
em prol de arrecadações
#include <iostream>
#include <string>
using namespace std;

int main() {
    string nome = "Dona Alcione e Seu Antônio";
    string chave_pix = "98970271056";
    double meta = 1000.00; // Meta da vaquinha
    double arrecadado = 0.0;
    double doacao;
    char continuar;

    cout << "====== VAQUINHA SOLIDÁRIA ======" << endl;
    cout << "Ajude " << nome << " com alimentos ou qualquer valor via PIX!" << endl;
    cout << "Chave PIX: " << chave_pix << " (Luis Fernando)" << endl;
    cout << "Meta: R$ " << meta << endl << endl;

    cout << "Sobre eles:" << endl;
    cout << "Dona Alcione tem problemas nos rins e depende de remédios." << endl;
    cout << "Seu Antônio também precisa de medicamentos e vive de reciclagem." << endl;
    cout << "Toda ajuda é bem-vinda!" << endl << endl;

    do {
        cout << "Digite o valor da sua doação (R$): ";
        cin >> doacao;

        if (doacao > 0) {
            arrecadado += doacao;
            cout << "Obrigado pela sua contribuição!" << endl;
            cout << "Total arrecadado até agora: R$ " << arrecadado << endl;
        } else {
            cout << "Valor inválido. Tente novamente." << endl;
        }

        if (arrecadado >= meta) {
            cout << "\n🎉 Parabéns! A meta foi atingida!" << endl;
            break;
        }

        cout << "Deseja continuar doando? (s/n): ";
        cin >> continuar;

    } while (continuar == 's' || continuar == 'S');

    cout << "\nEncerrando vaquinha. Total final arrecadado: R$ " << arrecadado << endl;
    cout << "Compartilhe essa causa e continue ajudando! 💚" << endl;

    return 0;
}
