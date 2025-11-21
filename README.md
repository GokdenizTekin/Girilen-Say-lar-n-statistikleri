#include <iostream>
#include <ctime>
using namespace std; 
//2a+1
int main() {
    setlocale(LC_ALL, "Turkish");
    int a, b, c, d, e, f, g, h, j, k;
    char l;
   
    do {
        d = 0;
        c = 0;
        e = 1;
        f = 2147483647;
        g = 0;
        h = 2;
        j = 2147483646;
        k = 0;
        do {
            cout << "bir sayı giriniz(bitirmek için 0)";
            cin >> a;
            if (a < 0) {
                cout << "pozitif sayı girmelisiniz" << endl;
                continue;
            }
            else if (a % 2 != 0 && a > 0) {
                g++;
                if (a > e) {
                    e = a;
                }
                if (a < f) {
                    f = a;
                }
                if(a>0)
                    c += a;
            }

            else if (a % 2 == 0 && a > 0) {
                k++;
                if (a > h) {
                    h = a;
                }
                if (a < j) {
                    j = a;
                }
                if(a>0)
                    d += a;
            }
        } while (a != 0);
        cout << endl;
        cout << "girilen tek sayıların istatistikleri" << endl;
        cout << "girilen tek sayıların en küçüğü:" << f << endl;
        cout << "girilen tek sayılardan en büyüğü:" << e << endl;
        cout << "girilen tek sayıların sayısı:" << g << endl;
        cout << "girilen tek sayıların toplamı:" << c << endl;
        cout << "girilen tek sayıların ortalaması:" << (float)c / g << endl;
        cout << endl;
        cout << "girilen çift sayıların istatistikleri" << endl;
        cout << "girilen çift sayıların en küçüğü:" << j << endl;
        cout << "girilen cift sayılardan en büyüğü:" << h << endl;
        cout << "girilen çift sayıların sayısı:" << k << endl;
        cout << "girilen çift sayıların toplamı:" << d << endl;
        cout << "girilen çift sayıların ortalaması:" << (float)d / k << endl;
        cout << "devam etmek ister misin E/e:" << endl;
        cin >> l;

    } 
    while(l=='e' || l=='E');
    return 0;
}      


