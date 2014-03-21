# include<stdio.h> 
# include<stdlib.h>
# include<conio.h>
# include<time.h>
void JetonSayici(int jetonSayisi);
void main()
{
	int js;
	printf("Baslamak icin lutfen jeton sayisini giriniz... ");
	scanf_s("%d", &js);

	JetonSayici(js);

	getwchar();
	getwchar();

}
void JetonSayici(int JetonSayisi)
{
	srand(time(NULL));
	int hazne[10] = { 0, 0, 0, 0, 0, 0, 0, 0, 0, 0 };
	int jeton[BUFSIZ] = { 0 };
	int j, sayi = 0, ihtimal = 0, hazne1 = 0, hist;
	int max = 0;
	int kontrol = 0;
	for (j = 0; j<JetonSayisi; j++)
	{
		printf("\n%2d.jetonu atmak icin herhangi bir tusa basiniz:\n", j + 1);
		getwchar();
		for (int h = 0; h<10; h++)
		{
			sayi = rand() % 2;
			if (sayi == 1)
				ihtimal++;
		}
		if (ihtimal == 9)
			hazne[9]++;
		else if (ihtimal == 8)
			hazne[8]++;
		else if (ihtimal == 7)
			hazne[7]++;
		else if (ihtimal == 6)
			hazne[6]++;
		else if (ihtimal == 5)
			hazne[5]++;
		else if (ihtimal == 4)
			hazne[4]++;
		else if (ihtimal == 3)
			hazne[3]++;
		else if (ihtimal == 2)
			hazne[2]++;
		else if (ihtimal == 1)
			hazne[1]++;
		else if (ihtimal == 0)
			hazne[0]++;
		hazne1 = ihtimal;
		printf("\t<<..::jeton %d.hazneye dustu::..>>", hazne1);
		printf("\n");
		ihtimal = 0;
	}
	system("CLS");
	printf("\t--------------------------------------\n");
	printf("\t| Haznelerdeki Toplam Jeton sayilari |\n");
	printf("\t--------------------------------------\n");
	printf("\t---------------------------------------\n");
	for (int h = 0; h<10; h++)
	{
		printf("\t|%6d.haznedeki jeton sayisi: %3d   |", h, hazne[h]);
		printf("\n");
	}
	printf("\t---------------------------------------\n\n");
	for (int k = 0; k<10; k++)
	{
		if (hazne[k]>max)
			max = hazne[k];
	}
	printf("\t\t-------------\n");
	printf("\t\t| HISTOGRAM |\n");
	printf("\t\t-------------\n");
	printf("+----+---+---+---+---+---+---+---+---+---+---+\n");
	for (hist = max; hist > 0; hist--)
	{
		printf("<%3d >", hist);
		for (int l = 0; l<10; l++)
		{
			if (hist > hazne[l])
				printf("   |");
			else
				printf(" & |");
		}
		printf("\n");
	}
	printf("+----+---+---+---+---+---+---+---+---+---+---+\n");
	printf("| ** | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10|\n");
	printf("+----+---+---+---+---+---+---+---+---+---+---+\n");
}
