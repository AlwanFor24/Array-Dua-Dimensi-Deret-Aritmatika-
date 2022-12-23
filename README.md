# Ujian-Akhir-Semester_Dasar-Pemograman_1227050017
<br>Mata Kuliah 		: Dasar Pemograman
<br>Nama		      	: Alwan Maulana Firdaus
<br>NIM		           	:	1227050017
<br>Jurusan		    	:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 


## Deskripsi Umum
<br>Menampilkan deret aritmatika bilangan yag tidak habis dibagi 3, 5, 7. Input baris pertama merupakan banyaknya baris sedangkan baris kedua merupakan banyaknya kolom. Batas input adalah 0-20 . Output merupakan bilangan yang tidak habis dibagi 3, 5, 7. Algorima dari program ini adalah :
1. User menginputkan berapa banyak baris pada array mulai dari range 0-20.
2. User menginputkan berapa banyak baris pada array mulai dari range 0-20.
3. User menginputkan satu persatu nilai array,dimulai dari baris 1 dan kolom 1.
4. Jika sudah,nilai dalam array tersebut di tampilkan sesuai aturan matriks.
5. Kemudian nilai divalidasi kembali apakah nilai tersebut habis dibagi 3,5 dan 7.
6. Apabila nilai tadi habis dibagi 3,5 dan 7, maka nilai tidak akan ditampilkan, apabila tidak habis. tampilkan kembali kepada user


## Source Code
<code>
#include <iostream>

using namespace std;

void garis(){
	cout<<"---------------------"<<endl;
}

main(){
	int row,clm,x,y,z,i;
	cout<<"Banyak Baris: ";
	baris:
	cin>>row;
	if(row>20){
		cout<<"Oops mohon masukkan nilai dari 1-20!"<<endl;
		goto baris;
	}
	cout<<"Banyak kolom : ";
	cin>>clm;
	if(clm>20){
		cout<<"Oops mohon masukkan nilai dari 1-20!!"<<endl;
		goto baris;
	}
	garis();
	
	int array[row][clm];
    cout<<"Berikan nilai pada array!"<<endl;
    garis();
    for (x=1; x<=row; x++){
    	for(y=1; y<=clm; y++){
    		cout<<" Baris ke-"<<x<<" Kolom ke-"<<y<<": \n";
    		cin>>array[x][y];
		}
		garis();
	}	
	
	cout<<"Array awal : \n";
	garis();
	for(x=1;x<=row;x++){
		for(y=1;y<=clm;y++){
				cout<<" "<<array[x][y];
		}
		cout<<endl;
	}
	garis();
	
	int hasil[x * y];
	int kali=0;
	for(x=1;x<=row;x++){
		for(y=1;y<=clm;y++){
			if(array[x][y]%3 != 0 && array[x][y]%5 != 0 && array[x][y]%7 != 0){
				hasil[kali]=array[x][y];
				kali++;
			}
		}
	}
	
	cout<<"Hasilnya yang tidak bisa dibagi 3, 5, 7 adalah : ";
	for(int i = 0; i < kali; i++){
		cout<<hasil[i];
		if(i < kali -1){
			cout<<", ";
		}else{
			cout<<".";
		}
	}
}
</code>

## Output
<img width="656" alt="Screenshot 2022-12-24 004031" src="https://user-images.githubusercontent.com/121307307/209381794-ab4da6f5-8976-477c-8240-2941528d914e.png">

