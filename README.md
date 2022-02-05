void bul_bUnlu_uyumu(char x[]);
void bul_kUnlu_uyumu(char x[]);
 int main(){
      char metin[100];
     printf("Metin giriniz:");
     gets(metin);
     bul_bUnlu_uyumu(metin);
     bul_kUnlu_uyumu(metin);
     return 0;}
void bul_bUnlu_uyumu(char x[]){
 int i=0,kalin_unlu=0,ince_unlu=0;
 while(x[i] != '\0')
 {
 if(x[i]=='a'|| x[i]=='o'|| x[i]=='u'|| x[i]=='ı'){
 kalin_unlu++;}
 if(x[i]=='e'|| x[i]=='i'|| x[i]=='ö'|| x[i]=='ü'){
 ince_unlu++;}
 i++;}
 if(kalin_unlu==0 || ince_unlu==0){
    printf("%s metni buyuk unlu uyumuna uyar\n",x);}
 else {printf("%s metni buyuk unlu uyumuna uymaz\n",x);}
 }
void bul_kUnlu_uyumu(char x[]){
int k=0,deneme1=0,deneme2=0,unlu_harf=0,top;
 while(x[k] != '\0')
 {
 if(x[k]=='o'|| x[k]=='u'|| x[k]=='ö'|| x[k]=='ü'|| x[k]=='a'|| x[k]=='e'|| x[k]=='ı'|| x[k]=='i'){
 unlu_harf++;}
 if(x[k]=='a'|| x[k]=='e'|| x[k]=='ı'|| x[k]=='i'){
 deneme1++;}
 if(x[k]=='o'|| x[k]=='u'|| x[k]=='ö'|| x[k]=='ü' && x[k+2]=='a'|| x[k+2]=='e'|| x[k+2]=='u'|| x[k+2]=='ü'){
 deneme2=2;}
 k++;}
 top=deneme1+deneme2;
if(deneme1==unlu_harf || top==unlu_harf || deneme2==unlu_harf){
 printf("%s metni kucuk unlu uyumuna uyar",x);}
 else {printf("%s metni kucuk unlu uyumuna uymaz",x);}
}
