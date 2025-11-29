# EAD-tp
#1
#include <stdio.h>

int main() {
    int a = 10, *pa = &a;
    float b = 2.5, *pb = &b;
    char c = 'x', *pc = &c;

    printf("%d %.2f %c\n", a, b, c);

    *pa = 20;
    *pb = 5.5;
    *pc = 'z';

    printf("%d %.2f %c\n", a, b, c);
    return 0;
}

#include <stdio.h>

int main() {
    int a, b;
    if (&a > &b) printf("%p\n", (void*)&a);
    else printf("%p\n", (void*)&b);
    return 0;
}

#include <stdio.h>

int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    if (&a > &b) printf("%d\n", a);
    else printf("%d\n", b);
    return 0;
}
#include <stdio.h>

void troca(int *a, int *b) {
    int t = *a; *a = *b; *b = t;
}

int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    troca(&a, &b);
    printf("%d %d\n", a, b);
    return 0;
}
#include <stdio.h>

void maiorMenor(int *a, int *b) {
    if (*a < *b) {
        int t = *a; *a = *b; *b = t;
    }
}

int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    maiorMenor(&a, &b);
    printf("%d %d\n", a, b);
    return 0;
}

#include <stdio.h>

int somaDobro(int *a, int *b) {
    *a *= 2;
    *b *= 2;
    return *a + *b;
}

int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    printf("%d\n", somaDobro(&a, &b));
    return 0;
}
#include <stdio.h>

void soma(int *a, int b) {
    *a = *a + b;
}

int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    soma(&a, b);
    printf("%d %d\n", a, b);
    return 0;
}
#include <stdio.h>

int main() {
    float v[10];
    for (int i = 0; i < 10; i++)
        printf("%p\n", (void*)&v[i]);
    return 0;
}
#include <stdio.h>

int main() {
    float m[3][3];
    for (int i = 0; i < 3; i++)
        for (int j = 0; j < 3; j++)
            printf("%p\n", (void*)&m[i][j]);
    return 0;
}
#2
int dobro(int x){ return x*2; }

#include <stdio.h>

void dataExtenso(int d, int m, int a) {
    char *mes[]={"janeiro","fevereiro","marco","abril","maio","junho","julho","agosto","setembro","outubro","novembro","dezembro"};
    printf("%d de %s de %d\n", d, mes[m-1], a);
}

int main(){
    int d,m,a;
    scanf("%d%d%d",&d,&m,&a);
    dataExtenso(d,m,a);
    return 0;
}
int sinal(int x){
    if (x > 0) return 1;
    if (x < 0) return -1;
    return 0;
}
#include <math.h>

int quadradoPerfeito(int n){
    int r = sqrt(n);
    return r*r == n;
}
float volumeEsfera(float r){
    return (4.0/3.0) * 3.141592 * r*r*r;
}
int emSegundos(int h,int m,int s){
    return h*3600 + m*60 + s;
}
float ctof(float c){
    return c*9.0/5.0 + 32;
}
#include <math.h>

float hip(float a,float b){
    return sqrt(a*a + b*b);
}
float vol(float r,float h){
    return 3.141592 * r*r * h;
}
int maior(int a,int b){
    return a>b?a:b;
}
float media(float a,float b,float c,char t){
    if(t=='A') return (a+b+c)/3;
    return (a*5 + b*3 + c*2)/10;
}
#include <stdio.h>

int somaDigitos(int n){
    int s=0;
    while(n>0){ s+=n%10; n/=10; }
    return s;
}

int main(){
    int n;
    scanf("%d",&n);
    if(n<=0){ printf("Numero invalido\n"); return 0; }
    printf("%d\n", somaDigitos(n));
    return 0;
}
float calc(float a,float b,char op){
    if(op=='+') return a+b;
    if(op=='-') return a-b;
    if(op=='*') return a*b;
    return a/b;
}
#include <stdio.h>

int main(){
    float km, l, c;
    scanf("%f%f",&km,&l);
    c = km/l;
    if(c<8) printf("Venda o carro!\n");
    else if(c<=14) printf("Economico!\n");
    else printf("Super economico!\n");
    return 0;
}
int forma(int a,int b,int c){
    return a<b+c && b<a+c && c<a+b;
}

int tipo(int a,int b,int c){
    if(a==b && b==c) return 1;
    if(a==b || b==c || a==c) return 2;
    return 3;
}

