# 12.-odev

/*kullan�c� bir say� girisi yapacak daha sonra switch case yap�s� ile kullan�c�ya bu say� ile hangi i�lemi yapmak istiyorsunuz sorusu sorulsun.
1. soru tek mi �ift mi buldurma i�lemi
2. soru fakt�riyeli bulma i�lemi
3. soru pi say�s�yla �arp�m bulma i�lemi
NOT: islemler fonskiyonlarla ger�ekle�tirilecek ve 1. soru geri d�n�� yapmayan bir fonksiyon olacak*/

#include<stdio.h>
#include<stdlib.h>

void tc(int);
int fact(int);
float pi(int);
int main(void)
{
	int secim=0;
	int sayi;
	
	
	printf("1. teklik ciftlik bulma\n2. faktoriyel bulma\n3.pi sayisi ile carpimini bulma\n");
	scanf("%d" , &secim);
	
	printf("bir sayi girisi yapiniz");
	scanf("%d" , &sayi);
	
	switch(secim)
	{
		case 1: 
		tc(sayi);
		break;
		
		case 2:
		printf("%d" , fact(sayi));
		break;
		
		case 3:
		printf("%f" , pi(sayi));
		break;
		
		default:
			printf("gecersiz tuslama yapildi.");
		break;
		
	}
	
	return 0;	
}

void tc(int a1)
{
	if(a1%2==0)
	{
		printf("sayiniz cifttir.");
	}
	
	else if(a1%2==1)
	{
		printf("sayiniz tektir.");
	}
	
	
}

int fact(int a1)
{
	int fact,i;
	
	for(i=1;i<=a1;i++)
	{
		fact=fact*i;
	}
	
	return fact ;
}

float pi(int a1)
{
	return a1*3.14;	
}
