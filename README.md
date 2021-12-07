#include <stdlib.h>
#include <stdio.h>
#include <conio.h>
#include <time.h>
#include <unistd.h>
#include <windows.h>

void panggilMenu(void);
void Penghitungan();
void struk(void);
void SetColor(unsigned short);

struct menu
    {
        int menuminuman;
    };
    struct subtotal
    {
        int jmlbeli1,jmlbeli2,jmlbeli3,jmlbeli4,jmlbeli5,jmlbeli6,jmlbeli7,jmlbeli8,jmlbeli9,jmlbeli10,jmlbeli11,jmlbeli12,jmlbeli13,jmlbeli14;
        int totalharga, bayar, kembalian;
    };
    struct minum
    {
        int fanta, cocacola, sprite, greensands, bintangradler, pocarisweet, hydrococo, isoplus, mizone, goodmood, airputih, milo, tehkotak, nescafe;

    };
    struct minum minuman;
    struct menu menuminum;
    struct subtotal sub;
    
    char yakin;
    time_t ambil_waktu;
    
void garistepi(int x) {
	int i;
	for(i = 0; i < x; i++) {
		printf("=");
	}
	printf("\n");
}
   
void delay() {
	int delay;
	delay=1;
	while(delay<100000000) {
		delay++;
	}
}

void loadscr() {
	int i;
	char load[] = {'W','E','L','C','O','M','E'};
	for(i=0; i<=6; i++) {
		printf("%c\t", load[i]);
		delay();
	}
	sleep(2);
}

void gotoxy(int x, int y) {
    COORD coord;
    coord.X = x;
    coord.Y = y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), coord);
}

    int main()
{
    panggilMenu();
    return 0;
}

void panggilMenu (void){
	system("color F0");
	gotoxy(32,13);
    loadscr();
    system("cls");
    printf ("\n\t\t\t  Selamat datang di Mesin Minuman Kelompok 7.\n");
    printf ("\t\t\t     Silakan pilih menu yang Anda sukai:\n\n");
    garistepi(120);
    printf ("|No.| Minuman \t\t| Harga      |\t\t|No.| Minuman\t\t | Harga     |\n");
    printf("|-------------------------------------------------------------------------------------\n");
    printf("| 1 | FANTA \t\t|  Rp 10.000 |\t\t");
    printf("| 2 | COCA-COLA\t\t | Rp 10.000 | \n");
    printf("| 3 | SPRITE \t\t|  Rp 10.000 |\t\t");
    printf("| 4 | GREEN SANDS\t | Rp 10.000 |\n");
    printf("| 5 | BINTANG RADLER \t|  Rp 20.000 |\t\t");
    printf("| 6 | POCARI SWEET\t | Rp 10.000 |\n");
    printf("| 7 | HYDRO COCO \t|  Rp 10.000 |\t\t");
    printf("| 8 | ISO PLUS\t\t | Rp 10.000 |\n");
    printf("| 9 | MIZONE \t\t|  Rp 10.000 |\t\t");
    printf("| 10| GOOD MOOD\t\t | Rp 20.000 |\n");
    printf("| 11| AIR PUTIH \t|  Rp 5.000  |\t\t");
    printf("| 12| MILO\t\t | Rp 5.000  |\n");
    printf("| 13| TEH KOTAK \t|  Rp 5.000  |\t\t");
    printf("| 14| NESCAFE\t\t | Rp 5.000  |\n");
    garistepi(120);
    printf("\n99. Struk Pembayaran\n55. Reset pilihan\n00.  Keluar\n");
    garistepi(120);
    
    for (menuminum.menuminuman!=0;menuminum.menuminuman!=99;){
 
 printf("\nInput pilihan yang Anda inginkan:         "); scanf("%d",&menuminum.menuminuman); 
    switch(menuminum.menuminuman) {
    case 1:
            printf("\n [1] Pemesanan FANTA\n");
            printf("jumlah pesan =\t\t\t  ");scanf("%d",&minuman.fanta);
            garistepi(100);
            sub.jmlbeli1=minuman.fanta*10000;
            break;
    case 2:
            printf("\n [2]Pemesanan COCA-COLA\n");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.cocacola);
            garistepi(100);
            sub.jmlbeli2=minuman.cocacola*10000;
    break;
    case 3:
            printf("\n [3] Pemesanan SPRITE\n");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.sprite);
            garistepi(100);
            sub.jmlbeli3=minuman.sprite*10000;
    break;
    case 4:
            printf("\n [4] Pemesanan GREEN SANDS\n");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.greensands);
            garistepi(100);
            sub.jmlbeli4=minuman.greensands*10000;
    break;
    case 5:
            printf("\n [5] Pemesanan BINTANG RADLER\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.bintangradler);
            garistepi(100);
            sub.jmlbeli5=minuman.bintangradler*20000;
    break;
    case 6:
            printf("\n [6] Pemesanan POCARI SWEET\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.pocarisweet);
            garistepi(100);
            sub.jmlbeli6=minuman.pocarisweet*10000;
    break;
    case 7:
            printf("\n [6] Pemesanan HYDRO COCO\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.hydrococo);
            garistepi(100);
            sub.jmlbeli7=minuman.hydrococo*10000;
    break;
    case 8:
            printf("\n [6] Pemesanan ISO PLUS\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.isoplus);
            garistepi(100);
            sub.jmlbeli8=minuman.isoplus*10000;
    break;
    case 9:
            printf("\n [6] Pemesanan MIZONE\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.mizone);
            garistepi(100);
            sub.jmlbeli9=minuman.mizone*10000;
    break;
    case 10:
            printf("\n [6] Pemesanan GOOD MOOD\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.goodmood);
            garistepi(100);
            sub.jmlbeli10=minuman.goodmood*20000;
    break;
    case 11:
            printf("\n [6] Pemesanan AIR PUTIH\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.airputih);
            garistepi(100);
            sub.jmlbeli10=minuman.airputih*5000;
    break;
    case 12:
            printf("\n [6] Pemesanan MILO\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.milo);
            garistepi(100);
            sub.jmlbeli10=minuman.milo*5000;
    break;
    case 13:
            printf("\n [6] Pemesanan TEH KOTAK\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.tehkotak);
            garistepi(100);
            sub.jmlbeli10=minuman.tehkotak*5000;
    break;
    case 14:
            printf("\n [6] Pemesanan NESCAFE\n ");
            printf("jumlah pesan = \t\t\t  ");scanf("%d",&minuman.nescafe);
            garistepi(100);
            sub.jmlbeli10=minuman.nescafe*5000;
    break;
    case 99:
            system("cls");
			Penghitungan();  
    break;
    case 55:
            system("cls"); 
            panggilMenu();  
    break;
    case 00:
            peyakinan:
            printf("Apakah anda yakin ingin keluar?\n\n[input Y untuk Ya]\t[input T untuk Tidak]\n\n");
            printf("Input Pilihan \t\t\t\t");scanf("%s",&yakin);

            if (yakin=='Y'||yakin=='y') 
            {
                system("cls");
                printf("\t\t- Terima Kasih atas kunjungan Anda -\n\n");
            system("pause");
            panggilMenu();
            }
            else if (yakin=='T'||yakin=='t')  
            {
                system("cls");
                panggilMenu();
            }
            else  //inputan user bukan Y atau T
            {
                printf("\nKesalahan inputan\n\n");
                system("pause");
                goto peyakinan;
            }

    break;
    default: 
        printf("Kesalahan inputan, menu no.%d tidak ada dalam daftar\n",menuminum.menuminuman);
        printf("- Silakan input kembali\n");
    break;

    }

}
}

void Penghitungan(void)
{
            printf("Pesanan Minuman \n");
            printf("\tJumlah  | Nama Minuman   | Total Harga\n\t====================================\n");
            printf("\t   %d   : FANTA          : Rp. %d \n",minuman.fanta, sub.jmlbeli1);
            printf("\t   %d   : COCA-COLA      : Rp. %d \n",minuman.cocacola, sub.jmlbeli2);
            printf("\t   %d   : SPRITE         : Rp. %d \n",minuman.sprite, sub.jmlbeli3);
            printf("\t   %d   : GREEN SANDS    : Rp. %d \n",minuman.greensands, sub.jmlbeli4);
            printf("\t   %d   : BINTANG RADLER : Rp. %d \n",minuman.bintangradler, sub.jmlbeli5);
            printf("\t   %d   : POCARI SWEET   : Rp. %d \n",minuman.pocarisweet, sub.jmlbeli6);
            printf("\t   %d   : HYDRO COCO     : Rp. %d \n",minuman.hydrococo, sub.jmlbeli7);
            printf("\t   %d   : ISO PLUS       : Rp. %d \n",minuman.isoplus, sub.jmlbeli8);
            printf("\t   %d   : MIZONE         : Rp. %d \n",minuman.mizone, sub.jmlbeli9);
            printf("\t   %d   : GOOD MOOD      : Rp. %d \n",minuman.goodmood, sub.jmlbeli10);
            printf("\t   %d   : AIR PUTIH      : Rp. %d \n",minuman.airputih, sub.jmlbeli11);
            printf("\t   %d   : MILO           : Rp. %d \n",minuman.milo, sub.jmlbeli12);
            printf("\t   %d   : TEH KOTAK      : Rp. %d \n",minuman.tehkotak, sub.jmlbeli13);
            printf("\t   %d   : NESCAFE        : Rp. %d \n",minuman.nescafe, sub.jmlbeli14);
            printf("\t---------------------------------------------------------\n");
   

            sub.totalharga=sub.jmlbeli1+sub.jmlbeli2+sub.jmlbeli3+sub.jmlbeli4+sub.jmlbeli5+sub.jmlbeli6+sub.jmlbeli7+sub.jmlbeli8+sub.jmlbeli9+sub.jmlbeli10+sub.jmlbeli11+sub.jmlbeli12+sub.jmlbeli13+sub.jmlbeli14;
            printf("\n===============================\nTotal Harga adalah = Rp.%d,-\n===============================\n",sub.totalharga);
           
   bayar:
            printf("\nMasukkan uang bayar = ");scanf("%d",&sub.bayar);
   
            if (sub.bayar>=sub.totalharga)
            {
            sub.kembalian=sub.bayar-sub.totalharga;
            printf("\nKembalian = %d", sub.kembalian);
            }
            else
            {
                printf("Uang Anda tidak cukup! Silakan input ulang\n");

                goto bayar;
            }
           
   printf("\nTekan apa saja untuk melihat struk pembayaran\n");
            system("Pause");
            system("cls");
            struk();
}

void struk(void)
    {
        time(&ambil_waktu); //mengambil waktu saat ini
        printf("=================================================================\n");
        printf("| \t\tMesin Minuman Kelompok 7             \t\t|\n");
        printf("| \t\tJl.Rungkut Anyar, Surabaya\t\t\t|\n| \t\t\tJawa Timur\t\t\t\t|\n");
        printf("| \t     Telp : (031)381936 / 0893749172543                 |\n");
        printf("|_______________________________________________________________|\n");
        printf("| Nama Pesanan  \t| Harga Satuan  | Jumlah  |    Total  \t|\n");
        printf("|===============================================================|\n");
        if (sub.jmlbeli1>0)
        {
        printf("| Fanta\t|     10.000\t|    %d\t  |  Rp.%d\t\t|",minuman.fanta,sub.jmlbeli1);
        }
                if (sub.jmlbeli2>0)
        {
        printf("\n| Coca-cola\t|     10.000\t|    %d\t  |  Rp.%d\t\t|",minuman.cocacola,sub.jmlbeli2);
        }
                if (sub.jmlbeli3>0)
        {
        printf("\n| Sprite\t|     10.000\t|    %d\t  |  Rp.%d\t\t|",minuman.sprite,sub.jmlbeli3);
        }
                if (sub.jmlbeli4>0)
        {
        printf("\n| Green Sands\t|     10.000\t|    %d\t  |  Rp.%d\t\t|",minuman.greensands,sub.jmlbeli4);
        }
                if (sub.jmlbeli5>0)
        {
        printf("\n| Bintang Radler\t|     20.000\t|    %d\t  |  Rp.%d\t\t|",minuman.bintangradler,sub.jmlbeli5);
        }
                if (sub.jmlbeli6>0)
        {
        printf("\n| Pocari Sweet\t|     10.000\t|    %d\t  |  Rp.%d\t\t|",minuman.pocarisweet,sub.jmlbeli6);
        }
                if (sub.jmlbeli7>0)
        {
        printf("\n| Hydro Coco\t|     10.000\t|    %d\t  |  Rp.%d\t\t|",minuman.hydrococo,sub.jmlbeli7);
        }
                if (sub.jmlbeli8>0)
        {
        printf("\n| Iso Plus\t|     10.000\t|    %d\t  |  Rp.%d\t\t|",minuman.isoplus,sub.jmlbeli8);
        }
                if (sub.jmlbeli9>0)
        {
        printf("\n| Mizone\t|     10.000\t|    %d\t  |  Rp.%d\t\t|",minuman.mizone,sub.jmlbeli9);
        }
                if (sub.jmlbeli10>0)
        {
        printf("\n| Good Mood\t|     20.000\t|    %d\t  |  Rp.%d\t\t|",minuman.goodmood,sub.jmlbeli10);
        }
        		if (sub.jmlbeli11>0)
        {
        printf("| Air Putih\t|     5.000\t|    %d\t  |  Rp.%d\t\t|",minuman.airputih,sub.jmlbeli11);
        }
                if (sub.jmlbeli12>0)
        {
        printf("\n| Milo\t|     5.000\t|    %d\t  |  Rp.%d\t\t|",minuman.milo,sub.jmlbeli12);
        }
                if (sub.jmlbeli13>0)
        {
        printf("\n| Teh Kotak\t|     5.000\t|    %d\t  |  Rp.%d\t\t|",minuman.tehkotak,sub.jmlbeli13);
        }
                if (sub.jmlbeli14>0)
        {
        printf("\n| Nescafe\t|     5000\t|    %d\t  |  Rp.%d\t\t|",minuman.nescafe,sub.jmlbeli14);
        }
        
        printf("\n|_______________________________________________________________|");
        printf("\n| Total Keseluruhan = %d\t\t\t\t\t|", sub.totalharga);
        printf("\n| Uang bayar        = %d\t\t\t\t\t|", sub.bayar);
        printf("\n| Kembalian         = %d\t\t\t\t\t|", sub.kembalian);
        printf("\n|                                                               |");
        printf("\n|                                                               |");
        printf("\n| Waktu/Hari : %s|", ctime (&ambil_waktu));
        printf("\n| Perhatian : Barang yang dibeli tidak bisa dikembalikan!\t|");
        printf("\n|                                                               |\n");
        printf("-----------------------------------------------------------------\n");


    }

